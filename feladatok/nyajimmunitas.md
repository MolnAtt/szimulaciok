# Nyájimmunitás
## Röviden
A feladat a vírus terjedésének és a nyájimmunitás kialakulásának szimulációja lesz.

## Fogalmak
- Immunitás: Ha egy betegségből felgyógyul egy ágens, akkor egy ideig immunis lesz a vírusra, azaz egy ideig nem fogja tudni azt újra elkapni. Ebben a szimulációban feltesszük, hogy ez idő alatt továbbadni sem tudja a vírust.
- Nyájimmunitás: Egy közösségben nyájimmunitás alakul ki akkor, ha elegendően sokan kapták el a vírust ahhoz, hogy az így kialakuló immunitással bíró egyéneken fennakadjon a vírus, azaz az immunitással nem rendelkező, fertőzésnek kitett embereket ne érhesse el vagy ne érinthesse nagy mértékben a vírus. (Ilyen módon a vírus egy idő után akár ki is halhat.) 

## Részletesen
Adott egy képernyő, amin kis korongok (ágensek) vándorolnak. Ha a széléhez érnek, visszapattanhatnak, de ki is jöhetnek a túloldalon (toroid-univerzum), igazából mindegy. Az sem fontos most, hogy a korongok átmennek egymáson vagy elpattannak egymásról. A korongok három színnel rendelkezhetnek:
- lehetnek **egészségesek**,
- lehetnek **fertőzöttek** és ezáltal egyben betegek,
- lehetnek **immunisak**, azaz átestek már a fertőzésen.

## Paraméterek:
- ``a``: ágensek száma
- ``p``: a fertőzés valószínűsége, 0 és 100 közötti százelékérték
- ``t``: gyógyulás ideje
- ``i``: gyógyulás után kialakuló immunitás mennyi ideig tart.

## Működés
Ha egy fertőzött ágens közel kerül egy egészségeshez, akkor ``p`` valószínűséggel fennáll a fertőzés veszélye. 
Az ágensek a fertőzés után ``t`` idő felépülési idő után ``i`` ideig immunisak lesznek a fertőzésre. 

## Vizsgálat tárgya:
A paraméterek milyen beállítása esetén valószínűbb/gyorsabb a nyájimmunitás kialakulása?

## Megjegyzés: 
Valószínűleg nagy jelentősége van a szimulációban annak, hogy a korongok lepattannak-e egymásról vagy sem: ha nem, akkor a fertőzött ágensek akadály nélkül fertőzhetnek végig mindent. Így biztosan nehezebb lesz a nyájimmunitást elérni.

## Fejlesztési lehetőségek:
- **Oltás:** Határozott időközönként egy adott számú (esetleg egy régióba eső) ágens fertőzöttségi állapot nélkül hosszabb időtartamra immunitást nyer.
- **Tesztelés:** Határozott időközönként egy adott számú (esetleg egy régióba eső) ágenst megvizsgál a program, hogy fertőzött-e. Ha igen, akkor őket karanténba zárja (lásd: karantén).
- **Karantén:** A fertőződés után valamekkora valószínűséggel felfigyel az állam a fertőzésre és karanténba zárja az illetőt. A karanténba került egyén nem mozog tovább, és nem adja tovább a fertőzést, amíg fel nem gyógyul.
- **Kijárási korlátozások:** Az ágensek egy részének a mozgását időszakosan leállítja.