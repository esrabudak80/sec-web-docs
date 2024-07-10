**Musavir Kontrol Pop-Up icin:**

- MT Oncelik_:_
    

```
  enum SgmBeyannameMusKontrolOncelikEnum {
    N
    A
    G
  }
```

- Kontrol amaci sabit.
    
- Kontrol Eden drop-down:
    
    ```
    skyGrupKullanicisByGrupKod (grupkod: "MUSAVIR")  {
         kullanicikod
         grupkod
       }
    ```
    
    -----------------------------------------------------------------------------------------
    
- **Mutation:**
    
    ```
    createSgmBeyannameMusKontrolForm (beyannameid: "" ,input: {
            kontroldenalan: ""
            oncelik: A
            kontrolamaci: ""
            kontrolegonderennot : ""
        }) {
            kontrolamaci
            oncelik
            kontrolegonderennot
            kontroldenalan
        }
    ```
    