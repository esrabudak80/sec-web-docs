- `sbr_firma` tablosunda `input`  degeri `ad` veya `ozelkod` alanlari arasindan arama yapilir. `ad` alanina gore siralanarak listelenir.
- Ornek Request:
```
sbrFirmasByFilterBasic( input: {
searchText: "",
firmaType: nakliyeci
}) {
	id
	ozelkod
	ad
}
```