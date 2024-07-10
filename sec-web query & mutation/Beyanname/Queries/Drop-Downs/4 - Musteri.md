- `sbr_firma` tablosunda `input`  degeri `ad` veya `ozelkod` alanlari arasindan arama yapilir. `ad` alanina gore siralanarak listelenir.
- `input` degeri gonderilmezse databaseden `1000` data seklinde donus yapar.
- Ornek Request:
```
sbrFirmasByFilterBasic( input: {
searchText: "",
firmaType: gumrukmusteri
}) {
	id
	gumrukmusteri
	ozelkod
	ad
	adres1
	adres2
	postakod
	sehirad
	ulkead
	uyar
}
```