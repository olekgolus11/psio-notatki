# Deskryptory kształtu
Deskryptory kształtu to generalnie takie sposoby, które w jakiś konkretny sposób opisują dany kształt. Różne deskryptory przejawiają różne cechy, takie jak owalność, dziurawość, rozmiar, nieregularność etc.

- [[#Pole powierzchni / objętość]]
- [[#Środek ciężkości]]
- [[#Obwód]]
- [[#Długości osi]]
- [[#Orientacja]]
- [[#Bounding box]]
- [[#Rectangularity]]
- [[#Ekscentryczność]]
- [[#Cyrkularność / krągłość / zwartość]]
- [[#Liczba Eulera]]
- [[#Kod łańcuchowy]]
- [[#Sygnatury]]
- [[#Tekstura]]

No i zadanka
- [[#Zadania]]


### Pole powierzchni / objętość
Tak jak nazwa wskazuje

![](https://i.imgur.com/yyDOY2q.png)

### Środek ciężkości
Nie wiem jak to ma cokolwiek pomóc w opisaniu kształtu, raczej mówi o tym gdzie obiekt się znajduje na płaszczyźnie

![](https://i.imgur.com/b2QjI3o.png)

### Obwód
Tak jak nazwa wskazuje

![](https://i.imgur.com/o3Rb8sa.png)

### Długości osi
Raczej do owalnych kształtów, same długości osi mogą być wykorzystywane do innych rzeczy opisanych niżej

![](https://i.imgur.com/WeZZGbR.png)

### Orientacja
Może przydać się gdy chcemy wydobyć obiekty skierowane w tym samym kierunku. Wyznaczana jest poprzez wskazanie osi symetrii dłuższej przekątnej elipsy, która dany kształt otacza (widoczne na rysunku)

![](https://i.imgur.com/UHmbOdZ.png)

### Bounding box
Bounding boxem nazywamy najmniejszy prostokąt który zawiera dany obszar. Oprócz tego jest kilka innych odmian podobnego rozwiązania, tj bounding circle oraz convex hull.

Na bazie wysokości i szerokości boxów możemy stwierdzić, co zostało wykryte, np. człowiek ma inne stosunki tych długości do samochodu czy pasów.

Po prawej stronie widać jak bounding box zadziała w przypadku obróconego o kilka stopni prostokąta i jak lepiej sobie z tym poradzi convex hull (który nie uwzględnia wklęśnięć).

![](https://i.imgur.com/WMPXsM4.png)

### Rectangularity
Na podstawie stosunku pola powierzchni do bounding boxa określamy jak bardzo kształt jest zbliżony do prostokąta.

![](https://i.imgur.com/BKGW0Tf.png)

### Ekscentryczność
Wspomniane w [[#Długości osi]] osie mogą przydać się do obliczenia czegoś innego. W tym przypadku korzystamy z nich do obliczenia ich stosunków do siebie, by następnie wyznaczyć ekscentryczność, która jest parametrem przybliżenia do okręgu. Im bliżej okręgu, tym parametr bliższy 1.

![](https://i.imgur.com/txB5dSi.png)

### Cyrkularność / krągłość / zwartość
Podobnie jak [[#Ekscentryczność]], wyznacza to miarę podobieństwa do koła. W tym wypadku jednak zamiast stosunku osi wykorzystujemy stosunek obwodu do czegoś razy pole powierzchni

![](https://i.imgur.com/SHsKOnN.png)


![](https://i.imgur.com/KaBiZ2Z.png)

![](https://i.imgur.com/pVufnEA.png)

### Liczba Eulera
Magiczna liczba opisująca topologię obiektu w taki sposób, że prezentuje różnicę osobnych obiektów i dziur w nich

![](https://i.imgur.com/afDjktB.png)

![](https://i.imgur.com/NxnEe9s.png)

### Kod łańcuchowy
Reprezentuje kontur danego obiektu poprzez sekwencję liczb, oznaczających dany kierunek na kompasie:
#### Bezwzględny
![](https://i.imgur.com/Bb1ZKQU.png)
#### Względny
![](https://i.imgur.com/bqS2rq1.png)

### Sygnatury
Obrazuje na wykresie zmienianie się kąta krawędzi w miarę przechodzenia wzdłuż tej krawędzi "rysikiem od środka". Na wykresie widzimy długość jak bardzo rysik musi się wydłużyć.

![](https://i.imgur.com/v69MIsM.png)


![](https://i.imgur.com/OLebsVN.png)

### Tekstura
Nie posiada konkretnej definicji, jest zestawem różnych cech

![](https://i.imgur.com/iw7gRXk.png)
#### Entropia i energia
Entropię rozumiemy jako losowość, tak jak w fizyce: wysoka entropia - wysoka losowość. Natomiast energię rozumiemy jako skupioną energię, niską entropię.

![](https://i.imgur.com/PPDKVZS.png)

![](https://i.imgur.com/1qACP0V.png)

## Zadania
![](https://i.imgur.com/D0ZCNb7.png)
![](https://i.imgur.com/G6jo8rl.png)
![](https://i.imgur.com/NnHCHLs.png)
![](https://i.imgur.com/39Q6w5Y.png)



#psio #it 