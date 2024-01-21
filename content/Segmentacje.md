# Segmentacje
Segmentacje obrazów, tj. oddzielenie obiektów od tła, bądź od innych obiektów, możemy podzielić na takie grupy:
1. Metody punktowe
	1. [[#Progowanie]]
	2. [[#Klasteryzacja]]
2. Metody krawędziowe
	1. [[#Metody oparte o pochodne obrazu]]
	2. [[#Metoda działów wodnych]]
3. Metody obszarowe
	1. [[#Rozrost obszaru]]
	2. [[#Podział obszaru]]
	3. [[#Metody hybrydowe]]
4. Metody modeli deformowalnych
	1. [[#Metody parametryczne]]
	2. [[#Metody geometryczne]]
5. Metody grafowe
	1. [[#Algorytm Felzenszwalba i Huttenlochera (FiH)]]
	2. [[#Metoda min przekroju / max przepływu]]
	3. [[#Metoda znormalizowanego]]
	4. [[#Metody najkrótszej ścieżki]]
	5. [[#Metoda błądzenia losowego]]

- [[#Zadanka]]

## Progowanie
Wydzielenie obszarów wg ich koloru/jasności
### Progowanie wielopoziomowe
Jest to podzielenie wg. danych progów wartości pikseli na różne kolory należące do danego przedziału

![](https://i.imgur.com/6VgkGp3.png)
![](https://i.imgur.com/1xHPGPg.png)
![](https://i.imgur.com/5XnZuJI.png)

### Progowanie adaptacyjne
Nie działa bezwzględnie na całym obszarze jak tak wielopoziomowe, tylko adaptuje się do mniejszych rozmiarów, bądź nawet każdego piksela indywidualnie 

![](https://i.imgur.com/FBhNZNq.png)

## Klasteryzacja
Podzielenie na obszary wg przestrzeni jakichś cech
### Metoda k - średnich
No tak w skrócie to wybierane są piksele o podobnej cesze (tutaj kolor) i przypisywane są na tej bazie do swojego centroida (tzn. po prostu do jakieś grupy koloru).

Tu widać dla k=3 że żółte plamki są cechowo blisko do koloru królika, natomiast dla k=5 podobieństwo było już za małe i się te grupy rozdzieliły.

![](https://i.imgur.com/MbLgKHw.png)

### Superpiksele
Tutaj w porównaniu do metody k-średnich istotne jest również położenie piksela, przez to jeśli dane piksele są identyczne z koloru ale po dwóch stronach obrazu to nie będą w tej samej grupie.

![](https://i.imgur.com/CVj8DnS.png)
![](https://i.imgur.com/mraVmWh.png)

### Mean-shift
Podobnie do k-means wymaga podobnego koloru, oraz podobnie do superpikseli wymaga położenia, ale robi to bardziej dynamicznie i "rozlewa" się po całym kolorze. Charakterystycznie wygląda, jak malowany

![](https://i.imgur.com/eYquVx2.png)

## Metody oparte o pochodne obrazu

![](https://i.imgur.com/3AhSlqi.png)

## Metoda działów wodnych
![](https://i.imgur.com/FnV1Djb.png)
![](https://i.imgur.com/P7uHYHD.png)

## Rozrost obszaru
Wybrany punkt na obszarze stopniowo się powiększa, w zależności od tego czy sąsiad spełnia pewną określoną cechę podobieństwa.

![](https://i.imgur.com/NfZ3C93.png)
![](https://i.imgur.com/4OW5jjf.png)

## Podział obszaru
Stopniowo, rekurencyjnie dzieli obraz wejściowy na podregiony, dopóki dany obszar nie jest uznany za jednorodny względem danego kryterium

![](https://i.imgur.com/oiU81ou.png)

## Metody hybrydowe

### Podział i łączenie obszarów
Najpierw dzielimy obszar na jednolite podobszar, a następnie łączymy je ze sobą na podstawie jakiegoś tam określonego kryterium

![](https://i.imgur.com/jnTI6VK.png)

Tutaj przykład z podziałem obrazu wg [[#Metoda działów wodnych]]

![](https://i.imgur.com/SQIWiF3.png)
![](https://i.imgur.com/cMlMQBD.png)


Tutaj przykład z podziałem wg [[#Superpiksele]]

![](https://i.imgur.com/Q9vRdQH.png)
![](https://i.imgur.com/PHjBvet.png)

## Metody parametryczne
### Model typu wąż
Zaznaczamy dany obszar, a nasze punkty doklejają się do krawędzi

![](https://i.imgur.com/xtZWkXB.png)
![](https://i.imgur.com/a1IrEBB.png)

### Model typu balon
Jest to rozwinięcie modelu węża, tylko tyle ze nie jest ograniczony przez skończoną liczbę punktów, co przekłada się na to że może przeniknąć przez nieciągłą krawędź i "wyskoczyć" na zewnątrz.

![](https://i.imgur.com/VZs36zN.png)
![](https://i.imgur.com/Vqlbjek.png)

## Metody geometryczne
### Geodezyjny aktywny kontur typu level-set
Ideą to zrzutowanie przekroju przestrzeni 3D na płaszczyznę
![](https://i.imgur.com/79oLnlu.png)

Można sobie wyobrazić ze ciemne piksele to dół a jasne to góra (ja to tak rozumiem)

![](https://i.imgur.com/pL0ewzg.png)

## Algorytm Felzenszwalba i Huttenlochera (FiH)
Zakładamy minimalne drzewo rozpinające na wszystkie podobne obszary na obrazie, i każdy obszar kolorujemy jakoś randomowo

![](https://i.imgur.com/Gw1HQgh.png)

## Metoda min przekroju / max przepływu
Wymaga wskazania pikseli źródłowych dla tła i dla obiektu
![](https://i.imgur.com/IAcwfLm.png)
![](https://i.imgur.com/PootUeX.png)
![](https://i.imgur.com/k75nOgl.png)

## Metoda znormalizowanego
Dzieli na wskazaną ilość obszarów

![](https://i.imgur.com/hauVqsk.png)

## Metody najkrótszej ścieżki
![](https://i.imgur.com/kMwtHJX.png)

## Metoda błądzenia losowego
Metoda podążająca wzdłuż krawędzi, jest odporna na dziury i słabe krawędzie
![](https://i.imgur.com/1Gc13WQ.png)

## Zadanka
![](https://i.imgur.com/MbEJNMO.png)
![](https://i.imgur.com/qaj8y6r.png)
![](https://i.imgur.com/kjMgonM.png)
![](https://i.imgur.com/9zeUvku.png)
![](https://i.imgur.com/Y24MKN6.png)
![](https://i.imgur.com/f0HgWyH.png)



#psio #it 