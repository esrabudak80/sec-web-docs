- `sgm_beyanname.bankaodemesekli` alanındaki kod değeri bu alana yansıtılır.
- `sbrOdemeSekliByKod (edikod: string)` querysine ilgili beyannamenin `bankaodemesekli` `edikod` parametresine gonderilir.
- Ornek request
```
sbrOdemeSekliByKod(edikod: "4") {
ad
}
```