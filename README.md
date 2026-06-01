# SupertrendATR DP LONG

Skrypt rozszerza możliwości klasycznego wskaźnika Supertrend, wprowadzając autorską korektę opartą o zmienność (ATR) oraz analizę wielointerwałową (Multi-Timeframe - MTF). Skrypt został zaprojektowany z myślą o wychwytywaniu i prowadzaniu pozycji wzrostowych (Long).

---

## 📌 Główne funkcje

* **Skorygowany Supertrend:** Oprócz standardowej linii Supertrend, algorytm oblicza drugą linię skorygowaną o bieżącą wartość Average True Range (ATR), tworząc dynamiczny bufor cenowy.
* **Analiza MTF (Multi-Timeframe):** Możliwość jednoczesnego śledzenia trendu na bieżącym wykresie oraz na wyższym interwale czasowym bez konieczności zmiany okna wykresu.
* **Wizualizacja trendu:** Dynamiczne wypełnienie tła (chmury) pomiędzy ceną a skorygowanymi liniami trendu, ułatwiające szybką identyfikację sentymentu.
* **Powiadomienia na wykresie:** Etykiety ze strzałkami wskazujące dokładne momenty odwrócenia trendu.

---

## ⚙️ Logika strategii

Algorytm działa w trybie **Long-Only** i opiera swoje wejścia oraz wyjścia na relacji ceny do dwóch różnych wariantów linii Supertrend:

* **Wejście (Long Entry):** Następuje w momencie, gdy zdefiniowane źródło ceny (domyślnie `close`) przecina od dołu w górę (crossover) bazową linię **oryginalnego** Supertrendu pierwszego interwału.
* **Wyjście (Close Entry):** Następuje, gdy cena przecina od góry w dół (crossunder) **skorygowaną** linię Supertrendu (Adjusted Supertrend) pierwszego interwału.

---

## 🛠 Konfiguracja parametrów

Skrypt oferuje elastyczne zarządzanie ustawieniami z poziomu interfejsu TradingView:

| Parametr | Zastosowanie |
| :--- | :--- |
| **Factor / Factor 2** | Mnożnik określający czułość wskaźnika Supertrend dla pierwszego i drugiego interwału. |
| **ATR Period / ATR Period 2** | Okres historyczny brany pod uwagę przy kalkulacji standardowego ATR wbudowanego w Supertrend. |
| **ATR ST** | Niezależny okres ATR wykorzystywany wyłącznie do przesunięcia (korekty) linii Supertrend. |
| **Timeframe 2** | Wybór dodatkowego, wyższego interwału czasowego do renderowania drugiego układu wskaźników. |
| **Source Long / Exit** | Definicja danych cenowych (np. `close`, `hl2`) wykorzystywanych jako wyzwalacze zdarzeń dla wejść i wyjść. |

W zakładce *Appearance* można w pełni spersonalizować kolory hossy i bessy, które automatycznie zaktualizują wykresy, wypełnienia oraz etykiety.

---

## 🚀 Instrukcja instalacji

1. Skopiuj całą zawartość pliku ze skryptem (od `//@version=5` aż do samego końca).
2. Zaloguj się na platformę [TradingView](https://www.tradingview.com/).
3. Otwórz wybrany wykres cenowy.
4. W dolnym panelu znajdź zakładkę **Pine Editor**.
5. Wklej skopiowany kod w miejsce istniejącego, zastępując go w całości.
6. Kliknij przycisk **Add to Chart** (Dodaj do wykresu) lub zapisz skrypt na swoim koncie (Save).

---

> **Zastrzeżenie:** Powyższy skrypt został udostępniony wyłącznie w celach edukacyjnych i analitycznych. Nie stanowi on porady inwestycyjnej ani rekomendacji do otwierania rzeczywistych pozycji na rynkach finansowych. Przed użyciem jakiejkolwiek strategii na prawdziwych środkach, zaleca się rzetelne testy historyczne (backtesting) oraz grę na koncie demonstracyjnym (paper trading).
