- `sbr_firma` tablosunda `input`  degeri `ad` veya `ozelkod` alanlari arasindan arama yapilir. `ad` alanina gore siralanarak listelenir.
- Ornek Request:
```
sbrFirmasByFilterBasic( input: {
searchText: "",
firmaType: sorumlu
}) {
ad
adres1
adres2
postakod
sehirad
ulkead
uyar
}
```