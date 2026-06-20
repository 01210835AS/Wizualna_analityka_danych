# Wizualna_analityka_danych
W repozytorium przechowywane są syntetycznie wygenerowane zbiory danych, wykorzystane do obliczeń, przetwarzania danych oraz przygotowania wizualizacji przedstawionych w pracy.

# Analiza AS Dataset

To repozytorium zawiera analizę eksploracyjną pliku `AS Dataset.xlsx`, który przedstawia dane supply-chain oraz inventory planning dla asortymentu biżuterii. Dataset obejmuje informacje o produktach, dostępności, brakach ilościowych, forecastach, poziomach zapasu oraz możliwościach transferów regionalnych.

## Opis datasetu

Plik Excel zawiera dane operacyjne i planistyczne dla **1 000 unikalnych SKU**. Dane dotyczą produktów z różnych rodzin, typów biżuterii, krajów pochodzenia, faz produktu oraz statusów związanych z dostępnością i opóźnieniami w łańcuchu dostaw.

Dataset może być wykorzystany do analizy:

- dostępności produktów,
- braków ilościowych,
- prognozowanego popytu,
- pokrycia supply względem demand,
- nadwyżek magazynowych,
- opóźnień produkcyjnych lub transportowych,
- transferów zapasu między regionami.

## Struktura pliku

| Arkusz | Opis |
|---|---|
| `Portfolio` | Dane master data produktów, m.in. SKU, rodzina produktu, typ biżuterii, faza produktu, RRP, kraj pochodzenia, opóźnienia i data wycofania |
| `Missing QTY` | Tygodniowe braki ilościowe dla poszczególnych SKU |
| `Weekly Av` | Tygodniowa dostępność produktów w skali od 0 do 1 |
| `Availability Overview` | Podsumowanie demand, supply, availability, missing quantity oraz recovery metrics |
| `Transfer_EU` | Potrzeby transferu IN oraz potencjał transferu OUT dla regionu EU |
| `Transfer_US` | Dane transferowe IN/OUT dla regionu US |
| `Transfer_Asia` | Dane transferowe IN/OUT dla regionu Asia |
| `Transfer_UK` | Dane transferowe IN/OUT dla regionu UK |
| `X. 2026_HC` | Dane planistyczne na 2026 rok w wersji hardcoded |
| `X. 2026_CAL` | Arkusz kalkulacyjny 2026 zawierający formuły i logikę planowania |

## Najważniejsze cechy datasetu

- około **1 000 unikalnych SKU**,
- główna kategoria: **Jewelry**,
- produkty w fazach:
  - `BASIC`,
  - `NEW`,
- główne rodziny produktów:
  - Mythos,
  - Heritage,
  - Fortune Keepers,
  - Secret Garden,
  - Steampunk,
- główne typy biżuterii:
  - Ring,
  - Necklace,
  - Stud Earrings,
  - Bracelet,
  - Drop Earrings,
- kraje pochodzenia produktów:
  - Thailand,
  - China,
  - Vietnam.

## Kontekst biznesowy

Dataset wspiera analizę dostępności produktów oraz optymalizację zapasu pomiędzy regionami. Dane pozwalają identyfikować produkty z niską dostępnością, braki ilościowe, nadwyżki magazynowe oraz możliwości transferów między regionami.

Głównym celem analizy jest ocena, czy dostępny supply pokrywa prognozowany demand oraz które SKU wymagają działań naprawczych, takich jak transfer zapasu lub recovery plan.

## Główne obserwacje

Dataset pokazuje, że całkowity supply jest wyższy niż prognozowany demand, jednak mimo tego występują braki na poziomie konkretnych SKU i regionów. Oznacza to, że głównym problemem biznesowym nie jest wyłącznie ilość zapasu, ale jego właściwa alokacja.

Najważniejsze wnioski:

- średnia dostępność tygodniowa jest ogólnie wysoka,
- część SKU ma bardzo niską dostępność i wymaga priorytetowej analizy,
- niektóre produkty wykazują istotne braki ilościowe w najbliższym horyzoncie planistycznym,
- region EU ma duży potencjał transferu OUT, ale wybrane SKU nadal wymagają transferu IN,
- dane regionalne mogą być wykorzystane do równoważenia zapasu pomiędzy EU, US, Asia i UK,
- arkusze 2026 zawierają szczegółową logikę demand, supply, availability i transferów.

## Możliwe obszary analizy

Na podstawie datasetu można przygotować analizy dotyczące:

- eksploracyjnej analizy danych,
- monitorowania dostępności SKU,
- identyfikacji braków ilościowych,
- analizy overstocku,
- analizy transferów regionalnych,
- porównania forecastu z supply,
- oceny wpływu opóźnień,
- segmentacji produktów według ryzyka,
- przygotowania dashboardu operacyjnego,
- kontroli jakości danych.

