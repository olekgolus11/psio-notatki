# Detekcja krawędzi
Krawędź to nic innego jak gwałtowna zmiana poziomu jasności obrazu. Może być stopniowa, gładka, ostra itp.

![](https://i.imgur.com/JSLEtUE.png)

Krawędzie dobrze są widoczne po analizie pochodnych:

![](https://i.imgur.com/lrQUuvM.png)

No i takie pochodne są wykorzystywane w maskach gradientowych (było kiedyś na analizie matematycznej - gradienty to są takie wektory, które trzymają informacje o kierunku i stopniu pochyłu).

## Maski gradientowe
Wyróżniamy trzy maski gradientowe:
- [[#Maski Prewitta]]
- [[#Maski Sobela]]
- [[#Maski Robertsa]]

![](https://i.imgur.com/qG3V9aY.png)


### Maski Prewitta
![](https://i.imgur.com/aNzGm3R.png)

### Maski Sobela
![](https://i.imgur.com/Ke6Z9Lv.png)
![](https://i.imgur.com/Qji7jig.png)

### Maski Robertsa
![](https://i.imgur.com/M5cRzHG.png)

## Laplasjany
Nie wiem, są sobie, chyba działają podobnie co maski gradientowe, tylko wykorzystują pochodne drugiego rzędu

![](https://i.imgur.com/Xtq3sDg.png)

### Laplasjan filtru Gaussa
Generalnie im bardziej rozmyjemy obraz tym mniej krawędzi na nim będzie.

![](https://i.imgur.com/KHZBJpS.png)

## Metoda Canny
Tu w jakiś sposób wykorzystywana jest pochodna filtru Gaussa i złączanie krawędzi na jakiejś tam podstawie dziwnej

![](https://i.imgur.com/CXBo1D4.png)
![](https://i.imgur.com/DV9ZW9T.png)

Tutaj jeszcze porównanie z Sobelem, widać duże różnice pomiędzy wszystkimi trzeba metodami:

![](https://i.imgur.com/lkeIQJn.png)

Czyli:
- LoG (laplasjan filtru gaussa) bardzo zakrzywia krawędzie, wygląda jakby było rysowane pisakiem przez dzieciaka
- Canny wygląda jakby ktoś strzelił potężny threshold na krawędzie
- A Sobel jakby próbował narysować coś białym ołówkiem

## Filtr wariacyjny
Nie wiem czym się charakteryzuje bo nie jest opisany

![](https://i.imgur.com/Gscsx1c.png)



#psio #it 