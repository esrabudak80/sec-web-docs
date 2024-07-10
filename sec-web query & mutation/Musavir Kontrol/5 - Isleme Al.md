- Sağ click basıldığında **'kontrolden al'** seçilir. Dosya işleme alınır. Kontrolden alan kolonu ve kontrolden alma zamanı değişir.
- `sgm_beyannamemuskontrol` tablosuna `beyannameid` ile istek atilir.
- `updateSgmBeyannameMusKontrolKontroldenAlan` mutation inda `beyannameid` parametre olarak beklenir.
- `kontroldenalan` `context.currentUser.kod` ile guncellenir. `kontalmazamani` `new Date()` olarak guncellenir.

Ornek Request: 
```
updateSgmBeyannameMusKontrolKontroldenAlan(beyannameid: "") {
kontroldenalan
kontalmazamani
upddate
upduser
}
```