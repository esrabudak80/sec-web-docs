- `sbr_banka` tablosunda `input`  degeri `ad` veya `edikod` alanlari arasindan arama yapilir. `edikod` alanina gore siralanarak listelenir.
- `input` degeri gonderilmezse databaseden `1000` data seklinde donus yapar.
- Ornek Request:
```
sbrBankas (input: "S"){
	edikod
	ad
}
```