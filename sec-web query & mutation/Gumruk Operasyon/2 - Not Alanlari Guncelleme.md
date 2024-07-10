- `sgm_gumrukoperasyontakip`  tablosundaki `bildirimnotu` ve `takipnotu` alani icin enum degerleri mevcuttur. Gelen `noteType` degerine gore `bildiirmnotu` veya `takipnotu` degeri guncellenir.

```
enum NoteType {
BILDIRIM = 'BILDIRIM',
TAKIP = 'TAKIP',
}
```

- `updateSgmGumrukOperasyonTakipNot` mutation `gumrukoperasyontakipid`,   `noteType`, `note` olarak uc parametre alir. 

```
updateSgmGumrukOperasyonTakipNot(id: "", noteType: TAKIP, note: "TEST") {
durum
takipnotu
bildirimnotu
takibealan
}
```

