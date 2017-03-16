# Laboratorium 1

> Narzędzia, ramki i zbiory danych, ich statystyki opisowe, preprocessing i proste uczenie maszyn.

## Narzędzia [`1_tools.py`](1_tools.py)

Aby móc korzystać z _Pythona_, w systemie operacyjnym musimy zainstalować jego interpreter (_szok_). Najwygodniejszym rozwiązaniem w tym wypadku jest zainstalowanie pakietu [Anaconda](https://www.continuum.io/downloads), który zawiera już wszystkie narzędzia potrzebne do wykonywania eksperymentów z maszynami uczącymi się.

Aby sprawdzić, czy na twojej maszynie zainstalowany jest interpreter języka _Python_, zwyczajnie wpisz w terminalu komendę `python`. Jeśli wszystko jest w normie, odpowie Ci jego znak zachęty.

Pierwszy skrypt towarzyszący temu laboratorium importuje wszystkie potrzebne nam biblioteki i wyświetla ich wersje.

```python
import sys
import scipy as sp
import numpy as np
import matplotlib as plt
import pandas as pd
import sklearn as skl

print 'Python: %s' % sys.version
print 'scipy: %s' % sp.__version__
print 'numpy: %s' % np.__version__
print 'matplotlib: %s' % plt.__version__
print 'pandas: %s' % pd.__version__
print 'sklearn: %s' % skl.__version__
```

> **Zadanie 1:** Stwórz własny skrypt, w którym zaimportujesz wszystkie potrzebne biblioteki i przywitasz się ze światem.

## Ramki danych [`2_data_frame.py`](2_data_frame.py)

Krótkie wprowadzenie do języka _Python_:

![](https://imgs.xkcd.com/comics/python.png)

- ten język jest prosty i jeśli umiesz programować w jakimkolwiek innym (a najpewniej umiesz), poradzisz sobie,
- komentujesz przy użyciu płotka (`#`),
- nie musisz deklarować typów zmiennych,
- zamiast klamerek stosujesz wcięcia (a więc znaczenie ma nie tylko wielkość znaków, ale i spacje).
- jeśli czegoś nie wiesz, wiesz, gdzie znajduje się [Stack Overflow](https://stackoverflow.com)

W tym zadaniu tworzymy tak zwaną _ramkę danych_, która różni się od klasycznej tablicy tym, że każdy wiersz i każda kolumna ma swoją nazwę. Będziemy potrzebować bibliotek `numpy` i `pandas`.

```python
import numpy as np
import pandas as pd
```

Na początek tworzymy tablicę. Nie jest to jednak tablica zwyczajna, a tablica `numpy`. Z pozoru nie różni się niczym od tej zadeklarowanej klasycznie, ale w rzeczywistości pozwala nam na skrócenie większości operacji i dzięki niej praktycznie niczego nie będziemy musieć wykonywać ręcznie.

```python
array = np.array([[1, 2, 3], [4, 5, 6]])
```

Chcemy jednak przygotować własną ramkę danych, a taka zawiera także opisy dla kolumn i wierszy. Przygotujmy sobie więc odpowiednie łańcuchy.

```python
index = ['first row', 'last row']
columns = ['was', 'is', 'will be']
```

Dysponując już wszystkimi potrzebnymi danymi, wykorzystując bibliotekę `pandas`, tworzymy ramkę danych.

```
dataFrame = pd.DataFrame(array, index=index, columns=columns)
```

> **Zadanie 2:** Wyświetl na ekranie utworzoną ramkę danych i zacznij chwalić się przed znajomymi, że programujesz w Pythonie.

## Zbiory danych [`3_dataset.py`](3_dataset.py)

Jeśli prowadzimy eksperymenty naukowe, z reguły wypada móc porównać swoje wyniki badań z innymi. W związku z tym, w przeważającej większości przypadków, testujemy nasze metody wykorzystując tak zwane _dane benchmarkowe_. Najbardziej powszechnie stosowanym źródłem takich danych jest [repozytorium UCIML](http://archive.ics.uci.edu/ml/).

Do niniejszej instrukcji dodany został plik [`wine.csv`](wine.csv), zawierający przykładowy, typowy zbiór danych, o którym więcej przeczytać możesz [na stronie repozytorium](http://archive.ics.uci.edu/ml/datasets/Wine). Zbiory najczęściej udostępniane są w formacie CSV. Jeśli nie wiesz, czym jest format CSV, nie przyznawaj się i sprawdź [w Wikipedii](https://en.wikipedia.org/wiki/Comma-separated_values). W skrócie to format tabeli, w którym wszystkie dane zapisujemy tekstowo, komórki oddzielamy przecinkiem, a kolejne wiersze – znakiem nowej linii.

Dla wygody, przed eksperymentami wczytujemy taki zbiór danych jako _ramkę danych_. Jak już wiesz, taka forma wymaga opisanych kolumn i wierszy. Opisem wiersza będzie w tym wypadku numer obiektu, więc nie musimy się nim martwić, ale opisy kolumn musimy już uzupełnić.

Przykładowo, dla zbioru `wine`:

```python
names = ['class', 'Alcohol', 'Malic acid', 'Ash', 'Alcalinity of ash ', 'Magnesium', 'Total phenols', 'Flavanoids', 'Nonflavanoid phenols', 'Proanthocyanins', 'Color intensity', 'Hue', 'OD280/OD315 of diluted wines', 'Proline']
```

Biblioteka `pandas` posiada wbudowaną funkcję wczytującą pliki CSV do ramek, więc używamy jej, aby odczytać nasz zbiór danych.

```python
data = pd.read_csv('wine.csv', names=names)
```

> **Zadanie 3:** Wybierz z repozytorium UCI jeden zbiór danych, przeczytaj jego opis i uzupełnij swój skrypt o wczytywanie tego zbioru, pamiętając o odpowiednim nazwaniu kolumn.

## Statystyki opisowe

## Preproccesing

## Uczenie
