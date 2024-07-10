- `sbr_liman` tablosunda `input`  degeri `ad` veya `edikod` alanlari arasindan arama yapilir.
- `input` degeri gonderilmezse databaseden `1000` data seklinde donus yapar.
- Ornek Request:
```
sbrLimans (input: "S") {
	id
	ad
	edikod
}
```