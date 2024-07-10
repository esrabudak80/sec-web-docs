###   sgmKalem  Validasyon
**Zorunlu Alanlar:**
- ``beyannameid``: string, UUID formatında, zorunlu
- ``edisirano``: tam sayı, zorunlu
- ``sirano``: sayı, zorunlu
- ``teslimsekli``: string, maksimum uzunluk: 3, zorunlu
- ``gtip``: string, maksimum uzunluk: 16, zorunlu
- ``ticaritanim``: string, maksimum uzunluk: 210, zorunlu
- ``menseulke``: string, maksimum uzunluk: 4, zorunlu
- ``rejim``: string, maksimum uzunluk: 4, zorunlu
- ``kapadet``: tam sayı, maksimum: 4, zorunlu
- ``ozellik``: string, maksimum uzunluk: 2, zorunlu
- ``kapcinsi``: string, maksimum uzunluk: 9, zorunlu
- ``faturatutari``: sayı, zorunlu
- ``faturatutaritl``: sayı, zorunlu
- ``fobtutar``: sayı, zorunlu
- ``istatistikikiymet``: sayı, zorunlu
- ``burutagirlik``: sayı, zorunlu
- ``netagirlik``: sayı, zorunlu
- ``birimi``: string, maksimum uzunluk: 10, zorunlu
- ``miktari``: sayı, zorunlu
- ``olcumiktari``: sayı, zorunlu
- ``olcubirimi``: string, maksimum uzunluk: 3, zorunlu
- ``muafiyet1``: string, maksimum uzunluk: 9, zorunlu
- ``kalemislemniteligi``: string, maksimum uzunluk: 2, zorunlu
- ``giriscikisamaci``: string, maksimum uzunluk: 2, zorunlu
- ``giriscikisamaciaciklama``: string, maksimum uzunluk: 300, zorunlu
- ``kapkonteynerno``: string, maksimum uzunluk: 30, zorunlu

**İsteğe Bağlı Alanlar:**
- ``imalatcifirmaid``: string, UUID formatında, isteğe bağlı
- ``ambalajturu``: string, maksimum uzunluk: 5, isteğe bağlı
- ``sgmKalemdiib``: dizi, ``sgmKalemDiibSchema`` şemasındaki ``kalemid`` hariç, isteğe bağlı
- ``sgmKalemEsyaGeriGelmeSebebi``: dizi, ``sgmKalemEsyaGeriGelmeSebebiSchema`` şemasındaki ``kalemid`` hariç, isteğe bağlı
- ``sgmKalemEkBelge``: dizi, ``sgmKalemEkBelgeSchema`` şemasındaki ``kalemid`` hariç, isteğe bağlı
- ``sgmKalemVergi``: dizi, ``sgmKalemVergiSchema`` şemasındaki ``kalemid`` hariç, isteğe bağlı
- ``sgmKalemKonteyner``: dizi, ``sgmKalemKonteynerSchema`` şemasındaki ``kalemid`` hariç, isteğe bağlı
- ``sgmKalemOdemeSekli``: dizi, ``sgmKalemOdemeSekliSchema`` şemasındaki ``kalemid`` hariç, isteğe bağlı
- ``sgmKalemDetay``: dizi, ``sgmKalemDetaySchema`` şemasındaki ``kalemid`` hariç, isteğe bağlı
- ``sgmKalemMarka``: dizi, ``sgmKalemMarkaSchema`` şemasındaki ``kalemid`` hariç, isteğe bağlı
- ``sgmTesvikCikis``: dizi, ``sgmTesvikCikisSchema`` şemasındaki ``kalemid`` hariç, isteğe bağlı
- ``sgmKalemAcmaKapama``: dizi, ``sgmKalemAcmaKapamaSchema`` şemasındaki ``kalemid`` hariç, isteğe bağlı
### sgmKalemOdemeSekli Validasyon
**Zorunlu Alanlar:**
- ``odemeseklikodu``: string, maksimum uzunluk: 2, zorunlu
**İsteğe Bağlı Alanlar:**
- ``odemetutari``: sayı, isteğe bağlı
- ``tbfid``: string, maksimum uzunluk: 30, isteğe bağlı
### sgmKalemVergi Validasyon
**İsteğe Bağlı Alanlar:**
- ``kodu``: string, maksimum uzunluk: 5, isteğe bağlı
- ``tutari``: sayı, isteğe bağlı
- ``orani``: string, maksimum uzunluk: 60, isteğe bağlı
- ``odemesekli``: string, uzunluk: 1, isteğe bağlı
- ``carpilan``: string, maksimum uzunluk: 10, isteğe bağlı
- ``gumrukteodeme``: string, maksimum uzunluk: 5, isteğe bağlı
- ``islemtipi``: string, maksimum uzunluk: 10, isteğe bağlı
- ``matrah``: sayı, isteğe bağlı
### sgmTesvikGirisCikis  Validasyon
**Zorunlu Alanlar:**
- ``tesvikgirisid``: string, UUID formatında, zorunlu

**İsteğe Bağlı Alanlar:**
- ``kalemsirano``: sayı, isteğe bağlı
- ``miktar``: sayı, nullable, isteğe bağlı
- ``miktarkg``: sayı, nullable, isteğe bağlı
- ``tutar``: sayı, nullable, isteğe bağlı
- ``aciklama``: string, nullable, isteğe bağlı
- ``kalemacmakapamaid``: string, UUID formatında, isteğe bağlı
- ``birimfiyat``: sayı, nullable, isteğe bağlı
- ``dovizkur``: sayı, nullable, isteğe bağlı
- ``vergioran``: sayı, nullable, isteğe bağlı
- ``exfaturano``: string, maksimum uzunluk: 25, nullable, isteğe bağlı
- ``forma``: string, maksimum uzunluk: 25, nullable, isteğe bağlı
- ``kontroledildi``: string, uzunluk: 1, default değeri: 'F', isteğe bağlı
- ``raporno``: string, maksimum uzunluk: 20, nullable, isteğe bağlı
- ``raportarih``: tarih, nullable, isteğe bağlı
- ``raporkg``: sayı, nullable, isteğe bağlı
- ``brutkg``: sayı, nullable, isteğe bağlı
- ``fobtutar``: sayı, nullable, isteğe bağlı
- ``iptaledildi``: boolean, nullable, isteğe bağlı
- ``tesciledildi``: boolean, nullable, isteğe bağlı
### sgmKalemMarka Validasyon
**İsteğe Bağlı Alanlar:**
- ``markaturu``: string, isteğe bağlı
- ``markatescilno``: string, maksimum uzunluk: 50, isteğe bağlı
- ``markaadi``: string, maksimum uzunluk: 150, isteğe bağlı
- ``markakiymeti``: sayı, isteğe bağlı
- ``referansno``: string, maksimum uzunluk: 50, isteğe bağlı
- ``modelyili``: string, maksimum uzunluk: 10, isteğe bağlı
- ``model``: string, maksimum uzunluk: 50, isteğe bağlı
- ``motorhacmi``: string, maksimum uzunluk: 10, isteğe bağlı
- ``silindiradedi``: tam sayı, isteğe bağlı
- ``renk``: string, maksimum uzunluk: 20, isteğe bağlı
- ``motorgucu``: tam sayı, isteğe bağlı
- ``motortipi``: string, isteğe bağlı
- ``vites``: string, isteğe bağlı
- ``motorno``: string, maksimum uzunluk: 30, isteğe bağlı
- ``imeino``: string, maksimum uzunluk: 15, isteğe bağlı
### sgmKalemKonteyner Validasyon
**Zorunlu Alanlar:**
- ``kapkonteynerno``: string, maksimum uzunluk: 30, zorunlu
- ``konteynerulke``: string, maksimum uzunluk: 4, zorunlu
- ``konteynertipi``: tam sayı, zorunlu
- ``limancikistarih``: tarih, zorunlu
### sgmKalemEsyaGeriGelmeSebebi Validasyon
**Zorunlu Alanlar:**
- ``esyagerigelmesebebikod``: tam sayı, zorunlu
**İsteğe Bağlı Alanlar:**
- ``aciklama``: string, maksimum uzunluk: 100, isteğe bağlı
### sgmKalemEkBelge Validasyon
**Zorunlu Alanlar:**
- ``grupkodu``: string, uzunluk: 1, default değeri: '3', zorunlu
**İsteğe Bağlı Alanlar:**
- ``ekbelgekodu``: string, maksimum uzunluk: 4, isteğe bağlı
- ``dogrulama``: string, isteğe bağlı
- ``referans``: string, maksimum uzunluk: 100, isteğe bağlı
- ``id``: tam sayı, isteğe bağlı
- ``belgetamamlamatarihi``: tarih, isteğe bağlı
- ``arsivid``: string, UUID formatında, isteğe bağlı
- ``belgedosyaad``: string, maksimum uzunluk: 250, isteğe bağlı
- ``vizetarihi``: tarih, isteğe bağlı

### sgmKalemDiib Validasyon
**Zorunlu Alanlar:**
- ``diibbelgeno``: string, maksimum uzunluk: 20, zorunlu
### sgmKalemDetay Validasyon
**Zorunlu Alanlar:**
- ``beyannameid``: string, UUID formatında, zorunlu
- ``esyatanimid``: string, UUID formatında, zorunlu
- ``gc``: string, uzunluk: 1, zorunlu
**İsteğe Bağlı Alanlar:**
- ``kap``: tam sayı, isteğe bağlı
- ``miktar``: tam sayı, isteğe bağlı
- ``brutkg``: sayı, isteğe bağlı
- ``netkg``: sayı, isteğe bağlı
- ``tutar``: sayı, isteğe bağlı
- ``dovizcinsi``: string, isteğe bağlı
- ``aciklama``: string, maksimum uzunluk: 255, isteğe bağlı
- ``faturano``: string, maksimum uzunluk: 50, isteğe bağlı
- ``faturatarih``: tarih, isteğe bağlı
- ``bolen``: string, maksimum uzunluk: 10, isteğe bağlı
- ``musrefno1``: string, maksimum uzunluk: 255, isteğe bağlı
- ``musrefno2``: string, maksimum uzunluk: 2500, isteğe bağlı
- ``tutar2``: sayı, isteğe bağlı
- ``antrepobeyannameno``: string, isteğe bağlı
- ``antrepokalemsirano``: tam sayı, isteğe bağlı
- ``worawid``: string, UUID formatında, isteğe bağlı
- ``masterid``: string, UUID formatında, isteğe bağlı
- ``deliveryno``: string, maksimum uzunluk: 13, isteğe bağlı
- ``menseulke``: string, maksimum uzunluk: 4, isteğe bağlı
- ``yatirimtesvikbelgeno``: string, maksimum uzunluk: 50, isteğe bağlı
- ``yatirimtesviktarihi``: tarih, isteğe bağlı
- ``cikisulkeliman``: string, maksimum uzunluk: 10, isteğe bağlı
- ``gondericireferans``: string, maksimum uzunluk: 50, isteğe bağlı
- ``konsimantono``: string, maksimum uzunluk: 25, isteğe bağlı
- ``konteynernumara``: string, maksimum uzunluk: 25, isteğe bağlı
- ``gemiadi``: string, maksimum uzunluk: 100, isteğe bağlı
- ``tasiyicikodu``: string, maksimum uzunluk: 10, isteğe bağlı
- ``bosaltmalimani``: string, maksimum uzunluk: 25, isteğe bağlı
- ``ilaveedilecekkiymet``: sayı, isteğe bağlı
- ``entegrasyonno``: string, maksimum uzunluk: 50, isteğe bağlı
### sgmKalemAcmaKapama Validasyon
**Zorunlu Alanlar:**
- ``kalemsirano``: tam sayı, zorunlu
- ``miktar``: sayı, zorunlu
**İsteğe Bağlı Alanlar:**
- ``beyannameno``: string, isteğe bağlı
- ``cikiskapadet``: tam sayı, isteğe bağlı
- ``dusumsira``: tam sayı, isteğe bağlı
- ``aciklama``: string, maksimum uzunluk: 100, isteğe bağlı