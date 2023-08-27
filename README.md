# SPIS TREŚCI
* [TL;DR](#tldr)
* [1. DANE](#1.DANE)
  
# TL;DR
Projekt powstał "dla zabawy", w celu praktycznego wykorzystania umiejętności obsługi PowerQuery oraz Tableau Public.
Cel: przekształcenie publicznie dostęnych danych w formę zdatną do analizy i przedstawienie ich w formie graficznej.
Użyte programy: Excel, PoqweQuery, Tableau Public.
Plany na przyszłość: stworzenie podobnej analizy z wykorzystaniem Power BI.
Na chwilę obecną zakładam, że projekt był jednorazowy i bazuje na danych do czerwca 2023 włącznie, nie wykluczam jednak późniejszych aktualizacji.

# 1. DANE
## 1.1. Źródło
W momencie tworzenia projektu (lipiec-sierpień 2023) w Gdańsku znajduje się 29 liczników rowerowych, które pojawiały się w mieście stopniowo od października 2013.<br>
Wszystkie dane dot. zarejestrowanych przejazdów są udostępniane publicznie na stronie [https://rowerowygdansk.pl/](https://rowerowygdansk.pl/pomiar-ruchu) w formie plików .xls zawierających dzienne i miesięczne statystyki od momentu instalacji licznika.

Udostępniane dane są wygodne do odczytu dla ludzkiego oka, lecz nie nadające się do analizy przez komputer. W celu ich obróbki skorzystałam z dodatku PowerQuery.
// screen RG1_Excel

## 1.2. Import danych
Część plików zaimportowałam do PowerQuery bezpośrednio ze strony internetowej. Niestety w przypadku znacznej części plików napotkałam niezidentyfikowany problem z ładowaniem nagłówków tabeli, co wymagało wstępnej edycji danych w Excelu. 
// screen RE02_PQ

# 2. PRZEKSZTAŁCENIE DANYCH


