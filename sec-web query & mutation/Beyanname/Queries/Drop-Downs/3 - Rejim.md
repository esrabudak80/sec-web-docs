- `sgm_rejim` tablosunda `input`  degeri `ad` veya `kod` alanlari arasindan arama yapilir. `kod` alanina gore siralanarak listelenir.
- `input` degeri gonderilmezse databaseden `1000` data seklinde donus yapar.
- Ornek Request:
```
sgmRejims (input: "S"){
	kod
	ad
}
```