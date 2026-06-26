# 🪙 Crypto Market Analytics

![Python](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)
![CoinGecko](https://img.shields.io/badge/CoinGecko%20API-8DC63F?style=flat-square)

System pobierania i analizy danych rynkowych kryptowalut w Pythonie, wykorzystujący **CoinGecko API** oraz bibliotekę **Pandas**.

Projekt pobiera na żądanie 50 największych kryptowalut, liczy kluczowe statystyki rynkowe i wizualizuje liderów wzrostów — całość w notebooku Jupyter (`analysis.ipynb`).

---

## 🚀 Co robi projekt (aktualny stan)

* **Pobieranie danych na żywo:** aktualne kursy, kapitalizacja i wolumen top-50 prosto z CoinGecko API (endpoint `coins/markets`).
* **Data Science Workflow:** konwersja odpowiedzi JSON do `pandas.DataFrame`.
* **Analityka:** łączna kapitalizacja top-50, statystyki opisowe (`.describe()`) oraz ranking 5 największych wzrostów w 24h.
* **Wizualizacja:** wykres słupkowy top-5 wzrostów (`matplotlib`).
* **Eksport:** każde uruchomienie zapisuje snapshot do pliku `.csv` z sygnaturą czasową.
* **Bezpieczeństwo:** klucz API ładowany ze zmiennej środowiskowej (`.env`, `python-dotenv`) — nie trafia do repozytorium.

## 🗺️ Plan rozwoju (Roadmap)

1. **Historia / Datalake:** automatyczne gromadzenie kolejnych snapshotów `.csv` w spójną, historyczną bazę danych rynkowych.
2. **Rozszerzona wizualizacja:** `seaborn` + dodatkowe wykresy (udział w rynku, wykresy kołowe, serie czasowe).
3. **Analiza korelacji:** zależności między wolumenem a zmiennością ceny (szukanie anomalii rynkowych).
4. **System alertów:** flagowanie nagłych skoków ceny lub wolumenu powyżej zadanego progu (np. >15% / 24h).

## 🛠️ Technologia i biblioteki

* **Python** (3.x)
* **Pandas** — analiza danych i operacje na tabelach
* **Requests** — komunikacja z API HTTP
* **Matplotlib** — wizualizacja danych
* **python-dotenv** — bezpieczne zarządzanie kluczami API

## 💻 Jak uruchomić lokalnie

1. Sklonuj repozytorium:
   ```bash
   git clone https://github.com/oskarolejnik/crypto-market-analytics.git
   cd crypto-market-analytics
   ```

2. Zainstaluj zależności:
   ```bash
   pip install pandas requests python-dotenv matplotlib jupyter
   ```

3. Skonfiguruj klucz API — utwórz plik `.env` w katalogu projektu:
   ```env
   COINGECKO_API_KEY=twoj_klucz_api
   ```

4. Uruchom notebook:
   ```bash
   jupyter notebook analysis.ipynb
   ```

---

> Projekt portfolio / nauka analizy danych. Dane pochodzą z [CoinGecko](https://www.coingecko.com/) i służą wyłącznie celom edukacyjnym — to nie jest porada inwestycyjna.
