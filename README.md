# glosowa__lacznosc

#W ramach tego projektu przeprowadzono analizę rozpoznawania komend głosowych.
Razem z innymi osobami zostały wybrane komendy głosowe, które potencjalnie mogłyby zostać użyte do sterowania np. inteligentnego budynku.
Po podziale komend uzyskano 43 słowa, w tym głoska W powtarzała się 3 krotnie, słowo ALARM oraz GARAŻ po dwa razy, co uwzględniono w wykonanym projekcie. W sumie posiadano nagrania od 10 osób (po 4 razy) z pełnym poprawnym opisem. 
W pre-processingu dokonano odszumienia sygnału oraz go docięto. 
Kolejno wyznaczono współczynniki takie jak długość słowa, średnia, energia, entropia, amplituda, normalizacja, wartość skuteczna, połowa różnicy pomiędzy trzecim a pierwszym kwartylem, maksimum, minimum oraz parametry w dziedzinie częstotliwości takie jak:  najczęściej występująca częstotliwość, kurtoza, skośność, średnia ważona częstotliwość. Jednak jak pokazała analiza nie miały one znaczącego wpływu na jakość wyników. 
Kluczowym rozwiązaniem było użycie melowych współczynników cepstralnych. Do tego celu rozciągnięto sygnał. 
Uzyskaną macierz MFCC rozwięnięto i tak też użyto do klasyfikacji. Przed samą klasyfikacją poddano jeszcze analizie głównych składowych wszystkie cechy ze względu na ich wielowymiarowość. Wybrano 20 głównych składowych, co okazało się najbardziej optymalne. 
Dane podzielono w stosunku 2:1 (uczące, testowe). Do klasyfikacji, ze względu na dużo liczbę zmiennych oraz zmienność dannych użyto klasyfikatora Random Forest. Uzyskano dokładność predykcji w wysokości 82%. Wyniki zobrazowano na Confusion Matrix w wersji znormalizowanej. 


#project

#In the framework of this project was carried out an analysis of the voice command recognition.
Together with other people, voice commands have been selected that could potentially be used to control, for example, a smart building.
After the division of the commands, 43 words were obtained, including the W-word repeating three times, the word ALARM and GARAZ twice, which was included in the project. In total, recordings were made from 10 people (4 times each) with a full correct description.
In the pre-processing, the signal was denoted and cut.
Subsequently, coefficients such as word length, average, energy, entropy, amplitude, normalization, effective value, half the difference between the third and the first quartile, maximum, minimum and frequency domain parameters such as: frequency, kurtosis, skewness, weighted average frequency. However, as the analysis showed, they did not have a significant impact on the quality of the results.
The key solution was to use melt Cepstral coefficients. The signal was stretched for this purpose.
The resulting MFCC matrix was developed and used for classification as well. Before the classification itself, all features were analyzed for the main components due to their multidimensionality. The main 20 components were chosen, which turned out to be the most optimal.
Data was divided in a 2: 1 ratio (teaching, testing). For the classification, due to a large number of variables and variability of data, the Random Forest classifier was used. A prediction accuracy of 82% was obtained. The results were visualized on the Confusion Matrix in the standard version.
