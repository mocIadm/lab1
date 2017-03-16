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

## Ramki danych

## Zbiory danych

http://archive.ics.uci.edu/ml/

## Statystyki opisowe

## Preproccesing

# Uczenie
