### İş Süreci ve Kuralları Analizi
1. **Gönderici Butonundan Seçim Yapıldığında:**
- Kullanıcı, Gönderici seçim butonuna tıkladığında bir müşteri seçer.
#### 4. **Veri Modülü ile Çalışma:**
- `DmBeyanname1` veri modülü kullanılarak işlemler gerçekleştirilir.
- Bu veri modülü, beyannamelerle ilgili veri işlemlerini yönetir.
#### 6. **İhracat Durumunda Gönderici ID'si Güncellenmesi:**
- **İşlem Türü Kontrolü:**
    - `FBeyannameIslemTuru` değişkeni 'EX' (ihracat) ise:
        - `TbBeyannamegondericiid` alanı, seçilen müşteri ID'si (`DmBeyanname2.QryMusteriKodPopfirmaid.AsString`) ile güncellenir.
    - Beyanname **ihracatsa (EX)**  beyannamenin **göndericiid**’si **firmaid** ile doldurulur. 
#### 7. **İthalat Durumunda Alıcı ID'si Güncellenmesi:**
- **Aksi Durum:**
    - Eğer `FBeyannameIslemTuru` 'EX' değilse:
        - `TbBeyannamealiciid` alanı, seçilen müşteri ID'si ile güncellenir.
        - Bu işlem, beyannamenin alıcı ID'sini seçilen müşteri firması ile günceller.
#### 8. **Uyarı Mesajlarının Gösterilmesi:**
- Seçilen müşteriyle ilgili bir uyarı durumu varsa (`QryMusteriKodPopuyar` true ise):
    - Kullanıcıya bir uyarı mesajı (`SiberMessageDlg`) gösterilir
#### 9. **Beyanname Sabit Bilgilerinin Güncellenmesi:**
- `BeyannameSabit` prosedürü çağrılarak, müşteri ID'si, gönderici ID'si ve alıcı ID'si kullanılarak beyanname sabit bilgileri güncellenir.
- Bu prosedür, beyannamenin sabit bilgilerini doğru bir şekilde güncelleyerek işlem devamlılığını sağlar.

#### 11. **Fatura Firması Kontrolü ve Ataması:**
   - **Veritabanı Sorgusu:**
     - Yeni bir sorgu (`XQTemp`) oluşturularak, veritabanından, seçilen müşteri grubunda fatura adresi olan bir firma sorgulanır.
```
select firmaid from sbr_firma (nolock) where grupfirmaid= :grupfirmaid and faturadresi=1
```

   - **Sonuç Kontrolü:**
     - Eğer böyle bir firma bulunamazsa (`XQTemp.IsEmpty`), `TbBeyannamefaturafirmaid` alanı, seçilen müşteri ID'si ile güncellenir. Bu, seçilen müşterinin aynı zamanda fatura firması olarak kullanılmasını sağlar.
    #### 12. **Blokaj Kontrolü:**

- **Bloke Durumu:**
    - Eğer müşteri ilişkileri tarafından müşteri bloke edilmişse (`QryMusteriKodPopmuhbloke` true ise):
        - Bir hata mesajı (`SiberRaise`) gösterilir ve işlem durdurulur.
        - Bu, bloke edilmiş müşterilerle işlem yapılmasını engeller. Örneğin, müşterinin ödemelerinde sorun varsa veya başka bir nedenle işlem yapması engellenmişse, bu kontrol devreye girer.
```
SiberRaise('Firma Müşteri İlişkileri Tarafından Bloke Edilmiştir. İşlemi Yapamazsınız.')
```
    
### Gonderici seciminde islemler ozet: 
1 - **Müşteri Seçimi ve Onayı:**
2 - **İhracat Durumunda Gönderici Güncelleme:**
3 - **İthalat Durumunda Alıcı Güncelleme:**
4 - **Uyarı Mesajlarının Gösterilmesi:**
5 - **Beyanname Sabit Bilgilerinin Güncellenmesi:**
6 - **Fatura Firması Kontrolü ve Ataması:**
7 - **Blokaj Kontrolü:**

### 080114 Yetkisi Olan Kullanicilarda Gonderici Secimi
```
select * from sky_yetki where kod = '080114'
```
- Eğer beyanname işlem türü **IM** ise **sevk ülkesi (sgm_beyanname.sevkulke)**  ve **ticaret yapılan ülkesi (sgm_beyanname.ticyapilanulke)**, **gönderici ülke kodu** ile doldurulur. 
- Beyanname rejimi **TREX**’den farklı ise **gideceği ülke (sgm_beyanname.gidecegiulke)** alanına otomatik olarak **052(TÜRKİYE)** yazılır.
- Beyanname **çıkış ülkesi (sgm_beyanname.cikisulke)** de **gönderici ülke kodu** ile doldurulur.
#### 1 - **Gönderici ID Kontrolü ve Ataması:**
- Gönderici ID (`vGondericiId`) belirlenir.
- Eğer `TbBeyannameGondericiid` boşsa, `vGondericiId` değeri `pGondericiId` olarak atanır.
- Aksi durumda, `TbBeyannameGondericiid` değeri `vGondericiId` olarak atanır
#### 2. **Gönderici Bilgilerinin Sorgulanması:**
- `QryGondericiDisp` sorgusu kapatılır.
- `firmaid` parametresi `vGondericiId` olarak ayarlanır.
- `QryGondericiDisp` sorgusu açılır ve gönderici bilgileri yüklenir.
#### 3. **İthalat İşlem Türü Kontrolü:**
- Eğer `FBeyannameIslemTuru` 'IM' (ithalat) ise, aşağıdaki işlemler gerçekleştirilir:
    - `FDontCheckTeslimYeri` değişkeni true olarak ayarlanır. Bu, teslim yeri kontrolünün geçici olarak devre dışı bırakılması için yapılır.
    - Beyanname alanları (`SevkUlke`, `TicYapilanUlke`, `GidecegiUlke`, `CikisUlke`) `QryGondericiDisp` sorgusundan alınan ülke kodu ile güncellenir.
        - `SevkUlke`, `TicYapilanUlke`, `CikisUlke` alanları gönderici ülke kodu ile güncellenir.
        - Eğer `TbBeyannameRejim` 'TREX' değilse, `GidecegiUlke` alanı '052' olarak ayarlanır.
#### 4. **Gönderici ve Alıcı ID Kontrolü:**
- Eğer `vGondericiId` boş değilse (`''`) ve `TbBeyannamealiciid` boş değilse, aşağıdaki işlemler gerçekleştirilir:
    - Yeni bir sorgu (`XQTemp`) oluşturulur.
    - `beyannameid`, `aliciid`, `gondericiid`, `firmaid` parametreleri ile sorgu çalıştırılır.
    - Eğer sorgu sonucu boş değilse (`XQTemp.IsEmpty`), beyanname açıklaması (`TBBeyannameaciklama`) güncellenir.
        - `XQTemp` sorgusundan alınan açıklama, mevcut açıklamaya eklenir (250 karakterle sınırlıdır).
#### **5. Teslim Yeri Ayarı:**
- `SetBeyannameTeslimYeri` prosedürü çağrılarak teslim yeri bilgileri ayarlanır.