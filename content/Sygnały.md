# Sygnały

- [[#Jak sygnał jest przetwarzany?]]
- [[#Transformacje sygnału dyskretnego]]
- [[#Dobra nie ma co się tego uczyć, tu jest w skrócie jak robić zadania]]
  - [[#Zadanie z bazą dyskretnej informacji]]
  - [[#Zadanie z wektorem N elementów]]
  - [[#Zadanie z jakimiś próbkami]]
  - [[#Zadanie z obliczaniem pliku dźwiękowego]]

## Jak sygnał jest przetwarzany?

1. Najpierw mamy sygnał fizyczny, może to być cokolwiek, np. fale dźwiękowe
2. **AKWIZYCJA**
3. W wyniku akwizycji otrzymujemy przetworzony sygnał fizyczny na sygnał w postaci napięcia, więc będziemy go mogli dalej przetworzyć
4. **KONWERSJA ANALOGO-CYFROWA** nasz sygnał analogowy przetwarzamy na cyfrowy
5. No i dalej robimy z nim co chcemy
   ![](https://i.imgur.com/nBWC7Eb.png)

### Warunek Nyquista

Aby poprawnie reprezentować sygnał, częstotliwość próbkowania musi być odpowiednio duża.

![](https://i.imgur.com/rgrEYL4.png)

## Transformacje sygnału dyskretnego

Celem transformacji jest dekompozycja próbek na funkcje bazowe - czyli takie, które w wyniku interferencji doprowadziły do właśnie tej funkcji którą analizujemy.

### Sformułowanie problemu

- Dane: wektor próbek $x=[x_{0},x_{1},x_{2},...,x_{n-1}]$
- Zbiór danych funkcji bazowych $B=[b^{0},b^{1},b^{2}...,b^{n-1}]$ (dane $b$ to wektor kolumnowy, trzyma on wartości wszystkich funkcji dla konkretnego $x$, będzie to widać niżej)
- Zbiór nieznanych współczynników $a=[a_0,a_1,a_2,...,a_{n-1}]$

Wynikiem dekompozycji jest przedstawienie próbek za pomocą kombinacji liniowej funkcji bazowych z odpowiednimi współcznynikami:

$$x=a_{0}\cdot b^{0}+a_{1}\cdot b^{1}+a_{2}\cdot b^{2}+...+a_{n-1}\cdot b^{n-1}$$

![](https://i.imgur.com/xrJVvWT.png)

Ten sam wektor próbek możemy zapisać w postaci takiej dyskretnej, zamiast funkcji trzymamy w tablicach odpowiednie dyskretne wartości:

![](https://i.imgur.com/MMFH0m4.png)

Z kolei tą możemy zapisać w postaci macierzy:

![](https://i.imgur.com/Qec0tiU.png)

## Dobra nie ma co się tego uczyć, tu jest w skrócie jak robić zadania

### Zadanie z bazą dyskretnej informacji

![](https://i.imgur.com/CThHKVl.png)

Dobra więc co robimy jak mamy zadanie z bazą jakąś z pizdy:

1. Ortogonalne to znaczy że ich iloczyn skalarny daje 0
2. Szukamy zatem jakiegoś wektora, który da iloczyn równy 0 z pierwszym i drugim
   - Niech będzie to $[-1,0,1]$ (wziąłem z dupy, trzeba sobie jakiś znaleźć), a ten akurat działa
3. Skoro mamy już bazę ortogonalną, to trzeba teraz skorzystać z tego zajebistego wektora, obliczamy więc współczynniki $a$:
   1. $a_{1}=<x,b^{1}>=[3,-2,1]\cdot[1,0,1]=3+0+1=4$
   2. $a_{2}=<x,b^{2}>=[3,-2,1]\cdot[0,1,0]=0-2+0=-2$
   3. $a_{3}=<x,b^{3}>=[3,-2,1]\cdot[-1,0,1]=-3+0+1=-2$
4. Nasz wynik końcowy zapisujemy jako równanie:
   - $x=4\cdot[1,0,1]-2\cdot[0,1,0]-2\cdot[-1,0,1]$

### Zadanie z wektorem N elementów

![](https://i.imgur.com/crOGKAH.png)

> [!cite]+ GPT - wyjaśnienie dla debila
> Widmo amplitudowe sygnału pokazuje, jakie częstotliwości składają się na dany sygnał i z jaką amplitudą one występują. W przypadku sygnału składającego się z dwóch sinusoid, widmo amplitudowe będzie składało się z dwóch pików odpowiadających tym dwóm częstotliwościom.
>
> Sygnał, który masz, to suma dwóch sinusoid:
>
> y = sin(2π/8 _ 2x + 1) + 2sin(2π/8 _ 4x)
>
> Pierwsza sinusoida ma częstotliwość 2/8 cykli na próbkę (bo 2π/8 jest częstotliwością kątową, a mnożymy ją przez 2), a druga sinusoida ma częstotliwość 4/8 cykli na próbkę (bo mnożymy 2π/8 przez 4).
>
> Widmo amplitudowe dla dyskretnego sygnału składającego się z N=8 próbek będzie miało 8 punktów. Dla sygnału, który jest sumą dwóch sinusoid, spodziewamy się zobaczyć dwa piki w widmie amplitudowym odpowiadające tym dwóm częstotliwościom.
>
> Ponieważ mamy 8 próbek, to nasze częstotliwości będą wyrażone jako wielokrotności podstawowej częstotliwości 1/8 cykli na próbkę. Pierwsza sinusoida ma częstotliwość 2/8, co odpowiada 2 \* 1/8, czyli drugiemu punktowi w widmie (pierwszy punkt to częstotliwość 0). Druga sinusoida ma częstotliwość 4/8, co odpowiada 4 \* 1/8, czyli piątemu punktowi w widmie.
>
> Amplitudy tych sinusoid to odpowiednio 1 dla pierwszej sinusoidy i 2 dla drugiej. Oznacza to, że w widmie amplitudowym spodziewamy się piku o wysokości 1 dla drugiego punktu i piku o wysokości 2 dla piątego punktu.
>
> Jeśli chcesz narysować widmo amplitudowe bez obliczania DFT, możesz po prostu zaznaczyć te dwa piki na wykresie z osią częstotliwości od 0 do (N-1)/N, czyli od 0 do 7/8 w tym przypadku. Pamiętaj, że widmo dla sygnału rzeczywistego jest symetryczne, więc piki pojawią się również dla częstotliwości ujemnych, ale w przypadku DFT dla sygnału o długości N=8, częstotliwości ujemne są "zwinięte" i odpowiadają wyższym częstotliwościom dodatnim (tzw. aliasing).
>
> Oto przykładowy wykres widma amplitudowego:
>
> ```
> Amplituda
> |
> |           *
> |           |
> |     *     |
> |     |     |
> |     |     |
> |------------------> Częstotliwość
> 0   2/8    4/8
> ```
>
> Gdzie "\*" oznacza pik w widmie amplitudowym.

Chyba będzie jedna z tych dwóch opcji, nie mam niestety jak tego zweryfikować, robiłem wszystko z gpt.

![](https://i.imgur.com/VqMSZi6.png)
![](https://i.imgur.com/SRPX40b.png)

### Zadanie z jakimiś próbkami

![](https://i.imgur.com/jMTe4QZ.png)

Po kolei:

1. Liczycie sinusy, czyli dla każdego $x_{i}$ podstawiacie $i$ do wzoru, Wyjdą wam 4 wyniki. Darmowe punkty.
2. Nasz sygnał ma częstotliwość taką, która odpowiada pełnemu cyklowi w ciągu 8 próbek, a ponieważ mamy do dyspozycji tylko 4 próbki, to sygnał wykonuje pół cyklu w oknie analizy. W tym wypadku najlepiej przyjąć taki komponent DFT, który wykona pełny cykl w ciągu tych 4 próbek, będzie to ten dla którego $k=1$ (bo $\frac{2\pi}{8}+\frac{\pi}{4}$ to $\frac{2\pi}{4}$)

A to dodatkowe to z pizdy wyjęte

### Zadanie z obliczaniem pliku dźwiękowego

> [!cite]+ Zad 3
> Częstotliwość próbkowania wynosi 8kHz, zapis 10s, a 1 próbka = 1 bajt.
> Jaki jest najmniejszy możliwy rozmiar pliku jeżeli nagłówek ma 800B?

W sumie wszystko mnożymy i dodajemy rozmiar nagłówka, essa?

![](https://i.imgur.com/5N1o4aD.png)

#psio #it
