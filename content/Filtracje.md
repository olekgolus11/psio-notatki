# Filtracje

- [[#Filtracja zwykła]]
- [[#Filtracja medianowa]]
- [[#Filtracja uśredniająca]]
- [[#Filtr Gaussa]]
- [[#Wyostrzenie]]
- [[#Filtr maksymalny i minimalny]]
- [[#Zadania]]

## Filtracja zwykła

Mamy jedną macierz wejściową oraz jedną macierz filtracyjną. Z macierzy wejściowej wyciągamy podmacierze wielkości filtracyjnej, i mnożymy elementy przez siebie, które następnie sumujemy.

## Filtracja medianowa

Bierzemy podmacierz o jeden rozmiar mniejszą, i z liczb które się w tej macierzy zawierają wyciągamy medianę, którą wpisujemy w macierz wynikową w taki sam sposób jak w filtracji zwykłej.

![](https://i.imgur.com/ovDYar7.png)

## Filtracja uśredniająca

Działa w podobny sposób co medianowa, tylko zamiast mediany bierzemy średnią.

W przypadku np. zaszumionego obrazu [[#Filtracja medianowa]] działa dużo lepiej bo wybiera najlepszy pixel, zamiast sumować go z szumem

![](https://i.imgur.com/sMFS10L.png)

## Histogram zwykły

Nie wymaga większego tłumaczenia, zapisujemy ilość powtórzeń danej wartości

![](https://i.imgur.com/3IRBYKM.png)

## Histogram skumulowany

Coś jak z dystrybuantą, tzn. lecimy od najmniejszych wartości do największych, gdzie dla wartości większych dodajemy ilość wartości mniejszych przed nimi

![](https://i.imgur.com/6drZlVS.png)

## Filtr Gaussa

Po prostu rozmycie

![](https://i.imgur.com/8bwXr6z.png)

## Wyostrzenie

Aby uzyskać wyostrzenie, należy najpierw wydobyć detale, a potem je dodać do obrazu:
$$detale=obraz\ oryginalny-filtracja\ uśredniająca$$
$$wyostrzenie=obraz\ oryginalny+k\cdot detale$$

![](https://i.imgur.com/KjRbAaC.png)

## Filtr maksymalny i minimalny

Na podstawie elementu strukturyzującego wybierana jest albo minimalna wartość albo maksymalna.

![](https://i.imgur.com/97YqgY6.png)

## Zadania

![](https://i.imgur.com/lZHOT1m.png)
![](https://i.imgur.com/diyBwUC.png)
![](https://i.imgur.com/1L9q8dI.png)
![](https://i.imgur.com/ZsnmHKH.png)
![](https://i.imgur.com/TzQqqkJ.png)

#psio #it
