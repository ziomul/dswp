# Statystyka
Głównym celem statystyki jest pozyskiwanie, prezentacja i analiza danych. Statystyka pozwala na wnioskowanie
z surowych danych. Np. mając próbkę danych pewnej populacji możemy podjąć próbę wyznaczenia wartości
oczekiwanej dla **średniej**. Następnie, można zweryfikować hipotezę, czy obliczona wartość jest zgodna z
założeniami. Istnieje wiele dziedzin statystki, które poddają analizie dane w bardzo różny sposób. 
## Możemy wyróżnić:
* Statystyka opisowa – głównym celem jest opis danych statystycznych uzyskanych podczas badania
statystycznego za pomocą wybranych parametrów, dzięki czemu można dokonać pewnych uogólnień na temat
danych, jak również wyciągnąć podstawowe wnioski.
* Testowanie hipotez – głównym celem testowania hipotez jest weryfikacja ogólnie postawionych założeń na
temat rozkładu, bądź określonych parametrów (takich jak wariancja, czy średnia).
* Analiza korelacji i regresji – głównym celem jest określenie współzależności zjawisk za pomocą korelacji oraz
wyznaczenie funkcji zależności pomiędzy zmiennymi za pomocą regresji.
* Analiza szeregów czasowych – głównym celem jest badanie zależności obserwowanych danych w stosunku do
określonego stałego przedziału czasowego (np. godzina, dzień, miesiąc).

## Głównymi pakietami w Pythonie do zastosowania w statystyce są:

Informacje dotyczące funkcji statystycznych w pakiecie SciPy.stats można znaleźć:
[link](https://docs.scipy.org/doc/scipy/reference/stats.html)



### Kod w python
import numpy as np
from scipy.stats import scoreatpercentile
data = np.loadtxt("Wzrost.csv", delimiter=',', skiprows=0, unpack=True)
print(data)
Statystyka i Algebra w Praktyce
4
data1 = np.loadtxt("FL_insurance_sample.csv", delimiter=',', usecols=(7,),
skiprows=1, unpack=True)
print(data1)
print(len(data1))
print("Maksymalny wzrost:", data.max())
print("Maksymalny wzrost, funkcja:", np.max(data))
print("Minimalny wzrost:", data.min())
print("Minimalny wzrost, funkcja:", np.min(data))
print("Średni wzrost:", data.mean())
print("Średni wzrost, funkcja:", np.mean(data))
print("Odchylenie standardowe, wzrost:", data.std())
print("Odchylenie standardowe, wzrost, funkcja:", np.std(data))
print("Mediana:", np.median(data))
print("Wartość na 50 procencie:", scoreatpercentile(data, 50))
