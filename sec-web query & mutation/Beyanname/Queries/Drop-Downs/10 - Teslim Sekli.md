- `sbr_teslimsekli` tablosunda `input`  degeri `ad` veya `edikod` alanlari arasindan arama yapilir. `ad` alanina gore siralanarak listelenir.
- `input` degeri gonderilmezse databaseden `1000` data seklinde donus yapar.
- Ornek Request:
```
sbrTeslimSeklis (input: "S"){
	edikod
	ad
}
```