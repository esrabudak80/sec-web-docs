- `sbr_gumruk` tablosunda `input`  degeri `ad` veya `kod` alanlari arasindan arama yapilir. `edikod` alanina gore siralanarak listelenir.
- `input` degeri gonderilmezse databaseden `500` data seklinde donus yapar.
- Ornek Request:
```
sbrGumruks (input: "S") {
	edikod
	ad
}
```