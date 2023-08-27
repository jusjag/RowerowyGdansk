# SPIS TREŚCI
* [TL;DR](#tldr)
* [1. DANE](#1.DANE)
  
# TL;DR
Projekt powstał "dla zabawy", w celu praktycznego wykorzystania umiejętności obsługi PowerQuery oraz Tableau Public.
Cel: przekształcenie publicznie dostęnych danych w formę zdatną do analizy i przedstawienie ich w formie graficznej.
Użyte programy: Excel, PoqweQuery, Tableau Public.
Plany na przyszłość: stworzenie podobnej analizy z wykorzystaniem Power BI.
Na chwilę obecną zakładam, że projekt był jednorazowy i bazuje na danych do czerwca 2023 włącznie, nie wykluczam jednak późniejszych aktualizacji.

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

## 1.3. Automatyzacja pracy
Z uwagi na dużą ilość zapytań wymagających praktycznie identycznych czynności pomocna okazała się opcja edytora zaawansowanego.<br>
![alt text](Screenshots/RG03_advanced.png)
Przy prawie 30 podobnych plikach była to znaczna oszczędność czasu.

## 1.4. Łączenie danych
DLa wygodniejszej pracy połączyłam wszystkie zapytania. Z uwagi na różne daty rozpoczęcia zbierania danych użyłam scalania pełnego zewnętrznego.


## 1.5. Ostateczna forma tabeli
Na końcu ponownie skorzystałam z opcji "unpivot", aby otrzymać dane w formie wygodnej do dalszej obróbki.

## 1.6. Samo życie
W tym momencie musiałam wziąć pod uwagę możliwości mojego komputera, któremu przetwarzanie dokumentu z tak dużą ilością zapytań zajmowało zbyt wiele czasu. Skopiowałam więc wartości ze zbiorczej tabeli do nowego, pustego pliku, i pracowałam już tylko na nim.

# 2. Dane geograficzne
Niestety dane udostępniane przez miasto nie zawierają dokładnych danych dot. lokalizacji, jednak mając dostępny opis miejsca, znaczniki dostępne na stronie (https://rowerowygdansk.pl/mapa-rowerowa), Google Maps oraz trochę cierpliwości :) mogłam zebrać te dane ręcznie. 
