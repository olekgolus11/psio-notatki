# Normalizacja jasności
- [[#Opis]]
- [[#Zadania]]

## Opis

Jest to nic innego jak zmapowanie jasności z jednego zakresu na drugi.

Wzór nie jest specjalnie skomplikowany i można go zrozumieć.
Każdy osobny pixel mapujemy w taki sposób:

$$L_{N}(x,y)=(L(x,y)-L_{min})\cdot\frac{L_{Nmax}-L_{Nmin}}{L_{max}-L_{min}}+L_{Nmin}$$

Można rozumieć to w taki sposób:

1. Pierwsza faza równania $L(x,y)-L_{min}$ to przerzucenie wartości na bezwzględną
2. Druga $\frac{L_{Nmax}-L_{Nmin}}{L_{max}-L_{min}}$ to obliczenie stosunku pomiędzy nowym zakresem a starym 
3. Następnie mnożymy wartość bezwzględną przez ten stosunek
4. A na koniec dodajemy wartość minimalną nowego zakresu by zrzutować to z powrotem na wartość względną

## Zadania
![](https://i.imgur.com/dTrXsVM.png)
![](https://i.imgur.com/sn7pz5M.png)


#psio #it