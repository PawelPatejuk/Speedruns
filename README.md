
# 🏆 Wizualizacja danych — Speedrun.com

## 📖 Opis projektu


Projekt ma na celu analizę i wizualizację danych z platformy [Speedrun.com](https://www.speedrun.com). Dzięki temu możemy:

-   Śledzić zmiany rekordowych czasów w wybranych grach w czasie ⏱️
    
-   Porównać osiągnięcia speedrunnerów z różnych krajów 🌐
    
-   Zidentyfikować najpopularniejsze tytuły i kategorie w społeczności 🎯
    
-   Porównać platformy (PC, konsola, mobilne) pod kątem aktywności speedrunnerów 💻🎮📱
    

W efekcie powstają interaktywne i statyczne wykresy, które ukazują dynamikę i różnorodność świata speedrunningu.

## 🧰 Technologia i zależności

Projekt oparty jest na notebooku Jupyter i wykorzystuje następujące biblioteki Python:

-  `opendatasets` – umożliwia pobieranie zestawów danych z Kaggle i innych źródeł.

-  `pandas` – potężna biblioteka do analizy i manipulacji danymi, używana w data science.

-  `pycountry` – zawiera informacje o krajach, językach i walutach zgodnie z międzynarodowymi standardami.

-  `dash` – framework do tworzenia interaktywnych aplikacji webowych opartych na Pythonie.

-  `jupyter_dash` – pozwala na uruchamianie aplikacji Dash bezpośrednio w notatnikach Jupyter.

-  `pyngrok` – ułatwia publikację aplikacji lokalnych w internecie za pomocą Ngrok.

-  `ydata-profiling[notebook]` – narzędzie do automatycznego eksploracyjnego raportowania dla Pandas DataFrame’ów. Generuje interaktywny raport HTML/iframe.

    

## 🏃‍♂️ Jak uruchomić

1.  Uruchom Jupyter Notebook:
    
    ```
    jupyter notebook
    ```
    
2.  Otwórz plik `Speedruns.ipynb` i wykonaj komórki kolejno od początku.
    
3.  W razie potrzeby dostosuj parametry w sekcji ładowania danych (np. wybrane gry, liczba rekordów).

4. W przypadku interakcji z dashboardami:
    
    -   Załóż darmowe konto w serwisie Ngrok ([ngrok.com](https://ngrok.com))
        
    -   W notebooku wpisz:
    
    ```
    ngrok.set_auth_token("<YOUR_TOKEN>")
    ```
    

## 🗂️ Struktura plików

```
grupa 16 Speedruns/
├── Speedruns.ipynb     # Główny notebook z analizą i wykresami
└── README.md           # Ten plik z instrukcją
```

## 🔗 Źródło danych

Dane pobierane są za pomocą publicznego API Speedrun.com:

```
https://www.speedrun.com/api/v1/
```

oraz z Kaggle.com:

```
https://www.kaggle.com/datasets/alexmerren1/speedrun-com-data
```

Możesz dostosować zapytania pod kątem interesujących Cię gier lub kategorii.

## 📈 Zawartość analizy

1.  🌎 **Użytkownicy serwisu** — analiza liczby aktywnych speedrunnerów, rozkładu geograficznego oraz demografii (kraj, poziom zaawansowania, liczba przesłanych rekordów). Pozwala zrozumieć profil i wzrost społeczności.
    
2.  🎮 **Najpopularniejsze gry** — ranking tytułów według liczby rekordów i aktywnych użytkowników. Wykresy słupkowe i kołowe prezentują, które gry cieszą się największym zainteresowaniem.
    
3.  🎮 **Szczegółowa analiza danej gry** — dla wybranego tytułu badamy historię rekordów, kluczowe kamienie milowe, najaktywniejszych graczy oraz różnice między kategoriami gry (np. any%, 100%).
    
4.  ⌛ **Speedruny — rozkład według lat, miesięcy i dni tygodnia** — wizualizacja liczby wykonanych speedrunów w podziale na lata, miesiące oraz dni tygodnia, co pomaga zidentyfikować sezonowe i tygodniowe wzorce aktywności.
    
5.  🕹️ **Porównanie platform** — zestawienie aktywności speedrunnerów na różnych platformach (PC, konsole, urządzenia mobilne) wraz z oceną średnich wyników i dynamiki rozwoju dla każdej z nich.
    
6.  💼 **Deweloperzy gier** — analiza wpływu wydawców i deweloperów na społeczność speedrun; liczba rekordów dla tytułów poszczególnych firm oraz identyfikacja najbardziej „speedrunowych” studiów.
