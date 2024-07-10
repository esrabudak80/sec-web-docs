- `createSgmKalem` ile yeni kalem olusturulur.
- `sgm_kalem` ile beraber ``sgm_tesvikcikis``, ``sgm_kalemacmakapama``, ``sgm_kalemdiib``, ``sgm_kalemesyagerigelmesebebi``, ``sgm_kalemekbelge``, ``sgm_kalemvergi``, ``sgm_kalemkonteyner``, ``sgm_kalemodemesekli``, ``sgm_kalemmarka``, ``sgm_kalemdetay`` tablolarina array tipinde kayit atar.
- Eksik tablolar: `sgm_kalemdiibdusum`, `sgm_kalemdiibdusumoranlama` analizi tamamlandiktan sonra ek gelistirme olarak devam edilecek.
- Ornek request
```
mutation CreateSgmKalem {
  createSgmKalem(input: {
    beyannameid: "5C373C0B-C510-47C2-8E74-D5D437BB9616",
    edisirano: 8,
    gtip: "8714.91.90.00.00",
    sirano: 44874.411283078705,
    teslimsekli: "FOB",
    ticaritanim: "CATAL YATAGI",
    menseulke: "736",
    rejim: "7100",
    kapadet: 1,
    ozellik: "01",
    kapcinsi: "KN",
    faturatutari: 332.28,
    faturatutaritl: 6162.066143999999,
    fobtutar: 332.28000000000003,
    istatistikikiymet: 346.2,
    burutagirlik: 17.3,
    netagirlik: 16.18,
    birimi: "SET",
    miktari: 130.0,
    olcumiktari: 130.0,
    olcubirimi: "SET",
    muafiyet1: "",
    kalemislemniteligi: "",
    giriscikisamaci: "",
    giriscikisamaciaciklama: "",
    kapkonteynerno: "TLLU8163309",
    sgmKalemdiib: [
      {
        diibbelgeno: "22102821064"
      }
    ],
    sgmKalemEsyaGeriGelmeSebebi: [
      {
        esyagerigelmesebebikod: 0,
        aciklama: "value2"
      }
    ],
    sgmKalemEkBelge: [
      {
        grupkodu: "1",
        ekbelgekodu: "3502",
        dogrulama: "F",
        referans: "REF1244",
        belgetamamlamatarihi: "2023-12-01T00:00:00Z",
        arsivid: "00000000-0000-0000-0000-000000000000",
        belgedosyaad: "dosya.pdf",
        vizetarihi: "2024-01-01T00:00:00Z"
      }
    ],
    sgmKalemVergi: [
      {
        kodu: "10",
        tutari: 500.75,
        orani: "18%",
        odemesekli: "P",
        carpilan: "Evet",
        gumrukteodeme: "Hayır",
        islemtipi: "KDV",
        matrah: 4500.00
      }
    ],
    sgmKalemKonteyner: [
      {
        kapkonteynerno: "TEMU1092078",
        konteynerulke: "999",
        konteynertipi: 2,
        limancikistarih: "2023-12-01T00:00:00Z"
      }
    ],
    sgmKalemOdemeSekli: [
      {
        odemeseklikodu: "1",
        odemetutari: 250.75,
        tbfid: "TBF123456"
      }
    ],
    sgmKalemDetay: [
      {
        beyannameid: "5C373C0B-C510-47C2-8E74-D5D437BB9616",
        esyatanimid: "00000000-0000-0000-0000-000000000000",
        gc: "G",
        kap: 10,
        miktar: 100,
        brutkg: 150.0,
        netkg: 140.0,
        tutar: 10000.50,
        dovizcinsi: "USD",
        aciklama: "Örnek açıklama",
        faturano: "FAT123456",
        faturatarih: "2023-12-01T00:00:00Z",
        bolen: "Bolen123",
        musrefno1: "MusrefNo1",
        musrefno2: "MusrefNo2",
        tutar2: 9500.00,
        antrepobeyannameno: "ANT123456",
        antrepokalemsirano: 1,
        worawid: "00000000-0000-0000-0000-000000000000",
        masterid: "00000000-0000-0000-0000-000000000000",
        deliveryno: "ABC",
        menseulke: "TR",
        yatirimtesvikbelgeno: "YAT123456",
        yatirimtesviktarihi: "2023-11-01T00:00:00Z",
        cikisulkeliman: "Cikis",
        gondericireferans: "GondericiRef123",
        konsimantono: "KonsimantoNo123",
        konteynernumara: "CONT123456",
        gemiadi: "Gemimizin Adı",
        tasiyicikodu: "123",
        bosaltmalimani: "BosaltmaLimani123",
        ilaveedilecekkiymet: 500.00,
        entegrasyonno: "EntegrasyonNo123"
      }
    ],
    sgmKalemMarka: [
      {
        markaturu: "A",
        markatescilno: "TESCIL123",
        markaadi: "Marka Adı",
        markakiymeti: 25000.00,
        referansno: "REF123456",
        modelyili: "2023",
        model: "Model 123",
        motorhacmi: "2000cc",
        silindiradedi: 4,
        renk: "Siyah",
        motorgucu: 150,
        motortipi: "A",
        vites: "A",
        motorno: "MOTOR123",
        imeino: "IMEI123456789"
      }
    ],
    sgmKalemAcmaKapama: [
      {
        beyannameno: "Beyan123456",
        kalemsirano: 1,
        miktar: 100.5,
        cikiskapadet: 10,
        aciklama: "Örnek açıklama"
      }
    ],
    sgmTesvikCikis: [
      {
        tesvikgirisid: "77A9BAF0-7ADF-4D38-9DB3-D81EFE844860",
        kalemsirano: 1,
        miktar: 100.5,
        miktarkg: 99.5,
        tutar: 1000.0,
        aciklama: "Örnek açıklama",
        kalemacmakapamaid: "123e4567-e89b-12d3-a456-426614174002",
        birimfiyat: 10.0,
        dovizkur: 8.5,
        vergioran: 18.0,
        exfaturano: "FAT123456",
        forma: "FormA",
        kontroledildi: "A",
        raporno: "RAP123456",
        raportarih: "2023-12-01T00:00:00Z",
        raporkg: 98.0,
        brutkg: 150.0,
        fobtutar: 900.0,
        iptaledildi: false,
        tesciledildi: true
      }
    ]
  }) {
    id
  }
}

```