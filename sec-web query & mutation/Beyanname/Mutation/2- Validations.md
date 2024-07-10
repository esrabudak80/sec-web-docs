### sgmBeyannameSchema Validasyon

**Zorunlu Alanlar:**

- `departmanid`: string, UUID formatında, zorunlu
- `referansno`: sayı, zorunlu
- `musteriid`: string, UUID formatında, zorunlu
- `kullanicikod`: string, zorunlu
- `gondericiid`: string, UUID formatında, zorunlu
- `faturafirmaid`: string, UUID formatında, zorunlu
- `aliciid`: string, UUID formatında, zorunlu
- `belgesayisi`: sayı, zorunlu
- `sevkulke`: string, maksimum uzunluk: 4, zorunlu
- `cikisulke`: string, maksimum uzunluk: 4, zorunlu
- `ticyapilanulke`: string, maksimum uzunluk: 4, zorunlu
- `kurtarihi`: tarih veya string, zorunlu
- `odemesekli`: string, maksimum uzunluk: 9, zorunlu
- `aciklama`: string, maksimum uzunluk: 500, zorunlu
- `gonderilengumruk`: string, maksimum uzunluk: 6, zorunlu
- `yukbosgumruk`: string, maksimum uzunluk: 6, zorunlu
- `rejim`: string, maksimum uzunluk: 4, zorunlu
- `toplamkap`: sayı, zorunlu
- `teslimsekli`: string, zorunlu
- `teslimyeri`: string, maksimum uzunluk: 40, zorunlu
- `faturadovizturu`: string, maksimum uzunluk: 3, zorunlu
- `dovizalis`: sayı, zorunlu
- `fobtutar`: sayı, zorunlu
- `konteynersayisi`: sayı, zorunlu
- `tasimasekli`: string, maksimum uzunluk: 2, zorunlu
- `sozlesmeturu`: string, maksimum uzunluk: 2, zorunlu
- `faturatutari`: sayı, zorunlu
- `konteyner`: boolean, zorunlu

**İsteğe Bağlı Alanlar:**

- `giriscikisgumruk`: string, maksimum uzunluk: 6, isteğe bağlı
- `beyansahibiid`: string, UUID formatında, isteğe bağlı
- `gidecegiulke`: string, maksimum uzunluk: 4, isteğe bağlı
- `esyaninbulunduguyer`: string, maksimum uzunluk: 40, isteğe bağlı
- `birlikkod`: string, maksimum uzunluk: 10, isteğe bağlı
- `genelsekreterlikkod`: string, maksimum uzunluk: 10, isteğe bağlı
- `birlikkayitno`: string, maksimum uzunluk: 20, isteğe bağlı
- `kriptokodu`: string, maksimum uzunluk: 35, isteğe bağlı
- `birliktutari`: sayı, isteğe bağlı
- `tescilno`: string, isteğe bağlı
- `tesciltarihi`: tarih veya string, isteğe bağlı
- `intactarihi`: tarih veya string, isteğe bağlı
- `musterireferansno`: string, maksimum uzunluk: 25, isteğe bağlı
- `musterireferansno2`: string, isteğe bağlı
- `onaykod`: string, maksimum uzunluk: 16, isteğe bağlı
- `bankaodemesekli`: string, maksimum uzunluk: 2, isteğe bağlı
- `odemearaci`: string, maksimum uzunluk: 2, isteğe bağlı
- `banka`: string, maksimum uzunluk: 12, isteğe bağlı
- `cikisaractipi`: string, maksimum uzunluk: 1, isteğe bağlı
- `cikisaracno`: string, maksimum uzunluk: 35, isteğe bağlı
- `cikisaraculke`: string, maksimum uzunluk: 4, isteğe bağlı
- `siniraractipi`: string, maksimum uzunluk: 1, isteğe bağlı
- `siniraracno`: string, maksimum uzunluk: 35, isteğe bağlı
- `nakliyeci`: string, maksimum uzunluk: 50, isteğe bağlı
- `tasiyicifirmaid`: string, UUID formatında, isteğe bağlı
- `basitusul`: sayı, isteğe bağlı
- `yukbosyer`: string, maksimum uzunluk: 50, isteğe bağlı
- `acentasevkbildirimno`: string, maksimum uzunluk: 20, isteğe bağlı
- `limankodu`: string, maksimum uzunluk: 10, isteğe bağlı
- `entegrasyonno`: string, maksimum uzunluk: 50, isteğe bağlı
- `tev`: sayı, isteğe bağlı