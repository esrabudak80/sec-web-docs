- `sgm_antrepo` tablosunda `input`  degeri `ad` veya `kod` alanlari arasindan arama yapilir. `ad` alanina gore siralanarak listelenir.
- `input` degeri gonderilmezse databaseden `500` data seklinde donus yapar.
- Ornek Request:
```
sgmAntrepos (input: "S"){
	kod
	ad
}
```