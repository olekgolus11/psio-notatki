# Zadania typu różne

Mogą się powtarzać z zadaniami które były w osobnych działach (na pewno się powtarzają)

![[Pasted image 20240121161705.png]]

> [!example]- Moja odpowiedź
> ![](https://i.imgur.com/8OLvZ7d.png)

![[Pasted image 20240121161623.png]]

> [!example]- Moja odpowiedź
>
> 1. Progowanie adaptacyjne
> 2. Zastosowanie etykietowania połączonych komponentów
> 3. Odfiltrowanie obiektów o zwartości mniejszej niż 0.8
> 4. Zastosowanie etykietowania połączonych komponentów i zliczenie grup

![](https://i.imgur.com/Q1zQKrJ.png)

> [!example]- Moja odpowiedź
>
> 1. Zastosowanie progowania by wyróżnić słoje na biało i krawędzie na czarno
> 2. Zastosowanie etykietowania połączonych komponentów
> 3. Wyznaczyć ilość etykiet (ilość grup)
> 4. Wyznaczyć długość krótkich osi obiektów korzystając z deskryptora kształtu badającego długości osi

![](https://i.imgur.com/gnAa514.jpg)

> [!example]- Moja odpowiedź
>
> 1. Zastosowanie metody mean-shift w celu ujednolicenia kolorów danej komórki
> 2. Zastosowanie progowania wielopoziomowego by zrzutować cały obraz na 3 kolory (ciemne komórki, jasne komórki oraz tło)
> 3. Mając przekształcony obraz, będziemy osobno badać każde z grup komórek, dla każdej te same czynności:
>    1. Binaryzacja obrazu na tło + druga grupa komórek (jako czarne piksele) oraz na badaną grupę komórek (jako białe piksele)
>    2. Zastosowanie erozji by rozdzielić komórki
>    3. Zastosowanie etykietowania połączonych komponentów
>    4. Zliczenie wystąpień komórek (ilości labeli)
>    5. Zliczenie wszystkich białych pikseli
>    6. Obliczenie średniego rozmiaru jako wszystkie piksele białe / liczba komórek

![](https://i.imgur.com/MvvLxpg.png)

> [!example]- Moja odpowiedź
>
> 1. Progowanie w taki sposób, by nie naruszyć struktury owada
> 2. Erozja w celu usunięcia czułek
> 3. Otwarcie, w celu odłączenia odnóży od odwłoku
> 4. Poetykietowanie połączonych komponentów
> 5. Odfiltrowanie tych obiektów, których zwartość jest większa niż 0.4 (odnóża są bardzo mało zwięzłe więc powinny się zachować)
> 6. Poetykietowanie połączonych komponentów, zliczenie grup

![](https://i.imgur.com/iy20Kux.png)

> [!example]- Moja odpowiedź
>
> 1. Zastosowanie progowania
> 2. Erozja
> 3. Etykietowanie połączonych komponentów
> 4. Zliczenie etykiet

![](https://i.imgur.com/lq4peNu.png)

> [!example]- Moja odpowiedź
>
> 1. Na bazie obrazu utworzyłbym widmo fouriera
> 2. Zamalowałbym białe plamki na czarne xD (poza środkową)
> 3. Zastosowałbym odwrotną transformatę

![](https://i.imgur.com/KZRRDtN.png)

> [!example]- Moja odpowiedź
>
> 1. Na bazie obrazu utworzyłbym widmo fouriera
> 2. Zamalowałbym białe plamki czarnymi
> 3. Odjąłbym od oryginalnego obrazu obraz po usunięciu szumu

![](https://i.imgur.com/AadcdRa.png)

> [!example]- Moja odpowiedź
> Procedura wyostrzania polega na wyciągnięciu detali z oryginalnego obrazu za pomocą odjęcia od oryginalnego obrazu filtracji uśredniające

![](https://i.imgur.com/jYtU5hQ.png)

> [!example]- Moja odpowiedź
> Entropia na pierwszym obrazie jest bardzo niska, gdzie na drugim widać, że jest wysoka. Z tego również wynika różnica w energii na obrazach, gdzie na pierwszym jest większa niż na drugim. Można to wszystko uzyskać analizując histogramy obu obrazów.
> Można również zauważyć, że histogram pierwszego obrazka będzie znacznie węższy niż drugi => kontrast jest większy na drugim obrazku

![](https://i.imgur.com/lz4lc0H.png)

> [!example]- Moja odpowiedź
>
> 1. [[Segmentacje#Progowanie adaptacyjne]]
> 2. [[Segmentacje#Progowanie]]
> 3. [[Segmentacje#Metoda min przekroju / max przepływu]]
> 4. [[Segmentacje#Progowanie adaptacyjne]]
> 5. [[Segmentacje#Algorytm Felzenszwalba i Huttenlochera (FiH)]]

![](https://i.imgur.com/gMXOfFo.png)

> [!example]- Moja odpowiedź
>
> 1. [[Operacje morfologiczne#White top-hat]] - Obrazuje różnicę, która powstaje w wyniku otwarcia - może się przydać kiedy chcemy usunąć księżyc z gwieździstego nieba xD
> 2. [[Operacje morfologiczne#Zamykanie (wypełnianie)]] - Wypełnia obraz wzdłuż konkretnych krawędzi - może się przydać jak chcemy zrobić zdjęcie pizzy i usunąć składniki xD
> 3. [[Operacje morfologiczne#Black top-hat]] - obrazuje różnicę, która powstaje w wyniku zamknięcia - może się przydać kiedy chcemy zostawić oko z illuminati 😀

![](https://i.imgur.com/1FhNVAL.png)

> [!example]- Moja odpowiedź
> ![](https://i.imgur.com/gwoY42Q.png)

![](https://i.imgur.com/FvPQdMh.png)

> [!example]- Moja odpowiedź
> a)
>
> 1. Kurtoza
> 2. Skośność
>    b)
> 3. Entropia
> 4. Energia

![](https://i.imgur.com/UQMSQsA.png)

> [!example]- Moja odpowiedź
>
> 1. Entropia :D
> 2. Energia :D
> 3. Kurtoza

![](https://i.imgur.com/3wnHOEP.png)

> [!example]- Moja odpowiedź
>
> 1. [[Segmentacje#Progowanie adaptacyjne]]
> 2. [[Segmentacje#Rozrost obszaru]]
> 3. [[Segmentacje#Model typu balon]]
> 4. [[Segmentacje#Metoda działów wodnych]] + markery
> 5. [[Segmentacje#Algorytm Felzenszwalba i Huttenlochera (FiH)]]

![](https://i.imgur.com/c8A7B4e.png)

> [!example]- Moja odpowiedź
>
> 1. [[Operacje morfologiczne#Zamknięcie]]
> 2. Chujoza garbata
> 3. [[Operacje morfologiczne#Szkielet]]

![](https://i.imgur.com/z2K6Loj.png)

> [!example]- Moja odpowiedź
> Krawędź to gwałtowna różnica jasności. Do wykrycia poziomych krawędzi można użyć maski gradientowej sobela ze współczynnikiem Gx

![](https://i.imgur.com/vF4idEU.png)

> [!example]- Moja odpowiedź
>
> 1. oryginał
> 2. Wyrównanie
> 3. Rozciąganie
>    Różnica jest taka, że wyrównanie to linearyzacja dystrybuanty, a rozciąganie to rozciągnięcie histogramu na dany zakres wartości

![](https://i.imgur.com/qD1q2vj.png)

> [!example]- Moja odpowiedź
> 0-1-2-3-4-4-6-6-0-6

![](https://i.imgur.com/XWeoJUT.png)

> [!example]- Moja odpowiedź
>
> 1. [[Segmentacje#Algorytm Felzenszwalba i Huttenlochera (FiH)]]
> 2. [[Segmentacje#Klasteryzacja|Klasteryzacja na podstawie cech teksturalnych]]
> 3. [[Segmentacje#Metoda działów wodnych|Metoda działów wodnych z markerami]]
> 4. [[Segmentacje#Model typu balon]]
> 5. [[Segmentacje#Progowanie adaptacyjne]]

![](https://i.imgur.com/plGr5mV.png)

> [!example]- Moja odpowiedź
> ![](https://i.imgur.com/MBrREgX.png)

![](https://i.imgur.com/N8msBno.png)
![](https://i.imgur.com/VdJI5zQ.png)
![](https://i.imgur.com/rFpdNsU.png)
![](https://i.imgur.com/mDRDi5k.png)
![](https://i.imgur.com/lKY68u7.png)
![](https://i.imgur.com/HtyuxKS.png)
![](https://i.imgur.com/Pxu0ali.png)
![](https://i.imgur.com/fOw7olJ.png)
![](https://i.imgur.com/1J9U5qr.png)
![](https://i.imgur.com/A3Ui85c.png)
![](https://i.imgur.com/B7ajlNk.png)
![](https://i.imgur.com/cyDx1XE.png)
![](https://i.imgur.com/rHhOHZs.png)
![](https://i.imgur.com/xxOnG71.png)
![](https://i.imgur.com/c40JNU5.png)
![](https://i.imgur.com/Fhbxdxu.png)
