# Bitcoin trader

Eesmärk oleks ehitada finantsvabadust võimaldav programm, mis teeb meie eest automaatseid väärtpaberi tehnguid ja teenib sellega vaheltkasu.  
Kasutame programmis algoritmilist valuutat Bitcoin (mida kontrollib arvutiprogramm) ning [fiat-valuutat](https://et.wikipedia.org/wiki/Fiat-raha) USD (mida kontrollib USA keskpank)

Hoiatus! Tegemist ei ole investeerimissoovitusega. Antud harjutus on õppimise eesmärgiga. Päris fintantsvaradega ümber käimisel kaasneb risk kaotada oma raha ning vajab pikemat kogemust, et turvaliselt investeerida.  
Selles harjutuses olev kauplemisalgoritm on väga algeline ja spekulatiivne - see eeldab, et hind püsib pikalt samas vahemikus. Peaksid arvestama, et inflatsiooni mõjul fiat-valuutad kaotavad oma väärtust/ostuvõimet.

### See programm tuleks ehitada kolmes osas:
1. Teeme raamatupidamise jaoks enda rahakoti mudeli ehk muutujad, kus on kirjas palju meil on Bitcoini ja palju on dollareid.
2. Kirjutame kauplemise funktsioonid `buy` ja `sell`, mis uuendavad meie rahakoti muutujaid vastavalt hinnale
3. Testime, kas `buy` ja `sell` töötavad
4. Kirjutame kauplemisalgormitmi ehk valemi, mille järgi iga sekund osta või müüa
5. Võtame praeguse Bitcoini hinna US dollarites CoinGecko API kaudu.

#### 1. & 2. Raamatupidamise ja kauplemise funktsioonide mõte
Meil on vaja teada, kui palju meil on erinevaid valuutasid. Seda on vaja teada kauplemiseks, kuna programm peab aru saama millal enam osta või müüa enam ei saa, sest raha on otsas.  
TODO joonis

#### 3. Kuidas kontrollida kas hakkas kauplemise funktsioonid hakkasid tööle
TODO

#### 4. Algeline kauplemisalgoritm
Kauplemise algoritmi eesmärk oleks vältida kahjumisse jäämist. Üks tehnika oleks oletada mingi keskmine, millest hind hakkab üles alla kõikuma.
- määrame selle nädala oodatud keskmise hinna
- vahetame meie Bitcoini kellegi teise dollarite vastu, kui Bitcoini hind dollarites on oodatust keskmisest kallim (müü/sell)
- vahetame meie dollareid kellegi teise Bitcoini vastu, kui Bitcoini hind dollarites on oodatust keskmisest odavam (osta/buy)

#### 5. Bitcoini hind API kaudu
TODO

### Hindamine
+1 hinne iga ülesande eest (raamatupidamine, kauplemise funktsioonid, kauplemise algoritm, Bitcoini hind läbi API)  
-1 hinne kui tunnis ei jõua esitada (sobib, kui Githubi jõuad üles laadida õige ajal aga näitad järgmine tund)

### Mis oskusi see ülesanne treenib
- Matemaatilised valemid programmeermiskeeles
- Funktsionaalne lugemine
- Ühiskonnaõpetus ja rahatarkus
- Võrgurakendused (HTTP API)
