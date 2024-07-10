- `sbr_firma` tablosunda `input`  degeri `ad` veya `ozelkod` alanlari arasindan arama yapilir. `ad` alanina gore siralanarak listelenir.
- `input` degeri gonderilmezse databaseden `1000` data seklinde donus yapar.
- Ornek Request:
```
sbrFirmas(
	args: {
		where: {
			sirketid: "BA3159D5-B9DF-4FA9-9EA3-17B4F9A99BAB",
			OR: [
			{ faturadresi: true },
			{ gumrukmusteri: true }
			],
			aktif: 1,
			grupfirmaid: "94F9B361-9114-4970-B69D-22A79E938972"}}) {
	id
	ozelkod
	ad
	adres1
	adres2
	postakod
	sehirad
	ulkead
	uyar
	aciklama
}
```