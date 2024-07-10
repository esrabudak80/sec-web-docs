- `sgm_beyannamemuskontrol` tablosu islemleri
- `updateSgmBeyannameMusKontrol` mutationindan `beyannameid` ve `UpdateSgmBeyannameKontrolInput` tipinde `input` beklenir.

```
input UpdateSgmBeyannameKontrolInput {
kontroldenalannot: String!
hatali: Boolean
hatagiderildi: Boolean
tcgbacmalar: Boolean
hatasiz: Boolean
gondericialici: Boolean
kapadedi: Boolean
cikisulkesi: Boolean
sevkulkesi: Boolean
teslimsekli: Boolean
faturatutari: Boolean
faturadovizcinsi: Boolean
navluntutari: Boolean
sigortaturari: Boolean
odemesekli: Boolean
banka: Boolean
konteynerno: Boolean
gtip: Boolean
menseulke: Boolean
burutagirlik: Boolean
netagirlik: Boolean
uluslararasianlasma: Boolean
kalemrejim: Boolean
birimmiktar: Boolean
ekbilgivebelge: Boolean
vergioran: Boolean
teminatturorantutar: Boolean
yurticitutari: Boolean
yurtdisitutari: Boolean
muafiyet: Boolean
ozellikbedellibedelsiz: Boolean
kapatma: Boolean
aciklama: Boolean
istatistikikiymet: Boolean
tamamlayiciolcu: Boolean
}
```

- Sayfa genelde checkbox ile hata isaretleme sayfasidir. Hatali alanlar backende `1` degerinde isaretlenerek gonderilir. `kontroldenalannot` alani zorunlu bir alandir. 
- Ornek request: 
  
```
  updateSgmBeyannameMusKontrol(
    beyannameid: "DDAD6B8F-DBD2-43D7-B418-CF0EE225C5D8", 
    input: {
      kontroldenalannot: "Test2 kontrol denalannot metni",
      hatali: true,
      hatagiderildi: false,
      tcgbacmalar: true,
      hatasiz: true,
      gondericialici: true,
      kapadedi: false,
      cikisulkesi: true,
      sevkulkesi: false,
      teslimsekli: true,
      faturatutari: false,
      faturadovizcinsi: true,
      navluntutari: true,
      sigortatutari: false,
      odemesekli: true,
      banka: false,
      konteynerno: true,
      gtip: false,
      menseulke: true,
      burutagirlik: false,
      netagirlik: true,
      uluslararasianlasma: false,
      kalemrejim: true,
      birimmiktar: false,
      ekbilgivebelge: true,
      vergioran: false,
      teminatturorantutar: true,
      yurticitutari: false,
      yurtdisitutari: true,
      muafiyet: false,
      ozellikbedellibedelsiz: true
      kapatma: false
	  aciklama: true
	  istatistikikiymet: false
	  tamamlayiciolcu:true
    }) {
      kontroldenalannot
      hatali
      hatagiderildi
      tcgbacmalar
      hatasiz
      gondericialici
      kapadedi
      cikisulkesi
      sevkulkesi
      teslimsekli
      faturatutari
      faturadovizcinsi
      navluntutari
      sigortatutari
      odemesekli
      banka
      konteynerno
      gtip
      menseulke
      burutagirlik
      netagirlik
      uluslararasianlasma
      kalemrejim
      birimmiktar
      ekbilgivebelge
      vergioran
      teminatturorantutar
      yurticitutari
      yurtdisitutari
      muafiyet
      ozellikbedellibedelsiz
	  kapatma
      istatistikikiymet
	  tamamlayiciolcu
	  aciklama
    }
```
