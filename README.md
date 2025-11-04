# Analiza Pokrycia Terenu 2014-2020

Projekt służy do automatycznej analizy zmian pokrycia terenu w latach 2014 → 2020 z wykorzystaniem ArcGIS i Pythona.

## Opis

* Tworzenie połączonych warstw dla lat 2014 i 2020 (`PT_2014`, `PT_2020`).
* Tworzenie warstwy przecięcia (`PT_2014_2020`) w celu analizy zmian.
* Analiza zmian na podstawie kodów `X_KOD`.
* Generowanie wykresów:

  * słupkowy (top 15 zmian + inne)
  * kołowy (udział zmian vs brak zmian)
* Zapis wykresów do plików JPG.

## Struktura projektu

```
/arcpy
│   AnalizaPokryciaTerenu.py
│   ImportSHP_do_Geobazy.py
│   README.md
│   .gitignore
│
└───ppa_projekt/ppa/ppa.gdb   # geobaza docelowa
```

## Instrukcja użycia

1. Skopiuj pliki `.shp` do odpowiednich folderów źródłowych (np. `2261_SHP_2020`).
2. Uruchom skrypt `ImportSHP_do_Geobazy.py`, aby wprowadzić shapefile do geobazy.
3. Uruchom `AnalizaPokryciaTerenu.py`, aby wygenerować analizę i wykresy.

## Wymagania

* ArcGIS Pro z ArcPy
* Python 3.x (zgodny z ArcGIS Pro)
* Matplotlib

## Uwagi

* Nie wrzucaj całej geobazy `.gdb` na GitHub (plik jest duży).
* Pliki tymczasowe i cache Pythona są ignorowane dzięki `.gitignore`.
