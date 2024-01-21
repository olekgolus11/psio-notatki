# Powtórka do egzaminu
- [[Filtracje]]
- [[Normalizacja jasności]]
- [[Local binary patterns]]
- [[Sąsiedztwo]]
- [[Deskryptory kształtu]]
- [[Segmentacje]]
- [[Operacje morfologiczne]]

# Operacje morfologiczne (dorobić)

# Filtracje i zakłócenia
## Filtr Gaussa
Na szum gausa
## Filtr medioanowy
Na sól i pieprz
## Rozmycie

# Krawędzie
## Maski gradientowe
### Sobel
### Roberts 
### Prewitt
## Detekcja krawędzi
### Laplasjan
### Canny
### LoG

# Zadania
## Zadania z deskryptorów
### Zad 1
![](https://i.imgur.com/blIamsb.png)
1. Eliminujemy obiekty z liczbą eulera różną od $1$.
2. Eliminujemy obiekty z cylkularnością mniejszą od $0.8$
### Zad 2
![](https://i.imgur.com/K70HuFx.png)
1. Dzielimy wg liczby eulera, kolejno: $1, -1, -3$

### Zad 3

![](https://i.imgur.com/OhMvIJo.png)
1. Dzielimy wg liczby eulera, kolejno: $1, 0, -4, -1$

## Zadanka z segmentacji
### Zad 1
![](https://i.imgur.com/pnrvjIq.png)
1. Mean-shift
2. Algorytm szwaba
3. Rozrost / random walker
4. Progowanie adaptacyjne
5. k-średnie

### Zad 2
![](https://i.imgur.com/6logkjj.png)
1. Progowanie adaptacyjne
2. Progowanie wielopoziomowe
3. Balon
4. Progowanie wielopoziomowe
5. Algorytm szwaba

### Zad 3

![](https://i.imgur.com/If0E44G.png)
1. Szwab
2. Klasteryzacja
3. Markery
4. Balon
5. Progowanie wielopoziomowe

### Zad 4

![](https://i.imgur.com/eHOqS9H.png)

1. Mean shift
2. Random walker
3. Metoda krawędziowa
4. Klasteryzacja

### Zad 5

![](https://i.imgur.com/tm8Tqru.png)
1. Wąż
2. Podział i łączenie obszarów
3. Balon
4. Random walker

### Zad 6
![](https://i.imgur.com/HhPdqz2.png)
1. Progowanie adaptacyjne
2. Rozrost obszaru
3. Balon / rozrost
4. Markery
5. Podział i łączenie obszarów

## Zadanka z operacji morfologicznych

### Zad 1

![](https://i.imgur.com/gXRXqAI.png)
1. White top hat
2. Zamykanie
3. Black top hat

### Zad 2

![](https://i.imgur.com/fgN5dD6.png)

1. Otwarcie
2. Zamknięcie
3. Erozja

### Zad 3

![](https://i.imgur.com/qTuOaxc.png)

1. Oryginał
2. Erozja
3. Gradient morfologiczny

### Zad 4
![](https://i.imgur.com/n6pttJA.png)
1. Orginał
2. Szkielet
3. White top hat
4. Gradient morfologiczny

## Zadanka z krawędzi
### Zad 1
![](https://i.imgur.com/6vrC2Qh.png)
1. Krawędź to zmiana jasności obrazu
2. Sobel Gy

#psio #it 