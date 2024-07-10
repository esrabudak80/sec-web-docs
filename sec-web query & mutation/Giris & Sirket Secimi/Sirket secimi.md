- once `sbrSubesFilteredByKod` `sbr_sube` `kod` `101` olanlarin querysi ile listeleme yapilir.
```
sbrSubesFilteredByKod {
	id
	ad
	sbrSirket {
	id
	ad
}}
```

```
  skyKullaniciSubeByKullaniciKod(kullanicikod: "SEMIHB") {
        id
        kullanicikod
        subeid
        onay
        sbrSube {
            id
            ad
            sbrSirket {
                id
                ad
            }
        }
    }
```

