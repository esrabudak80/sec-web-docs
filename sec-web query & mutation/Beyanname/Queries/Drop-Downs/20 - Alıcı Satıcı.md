- `sgm_alicisatici` tablosunda `input`  degeri `ad` veya `kod` alanlari arasindan arama yapilir. `ad` alanina gore siralanarak listelenir.
- `input` degeri gonderilmezse databaseden `500` data seklinde donus yapar.
- Ornek Request:
```
sgmAliciSaticis (input: "S"){
	id
	kod
	ad
}
```