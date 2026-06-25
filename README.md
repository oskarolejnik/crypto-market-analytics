# 🪙 Crypto Market Analytics

Automatyczny system pobierania i analizy danych rynkowych kryptowalut w czasie rzeczywistym, wykorzystujący **CoinGecko API** oraz bibliotekę **Pandas**.

Projekt pozwala na bieżąco monitorować 50 najważniejszych projektów kryptowalutowych, analizować ich dobowe zmiany procentowe oraz wyciągać kluczowe statystyki rynkowe.

---

## 🚀 Funkcje projektu
* **Live Data Fetching:** Pobieranie aktualnych kursów, kapitalizacji oraz wolumenu bezpośrednio z CoinGecko API.
* **Data Science Workflow:** Konwersja surowego formatu JSON do struktur Pandas DataFrame.
* **Analityka:** Automatyczne wyliczanie statystyk opisowych (`.describe()`) oraz filtrowanie topowych projektów o największych wzrostach.
* **Security:** Bezpieczne zarządzanie kluczami API za pomocą zmiennych środowiskowych (`.env`).

## 🗺️ Plan Rozwoju (Roadmap)
Projekt jest stale rozwijany. W najbliższych krokach planowane jest wdrożenie następujących modułów:
1. **Datalake & History Storage:** Automatyczny eksport pobranych danych do lokalnych plików `.csv` z timestampem, umożliwiający budowanie własnej, historycznej bazy danych rynkowych.
2. **Data Visualization:** Implementacja bibliotek `matplotlib` oraz `seaborn` w celu generowania automatycznych wykresów (np. wykresy słupkowe top 10 giełdowych liderów, wykresy kołowe udziału w rynku).
3. **Correlation Analysis:** Analiza statystyczna sprawdzająca zależności między wolumenem obrotu a zmiennością ceny (szukanie anomalii rynkowych).
4. **Alert System:** Prosty moduł powiadomień, który flaguje kryptowaluty notujące nagłe skoki wolumenu lub ceny powyżej ustalonego progu (np. >15% w 24h).

## 🛠️ Technologia i biblioteki
* **Python** (v3.x)
* **Pandas** – analiza danych i operacje na tabelach
* **Requests** – komunikacja z API HTTP
* **Python-dotenv** – bezpieczne zarządzanie kluczami

## 💻 Jak uruchomić projekt lokalnie

1. Sklonuj repozytorium:
   ```bash
   git clone [https://github.com/oskarolejnik/crypto-market-analytics.git](https://github.com/oskarolejnik/crypto-market-analytics.git)
