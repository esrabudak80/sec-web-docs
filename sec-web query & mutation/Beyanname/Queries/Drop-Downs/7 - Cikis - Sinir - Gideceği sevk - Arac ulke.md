- `sbr_ulke` tablosunda `input`  degeri `ad` veya `edikod` alanlari arasindan arama yapilir. `ad` alanina gore siralanarak listelenir.
- `input` degeri gonderilmezse databaseden `1000` data seklinde donus yapar.
- Ornek Request:
```
sbrUlkes (input: "S"){
	edikod
	ad
	orijinalad
	ingilizcead
}
```