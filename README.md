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

## Ramki danych [`2_data.py`](2_data.py)

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

Chcemy jednak stworzyć sobie ramkę danych, a taka zawiera także opisy dla kolumn i wierszy. Przygotujmy sobie więc odpowiednie łańcuchy.

```python
index = ['first row', 'last row']
columns = ['was', 'is', 'will be']
```

Dysponując już wszystkimi potrzebnymi danymi, wykorzysując bibliotekę `pandas`, tworzymy ramkę danych.

```
dataFrame = pd.DataFrame(array, index=index, columns=columns)
```

> **Zadanie 2:** Wyświetl na ekranie utworzoną ramkę danych i zacznij chwalić się przed znajomymi, że programujesz w Pythonie.

## Zbiory danych

http://archive.ics.uci.edu/ml/

## Statystyki opisowe

## Preproccesing

# Uczenie
