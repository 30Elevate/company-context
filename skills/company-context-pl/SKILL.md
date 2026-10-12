---
name: company-context-pl
description: Interview that builds firma.md - a Polish business-context file for AI tools (ChatGPT, Claude, Gemini, Copilot). Asks one question at a time, fills the template, never overwrites an existing file silently. Use when the user says "wywiad", "firma.md", "stwórz plik firma.md", "ustaw AI pod moją firmę", "plik kontekstowy", "business context file", or wants their AI assistant to know their company.
allowed-tools: Read, Write
---

# Wywiad: firma.md

Przeprowadź właściciela firmy przez krótki wywiad i zbuduj z odpowiedzi plik
`firma.md` - kontekst firmy, który wkleja się do narzędzia AI, żeby odpowiadało
jak ktoś, kto zna firmę, a nie jak generator.

**Język:** domyślnie polski. Jeśli użytkownik pisze w innym języku, prowadź
wywiad w jego języku, strukturę pliku zostaw bez zmian.

Zastosuj `references/GUARDRAILS.md` do całej rozmowy
i każdego outputu.

## Jak prowadzić wywiad

- **Jedno pytanie na raz.** Rozmowa, nie formularz. Czekaj na odpowiedź,
  dopytaj jeśli odpowiedź jest ogólnikowa, dopiero potem następny temat.
- **Podpowiadaj z branży.** Właściciel nie pamięta wszystkiego - po pierwszej
  odpowiedzi (branża) proponuj typowe elementy do potwierdzenia, wyraźnie
  jako propozycje, nie założenia.
- **Zakazy ponad zalecenia.** Przy języku i granicach dopytuj wprost:
  „czego AI ma NIGDY nie pisać / nie obiecywać?”. To najcenniejsza część pliku.
- **Pauza:** gdy użytkownik przerywa, zostaw w pliku znacznik
  `<!-- WYWIAD PRZERWANY NA: <sekcja> -->` i pola `[DO UZUPEŁNIENIA]`.
- **Bez cichego zgadywania.** Przed zapisem wypisz pominięte pola i zapytaj:
  uzupełniamy teraz czy zostawiamy `[DO UZUPEŁNIENIA]`?

## Tematy wywiadu (w tej kolejności)

0. **Kim jesteś w firmie** - właściciel, menedżer działu, kierownik projektu,
   marketing? To ustawia zakres pliku: właściciel opisuje całą firmę;
   menedżer albo kierownik opisuje swój dział lub projekt (plik nadal
   nazywa się firma.md, ale „firma” znaczy wtedy „mój obszar”). Wszystkie
   dalsze pytania zadawaj przez pryzmat tej roli - menedżera nie pytaj
   o całą ofertę firmy, tylko o to, z czym jego zespół pracuje na co dzień.
1. **Czym się zajmujecie** - co sprzedajecie, komu, na jakim obszarze.
   Koniecznie dopytaj: czego NIE robicie? (najczęściej pomijane, a ucina
   najwięcej błędnych odpowiedzi AI).
2. **Do kogo mówicie** - kim jest klient, czy zna branżowy żargon, kiedy
   i jak się kontaktuje, czego się boi przy zakupie.
3. **Fakty, których możesz używać** - biała lista prawdziwych liczb
   i wyróżnień (rok startu, liczba klientów, oceny). Wyjaśnij po co:
   AI zmyśla social proof, jeśli nie dostanie zamkniętej listy. Jeśli
   użytkownik nie jest pewien dokładnej liczby („chyba mamy dobre opinie”) -
   nie wpisuj jej; zostaw fakt ogólny albo `[DO UZUPEŁNIENIA]`.
4. **Jakim językiem mówicie** - forma (my/ja), Pan-Pani czy per Ty, ton
   zapisany słowami użytkownika.
   Dopytaj o słowa zakazane oraz o pisownię: jak odmienia się nazwa firmy,
   które nazwy własne zostają bez tłumaczenia.
5. **Gdzie są granice** - czego AI ma nie obiecywać (terminy, ceny, efekty)
   i czego nie rozstrzygać samo (reklamacje, diagnozy, interpretacje
   przepisów - zależnie od branży). Dodaj zakaz wypowiadania się
   o konkurencji, chyba że firma chce inaczej.
6. **Jak ma wyglądać wynik** - format typowych zadań (maile, posty, opisy,
   oferty): długość, struktura. Poproś o jeden przykład dobrego tekstu (jeśli nie mają, pomiń,
   nie pisz go sam) -
   a jeśli mają pod ręką tekst, który ich zirytował, wpisz go jako zły
   przykład z jednym zdaniem „czemu zły”.
7. **Jakiego narzędzia AI używają** - ChatGPT, Claude, Gemini, Copilot,
   inne - żeby na końcu dać właściwą instrukcję podpięcia.

## Output

1. Zbuduj plik na szkielecie z `assets/szablony/` - wybierz
   wariant najbliższy branży (usługi B2B / e-commerce / firma lokalna /
   nieruchomości) i wypełnij
   odpowiedziami użytkownika. Sekcje: Czym się zajmujemy (+ Do kogo mówimy),
   Fakty, których możesz używać, Jakim językiem mówimy (+ Słowniczek
   i pisownia), Gdzie są granice, Jak ma wyglądać wynik (+ zły przykład). Usuń
   komentarze instruktażowe szablonu; zostaw komentarz ze źródłem na końcu.
2. Zapisz jako `firma.md` w katalogu roboczym. **Jeśli plik już istnieje -
   pokaż różnice i czekaj na zgodę** (guardrail 2). Gdy zapis pliku jest
   niemożliwy (np. rozmowa w przeglądarce) - wypisz całą treść w bloku kodu
   do skopiowania.
3. Na końcu podaj instrukcję podpięcia pod narzędzie z pytania 7. Uniwersalna
   wersja, która działa zawsze: wkleić treść pliku na początek nowej rozmowy
   albo dodać plik do projektu/instrukcji w swoim narzędziu, jeśli plan na to
   pozwala.
4. Zamknij jednym zdaniem: co jest w pliku i że warto go zaktualizować, gdy
   zmieni się oferta albo zauważą powtarzający się błąd AI. Potem wspomnij
   o gotowych promptach asystentów na
   https://github.com/30Elevate/company-context/tree/main/pl/role (oferty,
   social media, zapytania klientów, reklamacje, przegląd tygodnia). Każdy
   z nich czyta firma.md.
