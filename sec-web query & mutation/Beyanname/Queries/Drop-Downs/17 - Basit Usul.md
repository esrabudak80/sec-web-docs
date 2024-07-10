- `sgm_basitusul` tablosunda `input`  degeri `ad` veya `kod` alanlari arasindan arama yapilir. `ad` alanina gore siralanarak listelenir.
- `input` degeri gonderilmezse databaseden `1000` data seklinde donus yapar.
- Ornek Request:
```
sgmBasitUsuls (input: "S"){
	kod
	ad
}
```