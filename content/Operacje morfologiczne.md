# Operacje morfologiczne
Przekształcają tylko tą część pikseli obrazu, których otoczenie jest zgodne z pewnym wzorcem.

Operacje te są dwuargumentowe, przyjmują **obraz** oraz **element strukturyzujący**. Element ten jest taką jakby maską, którą jeździmy po każdym pikselu obrazu i analizujemy dzięki niemu sąsiadów, w taki sposób, jaki kształt ten element posiada.

- [[#Erozja]]
- [[#Dylacja]]
- [[#Otwarcie]]
- [[#Zamknięcie]]
- [[#Hit-or-miss (i guess they never miss huh)]]
- [[#Kontur]]
- [[#Gradient morfologiczny]]
- [[#White top-hat]]
- [[#Black top-hat]]
- [[#Zamykanie (wypełnianie)]]
- [[#Połączone kompontenty]]
- [[#Otoczka wypukła]]
- [[#Pocienianie]]
- [[#Szkielet]]
- [[#Obcinanie]]
- [[#Pogrubianie]]
- [[#Transformata odległościowa]]

No i zadanka:
- [[#Zadanka]]
## Erozja
Polega na usunięciu wszystkich białych pikseli, które sąsiadują z choć jednym czarnym pikselem (analogia do zaznaczenia maski w gimpie i zmniejszenia zaznaczania).

![](https://i.imgur.com/gb6WEg5.png)
![](https://i.imgur.com/YwNM9oK.png)

## Dylacja
Jest odwrotnością erozji, zamieniamy wszystkie czarne piksele na białe jeśli sąsiadują z białym pikselem (analogia do zaznaczenia obszaru i powiększenia zaznaczenia)

![](https://i.imgur.com/n9JB2q5.png)
![](https://i.imgur.com/BNy50V5.png)

## Otwarcie
Jest niczym innym jak: najpierw erozja a potem dylacja.

Jak zapamiętać kolejność? Otwieramy, czyli erodujemy by otworzyły się dziury, a potem wracamy do oryginalnych rozmiarów w wyniku dylacji. 

![](https://i.imgur.com/u63zfEw.png)
![](https://i.imgur.com/s0OThKl.png)

## Zamknięcie
Jest odwrotnością procesu otwarcia - czyli najpierw dylacja a potem erozja.

Jak zapamiętać kolejność? Zamykamy, czyli pogrubiamy wszystko by zamknęły się dziury, a potem wracamy do oryginalnych rozmiarów w wyniku erozji.

![](https://i.imgur.com/FIc1d70.png)
![](https://i.imgur.com/ZC6V8hK.png)

## Hit-or-miss (i guess they never miss huh)
Wykorzystuje dwa elementy strukturyzujące takie, gdzie pierwszy element pasuje do badanego obiektu, a drugi kompletnie nie. Oprócz tego wykorzystuje się tutaj erozję.

W tym przykładzie chodzi o to, że pierwszy element strukturyzujący ($B_{1}$) to zbiór kropek 3x3 (nie ma tego tutaj pokazanego), a $B_{2}$ to otoczka tego elementu pierwszego.

Szukamy więc najpierw wszystkich pasujących kształtów (tu znajdziemy dwa), a potem szukamy wszystkich pasujących otoczek (też znajdziemy dwa, ale nie o tych samych punktach centralnych). 

Następnie porównujemy znalezione punkty ze sobą i bierzemy te wspólne (tutaj wyjdzie nam tylko jeden taki punkt)


![](https://i.imgur.com/QSIcSgB.png)

Tutaj mamy 4 maski $B_{1}$ (to są te jedynki), oraz 4 maski $B_{2}$ (to są zera).
Zauważ, że by znaleźć róg, róg ten musi mieć białe piksele (1) w kształcie L, a otaczać go z zewnątrz muszą czarne piksele (0).

![](https://i.imgur.com/gZBY5Op.png)

## Kontur
Konturem nazywamy dokładnie to:
$$Kontur=obraz\ oryginalny-wynik\ erozji$$
![](https://i.imgur.com/TyXp73G.png)

## Gradient morfologiczny
Jest to taki dopakowany kontur bo:

$$Gradient\ morfologiczny=wynik\ dylacji-wynik\ erozji$$

Czyli zamiast obrazu oryginalnego wykorzystujemy wynik dylacji (naturalnie taki gradient dla tego samego SE, czyli elementu strukturyzującego, jest dwa razy grubszy niż kontur)

![](https://i.imgur.com/RdodttH.png)

## White top-hat
Kiedy wykonujemy otwarcie, to usuwamy w ten sposób pewne części z obrazu. I to właśnie te części obrazuje white-top hat. Jest to nic innego jak różnica między oryginalnym obrazem a otwarciem na nim dokonanym.

Na lewo obraz oryginalny, a na prawo white-top hat. Wynikiem otwarcia byłyby tylko te wielkie białe koła.

![](https://i.imgur.com/GfRDQn7.png)
![](https://i.imgur.com/r6O78EL.png)
![](https://i.imgur.com/kgkUFHR.png)

## Black top-hat
Podobnie jak white-top hat obrazuje różnicę. Tylko w tym przypadku będzie to różnica, którą tworzy zamknięcie, a nie otwarcie.

![](https://i.imgur.com/4tlXMXI.png)

## Zamykanie (wypełnianie)
Nie mylić z zamknięciem. Trochę inny algorytm, słabo wyjaśniony, ale zamyka cały obiekt.

![](https://i.imgur.com/weWLqO0.png)

## Połączone kompontenty
Przypisanie każdej grupie pikseli jakiejś etykiety.

![](https://i.imgur.com/1MC8wmg.png)
![](https://i.imgur.com/ELxNr50.png)

## Otoczka wypukła
Wypełnia wklęśnięcia danego obszaru
![](https://i.imgur.com/NuArisU.png)
![](https://i.imgur.com/deNbB34.png)

## Pocienianie
Pocienianie działa podobnie do erozji, natomiast nie redukuje go całkowicie, a zmniejsza go do linii.

![](https://i.imgur.com/U2oQjkj.png)

## Szkielet
Jest to zbiór takich punktów, które są **równoodległe**  (nie równoległe bo można źle przeczytać xD) od co najmniej dwóch punktów należących do najbliższych brzegów.

Tu na obrazku dobrze to widać, każdy punkt czerwonej linii jest tak samo oddalony od jednego brzegu jak i od drugiego

![](https://i.imgur.com/YsLLqmQ.png)

## Obcinanie
Usuwa ze szkieletu niepotrzebne gałęzie zachowując topologię obrazu.

![](https://i.imgur.com/ifpbns9.png)

## Pogrubianie
Działa inaczej niż dylacja, bo mogłoby się wydawać że to to samo.

![](https://i.imgur.com/l8EiwlG.png)

## Transformata odległościowa
No taki blur. Każdy piksel przyjmuje nową wartość, która jest odległością do najbliższej krawędzi oryginalnego obiektu.

![](https://i.imgur.com/XY5JJjt.png)

## Zadanka
![](https://i.imgur.com/i6jOI9B.png)
![](https://i.imgur.com/E0ome7c.png)
![](https://i.imgur.com/aeKrp3z.png)
![](https://i.imgur.com/PkqSQd5.png)
![](https://i.imgur.com/Y6sve0B.jpg)
![](https://i.imgur.com/PzgFZ0N.png)


#psio #it  