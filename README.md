# Rowerowy Gdańsk - analiza danych z liczników rowerowych za lata 2013-2023

Zobacz gotowy raport: <br>
[Tableau Public](https://public.tableau.com/app/profile/justyna5640/viz/RowerowyGdask2013-2023/RowerowyGdansk)

# SPIS TREŚCI
* [TL;DR](#tldr)
* [1. DANE](#1.DANE)
  
# TL;DR
Projekt powstał "dla zabawy", w celu praktycznego wykorzystania umiejętności obsługi PowerQuery oraz Tableau Public.<br>
Cel: przekształcenie publicznie dostęnych danych w formę zdatną do analizy i przedstawienie ich w formie graficznej.<br>
Użyte programy: Excel, PowerQuery, Tableau Public.<br>
Na chwilę obecną zakładam, że projekt był jednorazowy i bazuje na danych do lipca 2023 włącznie, nie wykluczam jednak późniejszych aktualizacji.

# 1. Dane źródłowe
## 1.1. Źródło
W momencie tworzenia projektu (lipiec-sierpień 2023) w Gdańsku znajduje się 29 liczników rowerowych, które pojawiały się w mieście stopniowo od października 2013.<br>
Wszystkie dane dot. zarejestrowanych przejazdów są udostępniane publicznie na stronie [https://rowerowygdansk.pl/](https://rowerowygdansk.pl/pomiar-ruchu) w formie plików .xls zawierających dzienne i miesięczne statystyki od momentu instalacji licznika.
<br>
Część plików zaimportowałam do PowerQuery bezpośrednio ze strony internetowej. Niestety w przypadku znacznej części plików napotkałam niezidentyfikowany problem z ładowaniem nagłówków tabeli, co wymagało wstępnej edycji danych w Excelu. 
<br><br>
Udostępniane dane są wygodne do odczytu dla ludzkiego oka, lecz nie nadające się do analizy przez komputer:
<br><br>
![Widok w Excelu](Screenshots/RG01_Excel.png)
<br><br>
Po załadowaniu do PowerQuery tabela wygląda następująco:<br>
![Widok w PowerQuery](Screenshots/RG02_PQ.png)
<br><br>

## 1.2. Oczyszczanie danych
W celu otrzymania danych w formie zdatnej do analizy konieczne było:
1) Usunięcie pustych/niepotrzebnych kolumn i wierszy.<br> W poszczególnych plikach tabele ładowane były do różnych komórek, stąd pierwsze kroki w każdym z zapytań musiałam przygotować ręcznie.
2) Ustawienie nagłówków tabeli
3) "Unpivot"
4) Dodanie jednej kolumny z datą zamiast osobnych na rok i miesiąc.
5) Połączenie poszczególnych zapytań w jedną zbiorczą tabelę (screen efekt końcowy)

## 1.3. Automatyzacja pracy
Z uwagi na dużą ilość zapytań wymagających praktycznie identycznych czynności pomocna okazała się opcja edytora zaawansowanego.<br>
![alt text](Screenshots/RG03_advanced.png)
Przy prawie 30 podobnych plikach była to znaczna oszczędność czasu.

## 1.6. Samo życie
W tym momencie musiałam wziąć pod uwagę możliwości mojego komputera, któremu przetwarzanie dokumentu z tak dużą ilością zapytań zajmowało zbyt wiele czasu. Skopiowałam więc wartości ze zbiorczej tabeli do nowego, pustego pliku, i pracowałam już tylko na nim.

# 2. Dane geograficzne
Dane udostępniane przez miasto nie zawierają dokładnych danych dot. lokalizacji, jednak mając dostępny opis miejsca, znaczniki dostępne na stronie (https://rowerowygdansk.pl/mapa-rowerowa), Google Maps oraz trochę cierpliwości :) mogłam zebrać te dane ręcznie. 
//screen mapy rowerowej

# 3. Tableau Public
Do stworzenia i udostępnienia raportu wybrałam Tableau, z uwagi na możliwość wygodnego upublicznienia efektu.

# 4. Plany na przyszłość
W miarę zdobywania umiejętności zamierzam stworzyć podobny, ulepszony raport w Power BI.
