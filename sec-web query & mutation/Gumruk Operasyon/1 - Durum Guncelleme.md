```
enum SgmGumrukOperasyonTakipDurum {
BILDIRILDI = 100,
BILDIREN_NOT_DEGISTIRILDI = 150,
TAKIBE_ALINDI = 200,
TAKIBE_ALAN_NOT_DEGISTIRILDI = 250,
GERI_VERILDI = 300,
YAZDIRILDI = 500,
TAMAMLANDI = 900,
}
```

- `sgm_gumrukoperasyontakip` ve `sgm_gumrukoperasyontakip_log` tablosundaki `durum` alani icin yukaridaki enum degerleri mevcuttur.
- `updateSgmGumrukOperasyonTakipDurum` mutation `gumrukoperasyontakipid` ile  input olarak  `UpdateSgmGumrukOperasyonTakipDurumInput` alir. 

```
input UpdateSgmGumrukOperasyonTakipDurumInput {
durum: Int!
aciklama: String
}
```

```
updateSgmGumrukOperasyonTakipDurum(id: "", input: {
durum: 200,
aciklama: "Test"
}) {
durum
takipnotu
bildirimnotu
takibealan
}
```

-  Inputtaki `aciklama` alani nullable bir alandir. `durum` degeri `300` ise aciklama alani zorunludur. Inputta `aciklama` gelmezse hata firlatilir.