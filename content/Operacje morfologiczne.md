# Operacje morfologiczne
Przekształcają tylko tą część pikseli obrazu, których otoczenie jest zgodne z pewnym wzorcem.

Operacje te są dwuargumentowe, przyjmują **obraz** oraz **element strukturyzujący**. Element ten jest taką jakby maską, którą jeździmy po każdym pikselu obrazu i analizujemy dzięki niemu sąsiadów, w taki sposób, jaki kształt ten element posiada.

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



#psio #it 