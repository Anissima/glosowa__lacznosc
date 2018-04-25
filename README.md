# glosowa__lacznosc

#W ramach tego projektu przeprowadzono analizę rozpoznawania komend głosowych.
Razem z innymi osobami zostały wybrane komendy głosowe, które potencjalnie mogłyby zostać użyte do sterowania np. inteligentnego budynku.
Po podziale komend uzyskano 43 słowa, w tym głoska W powtarzała się 3 krotnie, słowo ALARM oraz GARAŻ po dwa razy, co uwzględniono w wykonanym projekcie. W sumie posiadano nagrania od 10 osób (po 4 razy) z pełnym poprawnym opisem. 
W pre-processingu dokonano odszumienia sygnału oraz go docięto. 
Kolejno wyznaczono współczynniki takie jak długość słowa, średnia, energia, entropia, amplituda, normalizacja, wartość skuteczna, połowa różnicy pomiędzy trzecim a pierwszym kwartylem, maksimum, minimum oraz parametry w dziedzinie częstotliwości takie jak:  najczęściej występująca częstotliwość, kurtoza, skośność, średnia ważona częstotliwość. Jednak jak pokazała analiza nie miały one znaczącego wpływu na jakość wyników. 
Kluczowym rozwiązaniem było użycie melowych współczynników cepstralnych. Do tego celu rozciągnięto sygnał. 
Uzyskaną macierz MFCC rozwięnięto i tak też użyto do klasyfikacji. Przed samą klasyfikacją poddano jeszcze analizie głównych składowych wszystkie cechy ze względu na ich wielowymiarowość. Wybrano 20 głównych składowych, co okazało się najbardziej optymalne. 
Dane podzielono w stosunku 2:1 (uczące, testowe). Do klasyfikacji, ze względu na dużo liczbę zmiennych oraz zmienność dannych użyto klasyfikatora Random Forest. Uzyskano dokładność predykcji w wysokości 82%. Wyniki zobrazowano na Confusion Matrix w wersji znormalizowanej. 
