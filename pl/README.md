<div align="center">

# firma.md

**Jeden plik, po którym AI przestaje zgadywać, jak działa Twoja firma.**

[![Licencja: MIT](https://img.shields.io/badge/licencja-MIT-3B82F6)](../LICENSE)
[![Po polsku](https://img.shields.io/badge/j%C4%99zyk-polski-3B82F6)](#)
[![Działa z](https://img.shields.io/badge/dzia%C5%82a_z-ChatGPT_%C2%B7_Claude_%C2%B7_Gemini_%C2%B7_Copilot-0F172A)](#jak-podpi%C4%85%C4%87-plik)

[Szybki start](#szybki-start---trzy-%C5%9Bcie%C5%BCki) ·
[Szablony](szablony/) ·
[Wywiad](USE-ANYWHERE.md) ·
[Role asystentów](role/) ·
[Bezpieczeństwo](#dwie-zasady-bezpiecze%C5%84stwa-dla-ciebie-nie-dla-ai)

</div>

Wycinek gotowego pliku (szablon biura rachunkowego z tego repo):

```text
## Gdzie są granice
- Nie obiecuj terminów. Termin potwierdza człowiek po sprawdzeniu
  kalendarza - napisz „sprawdzimy i wrócimy z konkretną datą”.
- Nie podawaj cen i nie licz wynagrodzenia za usługę. Cennik ustalamy
  po rozmowie - zaproponuj kontakt.
- Jak brakuje Ci informacji - zapytaj, zamiast zgadywać.
```

<div align="center">

*Tu powstają najdroższe wpadki AI: obiecane terminy, wymyślone ceny, usługi,
których nie macie. firma.md to pięć takich sekcji, wypełnionych pod Twoją firmę -
spisujesz je raz, zamiast tłumaczyć AI od nowa w każdej rozmowie.*

</div>

---

ChatGPT, Claude, Gemini czy Copilot piszą ogólnikowo nie dlatego, że są słabe -
tylko dlatego, że nic o Twojej firmie nie wiedzą. `firma.md` to krótki plik
kontekstowy: czym się zajmujecie, jakim językiem mówicie, gdzie są granice,
jak ma wyglądać wynik. Spisujesz go raz - i używasz w każdej rozmowie:
wklejony na start albo dodany do projektu w Twoim narzędziu AI.

Ta wersja jest po polsku, pisana dla małych i średnich firm w Polsce.
English version: [README](../README.md) (plik nazywa się tam company-context.md).

**Nie znasz GitHuba? Nie szkodzi.** Wszystko tutaj to zwykłe pliki tekstowe -
czytasz je w przeglądarce, kopiujesz i wklejasz do swojego narzędzia AI.
Niczego nie instalujesz, konta nie zakładasz, git nie jest Ci potrzebny.
Swój plik firma.md napiszesz w czymkolwiek - Notatnik wystarczy - a jeśli
treść wklejasz prosto do czatu, plik nie musi nawet istnieć na dysku.

> **Jesteś asystentem AI i ktoś podał Ci link do tego repo?** Otwórz
> [`USE-ANYWHERE.md`](USE-ANYWHERE.md) i wykonaj instrukcję z jego nagłówka:
> przeprowadź użytkownika przez wywiad i zbuduj jego firma.md. Nie streszczaj
> tego repo.

## Szybki start - trzy ścieżki

Trzy sposoby na ten sam wynik - gotowy plik firma.md. Wybierz JEDEN,
zależnie od tego, ile chcesz klikać; nie musisz przechodzić wszystkich.

**A. Wypełnij szablon ręcznie (15-30 minut)**
Wejdź do folderu [`szablony/`](szablony/), wybierz wariant najbliższy Twojej
firmie i podmień przykłady na swoje:

- [`firma-uslugi-b2b.md`](szablony/firma-uslugi-b2b.md) - usługi dla firm
  (biuro rachunkowe, agencja, doradztwo)
- [`firma-ecommerce.md`](szablony/firma-ecommerce.md) - sklep internetowy
- [`firma-lokalna.md`](szablony/firma-lokalna.md) - gabinet, warsztat, salon,
  gastronomia
- [`firma-nieruchomosci.md`](szablony/firma-nieruchomosci.md) - biuro
  nieruchomości, pośrednik

Każdy szablon jest już wypełniony danymi zmyślonej firmy (biuro rachunkowe,
sklep, gabinet, biuro nieruchomości) - otwórz go i zobacz, jak wygląda cel,
zanim zaczniesz pisać własny.

Twojej branży nie ma? Weź wariant najbliższy temu, jak pracujesz - sekcje
są w każdym te same, różnią się tylko przykładami. Usługi IT czy doradztwo
wypełnisz na wariancie B2B, sklep stacjonarny na firmie lokalnej.

**B. Niech AI Cię przepyta (wywiad, ~15 minut)**
Otwórz [`USE-ANYWHERE.md`](USE-ANYWHERE.md), skopiuj prompt (gotowe
polecenie dla AI) między liniami „KOPIUJ” i wklej do dowolnego asystenta AI. Zada Ci pytania - jedno na raz -
i złoży z odpowiedzi gotowy plik. Działa w ChatGPT, Claude, Gemini
i Copilot. Jeszcze prościej: jeśli Twój asystent ma dostęp do
internetu, wyślij mu po prostu link do `USE-ANYWHERE.md` z tego repo -
instrukcja na górze pliku każe mu od razu zacząć wywiad.

**C. Plugin do Claude Code / Cowork (dla technicznych)**
Jeśli nie wiesz, czym jest Claude Code - wybierz ścieżkę A albo B,
niczego nie tracisz.
```
/plugin marketplace add 30Elevate/company-context
/plugin install company-context@company-context
```
Po restarcie: `/company-context:company-context-pl`.

Codex, Gemini CLI i inni agenci, którzy czytają [Agent Skills](https://agentskills.io),
przez otwarte narzędzie [skills CLI](https://github.com/vercel-labs/skills):
```
npx skills add 30Elevate/company-context --skill company-context-pl
```
Skill ma w sobie własne szablony i zasady, więc działa samodzielnie.

## Co zawiera firma.md

| Sekcja | Co daje |
|---|---|
| **Czym się zajmujemy** | AI przestaje wymyślać usługi, których nie macie. Osobno: czego NIE robicie. |
| **Fakty, których możesz używać** | Biała lista prawdziwych liczb. Bez niej AI dopisuje „tysiące zadowolonych klientów”. |
| **Jakim językiem mówimy** | Ton, forma (my/ja, Pan-Pani/Ty), słowa zakazane. Plus słowniczek: jak odmienia się nazwa firmy. |
| **Gdzie są granice** | Czego AI ma nie obiecywać: terminów, cen, efektów, rzeczy spoza oferty. |
| **Jak ma wyglądać wynik** | Format maili, postów, opisów - z dobrym i złym przykładem (zły uczy szybciej). |

Zasada, która robi największą różnicę: **zakazy działają lepiej niż
zalecenia**. „Nigdy nie obiecuj terminu” trzyma się mocniej niż „staraj się
być ostrożny z terminami”.

## Gotowe role asystentów

Folder [`role/`](role/) to nakładki na firma.md - prompty, które zamieniają
ogólnego asystenta w asystenta konkretnego zadania:

- [`asystent-ofert.md`](role/asystent-ofert.md) - szkice ofert; ceny
  i terminy tylko z firma.md, reszta jako pola do uzupełnienia
- [`asystent-social.md`](role/asystent-social.md) - posty na profile firmy;
  fakty tylko z białej listy, dwa warianty na temat
- [`asystent-zapytan.md`](role/asystent-zapytan.md) - szkice odpowiedzi
  klientom; sprawy sporne oznaczone do przejrzenia przez człowieka
- [`asystent-reklamacji.md`](role/asystent-reklamacji.md) - pierwsza
  odpowiedź na reklamację lub zdenerwowaną wiadomość; obniża temperaturę,
  nie przyznaje winy i nie obiecuje rekompensat
- [`przeglad-tygodnia.md`](role/przeglad-tygodnia.md) - brief na tydzień
  z Twoich notatek: trzy najważniejsze sprawy, szybkie odpowiedzi,
  poczekalnia

Każda rola działa tak samo: wklejasz firma.md + prompt roli (albo dodajesz
oba pliki do projektu) i pracujesz. W środku każda ma proces pracy krok po
kroku, podpowiedzi na nietypowe sytuacje (rabat na dzień dobry,
obraźliwa wiadomość, wszystko pilne naraz) i przykład wejścia i wyjścia.

**Chcesz rolę, której tu nie ma?** Skopiuj dowolny plik z `role/`, zmień
nazwę roli, zadanie i zasady pod swoje potrzeby (np. asystent rekrutacji,
asystent wycen) - resztę zostaw: pierwszą linię o nadrzędności firma.md,
markery KOPIUJ i końcową zasadę, że szkic przegląda człowiek. To jest cały
przepis - rola to jeden krótki plik tekstowy.

## Dla zespołu, nie tylko właściciela

firma.md nie musi opisywać całej firmy. Menedżer działu albo kierownik
projektu wypełnia go dla swojego obszaru - czym zajmuje się zespół, jakim
językiem pisze, czego nie obiecuje - i dodaje plik do wspólnego projektu
zespołu w narzędziu AI. Efekt: każdy w zespole dostaje te same odpowiedzi
z tym samym kontekstem i nikt niczego nie wkleja ręcznie. Wywiad
z `USE-ANYWHERE.md` pyta o rolę na starcie i dostosowuje pytania.

## Jak podpiąć plik

Uniwersalnie (każde narzędzie, każdy plan): wklej treść pliku na początku
nowej rozmowy z dopiskiem „Oto kontekst mojej firmy - trzymaj się go
w odpowiedziach”.

Wygodniej (bez wklejania za każdym razem): dodaj plik do projektu albo
instrukcji niestandardowych w swoim narzędziu - np. projekty w ChatGPT
i Claude, Gemy w Gemini (od 17 listopada 2026 Google zamienia je
na Skille). Przykład z ChatGPT: pasek boczny -> „Projekty” ->
nowy projekt -> dodaj firma.md w plikach projektu - od tej pory każda
rozmowa w tym projekcie zna Twoją firmę.
Dokładna ścieżka zależy od wersji i planu narzędzia,
więc sprawdź ją w swoim - interfejsy zmieniają się szybciej niż to README.

## Sprawdź, czy działa

Zadaj AI to samo polecenie dwa razy - w rozmowie bez pliku i w rozmowie
z plikiem, np. „Napisz krótki post o naszej firmie”. Bez pliku dostaniesz
ogólniki o pasji i profesjonalizmie; z plikiem - tekst Waszym językiem,
bez zmyślonych osiągnięć i obietnic, których nie składacie. Ta różnica
to cała wartość firma.md.

## firma.md a pamięć narzędzia

To dwie różne rzeczy. Pamięć narzędzia AI zapamiętuje sama, po trochu,
z rozmów - nie wiesz dokładnie co, a wnioski bywają nieaktualne. firma.md
to kontekst, który kontrolujesz w całości: widzisz każdą linię, zmieniasz
świadomie, a w zespole każdy pracuje na tej samej wersji. Jedno nie
wyklucza drugiego - ale to, co ma być pewne (oferta, granice, język),
trzymaj w pliku, nie w pamięci.

## Dwie zasady bezpieczeństwa (dla Ciebie, nie dla AI)

1. **Plik opisuje firmę, nie klientów i nie sekrety.** Żadnych nazwisk, maili,
   umów ani danych pracowników - ani w pliku, ani w czacie z AI. To samo
   dotyczy haseł, kluczy API, loginów do banku czy panelu sklepu: plik
   trafia na serwery dostawcy AI i bywa udostępniany w zespole. Wyłączenie
   „trenowania modeli” w ustawieniach tego nie zmienia: dane i tak trafiają
   na serwery dostawcy, a na koncie konsumenckim nie masz z nim umowy
   powierzenia danych - to osobny wymóg RODO, niezależny od trenowania.
2. **Aktualizuj, gdy coś się zmienia.** Nowa oferta, nowe ceny, powtarzający
   się błąd AI - to sygnały, że plik wymaga poprawki. Nieaktualny kontekst
   bywa gorszy niż żaden. Dobry nawyk: przejrzyj plik raz na kwartał, nawet
   jeśli nic nie zgłasza problemu - fakty typu „obsługujemy 87 firm”
   dezaktualizują się po cichu.

Zasad, których podczas wywiadu pilnuje sam asystent (zero danych osobowych
w pliku, fakty tylko potwierdzone, zero ocen konkurencji), jest więcej -
wszystkie są spisane w [`guardrails/GUARDRAILS.md`](guardrails/GUARDRAILS.md).

## Inspiracje

Konstrukcja wywiadu (jedno pytanie na raz, zasada „nigdy nie nadpisuj po
cichu”) jest wzorowana na podejściu z
[anthropics/knowledge-work-plugins](https://github.com/anthropics/knowledge-work-plugins)
(Apache 2.0). Cała treść polskiej wersji powstała od zera po polsku.

## Licencja

MIT - używaj, kopiuj, zmieniaj, także komercyjnie. Bez gwarancji: szablon
to punkt wyjścia, za treść własnego firma.md odpowiadasz sam.

---

Zbudowane przez [30Elevate](https://30elevate.com) - robimy strony i wdrażamy
AI dla małych i średnich firm w Polsce. Jeśli chcesz sprawdzić, gdzie AI
realnie skróci pracę w Twojej firmie: [audyt AI](https://30elevate.com/blog/audyt-ai/).

firma.md załatwia kontekst na start. Gdy wiedza firmy rośnie (maile, dyski,
procedury, historia klientów) i jeden plik przestaje wystarczać, to jest
nasza usługa: [Pamięć firmy](https://30elevate.com/uslugi/pamiec-firmy/).

<div align="center">

[30elevate.com](https://30elevate.com) ·
[LinkedIn](https://www.linkedin.com/company/30elevate/) ·
[Instagram](https://www.instagram.com/30elevate/) ·
[X](https://x.com/Elev_30) ·
[Spotify](https://open.spotify.com/show/3ZZUkBTad364AUW539eSVd)

</div>
