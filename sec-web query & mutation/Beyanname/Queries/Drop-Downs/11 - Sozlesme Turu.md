- `sgm_ticarisozlesme` tablosunda `input`  degeri `ad` veya `kod` alanlari arasindan arama yapilir. `kod` alanina gore siralanarak listelenir.
- `input` degeri gonderilmezse databaseden `1000` data seklinde donus yapar.
- Ornek Request:
```
sgmTicariSozlesmes (input: "S"){
	kod
	ad
}
```