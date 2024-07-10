- `sgmBelgeIsleme` ucuna id gonderilerek ilgili alanlar cekilir.
```
sgmBelgeIsleme(id: "2F276E43-6F58-4640-8373-01CB30BAF356") {
	musteriid
	belgeturu
	geldigiyer
	geldigitarihsaat
	belgeilgili
}
```
### Musteri drop-down: 
- `sgmBelgeIsleme` tarafindan dondurulen `musteriid`, `sbrFirmasByFilterBasic` tarafindan dondurulen `id` ile eşleştirilir.
```
sbrFirmasByFilterBasic(input: {
	searchText: "LE"
	firmaType: gumrukmusteri
}){
	ad
}
```

- `sbrFirmasByFilterBasic`, `FirmaWhereInput` tipinde bir parametre olan `input` bekler. 
```
input FirmaWhereInput {
	searchText: String # search in ad, ozelkod
	firmaType: [FirmaEnum!]
}
```
- `searchText` ad ve ozelkod'da arama yapar
-  `firmaType` `FirmaEnum` tipindedir ve asagidaki degerlere sahiptir: 
```
enum FirmaEnum {
gumrukgonderici
gumrukalici
gumrukmusteri
nakliyeci
imalatci
sorumlu
kuryefirma
faturadresi
}
```

- Taskta musteri firma bilgilerine ihtiyac duydugumuz icin `firmaType` olarak `gumrukmusteri` degeri gonderilir.

### Ilgilisi drop-down: 
- `sgmBelgeIsleme` den donen `belgeilgili`, `skyKullanicis` dan donen `kod` ile eslenir.
```
skyKullanicis{
	kod
}
```