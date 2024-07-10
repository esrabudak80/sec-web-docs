- `sgmIsTakipViewExcelExport(columns: [String] filter: PagedQueryInput): String @requireAuth` querysinden Is takip Beyanname sayfasindan excel ciktisi olusturur.
- `columns` ve `filter` olarak iki parametre alir.
- `columns` parametresi istenen excelde gosterilmek istenen columnlardir. `extractColumnsFromJson` fonksiyonunda `columns` ve `jsonData(dbden gelen datalar)` karsilastirilarak eleme yapilir.
- `filter: PagedQueryInput` tipindedir. 
```
input PagedQueryInput {
filter: [FilterCriteria]!
order: [OrderInput]
pageNo: Int = 1
pageSize: Int = 10
}
```

- Ornek request:
```
"sgmIsTakipViewExcelExport": {
    "columns": ["ad", "ozelkod"],
    "filter": {
      "pageSize": 50,
      "filter": [
        {
          "fieldName": "ad",
          "condition": "contains"
        }
      ]
    }
}
```