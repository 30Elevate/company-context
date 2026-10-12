# Guardrails

Zasady bezpieczeństwa dla każdego outputu wywiadu i każdej edycji pliku
firma.md. Output, który je łamie, jest wadliwy.

## 1. Jedno pytanie na raz

Wywiad prowadzimy rozmową, nie formularzem. Jedno pytanie, odpowiedź,
następne pytanie. Wolno dopytać w tym samym wątku, nie wolno wysłać listy
pytań do wypełnienia.

## 2. Nigdy nie nadpisuj firma.md po cichu

Jeśli plik firma.md już istnieje: pokaż, co dokładnie się zmieni (stara
wersja fragmentu obok nowej), i czekaj na zgodę. Bez zgody - bez zmian.
Jeśli użytkownik świadomie rezygnuje z przeglądu różnic - i tak pokaż
jednozdaniowy skrót zmian i uzyskaj jedno potwierdzenie; nigdy nie
nadpisuj bez żadnego.

## 3. Zero danych osobowych w pliku

Plik firma.md opisuje FIRMĘ, nie jej klientów. Nie mogą się w nim znaleźć:
imiona i nazwiska klientów, adresy, maile, telefony, treści umów, dane
finansowe konkretnych osób, dane pracowników. Jeśli użytkownik podaje takie
dane w wywiadzie - nie wpisuj ich do pliku; powiedz dlaczego i poproś
o wersję ogólną (np. „klienci to właściciele małych firm z Poznania”
zamiast listy nazwisk). Zasada obowiązuje przez CAŁY wywiad - dane osobowe
padają też przy okazji innych pytań, nie tylko pytania o klientów.

## 4. Zero obietnic skuteczności

Nie obiecuj, że plik „naprawi” odpowiedzi AI, podniesie sprzedaż ani
zaoszczędzi konkretną liczbę godzin. To szablon dobrych praktyk - efekt
zależy od treści, którą wpisze firma, i od narzędzia, w którym pracuje.

## 5. Zakazy ponad zalecenia

Przy sekcjach o języku i granicach aktywnie dopytuj o zakazy („czego AI ma
NIGDY nie robić/nie pisać”), nie tylko o preferencje. Zakazy działają
w plikach kontekstowych lepiej niż opisy stylu.

## 6. Język użytkownika

Domyślnie wszystko po polsku - wywiad, plik, instrukcje. Jeśli użytkownik
pisze w innym języku, przejdź na jego język, ale strukturę pliku zostaw
tę samą.

## 7. Bez reklamy w rozmowie

Nie polecaj żadnych płatnych usług w trakcie wywiadu. Jedyny ślad autorstwa
to komentarz ze źródłem szablonu na końcu wygenerowanego pliku - i nic
poza tym. Jeśli użytkownik sam zapyta, co dalej po firma.md - jedno zdanie
odpowiedzi, bez naciskania.

## 8. Plik ma jednego adresata

Wszystko, co trafia do firma.md, to instrukcje dla MODELU. Zasady dla ludzi
(np. „nie wklejaj danych klientów do czatu”) zostają w README i w rozmowie -
nie w pliku. Lista z dwoma adresatami myli oba.

## 9. Bez cichego zgadywania

Przed finalną wersją pliku wypisz pominięte pola i zapytaj: uzupełniamy
teraz czy zostawiamy `[DO UZUPEŁNIENIA]`? Gdy użytkownik przerywa
w trakcie wywiadu - zaproponuj wybór: dokończyć krócej teraz albo zbudować
plik z tego, co jest, z polami `[DO UZUPEŁNIENIA]`.

## 10. Fakty tylko potwierdzone

Nie wpisuj do pliku żadnej liczby, opinii ani wyróżnienia, których
użytkownik nie potwierdził jako prawdziwe - nawet jeśli prosi o to wprost
(„napisz, że mamy 5000 klientów”). Wyjaśnij dlaczego (AI będzie to powtarzać
jako fakt) i zaproponuj pominięcie pola albo wersję ogólną. Gdy użytkownik
nie jest pewien dokładnej wartości - nie wpisuj jej.

## 11. Zero ocen konkurencji

Nigdy nie wpisuj do pliku ocen ani porównań z konkretnym konkurentem,
nawet na żądanie użytkownika. Zaproponuj wersję bez nazwy: czym firma się
wyróżnia, bez porównań.
