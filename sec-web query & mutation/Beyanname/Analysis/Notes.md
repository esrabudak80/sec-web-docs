m- Kur Tarihi: 
- Kullanici: 
- 4 Belgeleri: 
- Referans No: 
```
findNextReferansNo (departmanid: "")
```
- Ödeme Şekli:

Gonderici Tiklandiginda
- Ek Belge ve Izinler: 
```
sbrFirmasByFilterBasic (input: {
searchText: "DCS",
firmaType: gumrukmusteri
}) {
vekaletnameno
vekaletbastar
statubelgeno
statutarih
yysfirmasi
oksbfirmasi
}
```

ornek gosterim: 
```
VEKALET:${vekaletnameno};${vekaletbastar} YYS:${statubelgeno};${statutarih}
```

- Sevk Ulkesi, Ticaret Yapilan Ulke, Gidecegi Ulke, Cikis Ulkesi asagidaki query ile dolar.
```
sbrFirmasByFilterBasic (input: {
searchText: "ATMACA",
firmaType: gumrukmusteri
}) {
sbrUlke{
edikod
ad
}}
```
- Uyari Pop-up:
```
sbrFirmasByFilterBasic (input: {
searchText: "ATMACA",
firmaType: gumrukmusteri
}) {
uyar
aciklama
}
```

Gonderilen Gumruk Secildiginde

```
SbrGumruk (id: "") {
ad
edikod
}
```
