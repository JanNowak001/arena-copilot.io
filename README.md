# Jednostronicowe CV / Wizytówka Eventu

Ten projekt to prosty one-page (bez przewijania na desktopie) prezentujący CV (przykład: Jan Kowalski). Możesz łatwo podmienić treść na własne dane lub wykorzystać jako stronę promującą wydarzenie (np. Halloween Party).

## Struktura
- `index.html` – semantyczny HTML + mikro-dane schema.org Person
- `styles.css` – stylizacja (motyw Halloween / szkło + neon pomarańczowy)
- `assets/images/profile.jpg` – zdjęcie profilowe (dodaj własne)

## Jak edytować
1. Zmień tytuł i meta opis w `<head>`.
2. Podmień dane osobowe, umiejętności, doświadczenie i linki.
3. Dodaj swoje zdjęcie do `assets/images/profile.jpg` (zastąp plik). Zalecane proporcje kwadrat 600x600.
4. (Opcjonalnie) Zmień kolory w `styles.css` – szukaj `#ff9d42`.

## Uruchomienie lokalne
Otwórz plik `index.html` w przeglądarce (dwuklik). Nie ma zależności ani builda.

## Publikacja na GitHub Pages
1. Utwórz repozytorium na GitHub (jeśli nie istnieje) i dodaj pliki.
2. Commit & push:
```bash
git add .
git commit -m "Initial CV page"
git push origin main
```
3. Wejdź w Settings > Pages.
4. W sekcji Build and deployment wybierz: Source = Deploy from a branch, Branch = `main` / root.
5. Zapisz. Po ~1-2 minutach strona będzie dostępna pod `https://twoj_user.github.io/nazwa-repo/`.

### Custom (darmowa) domena
Możesz podłączyć darmową domenę:
- `eu.org` (formularz + oczekiwanie na akceptację)
- `is-a.dev` / `is-a-good.dev` (pull request w repo, szybka akceptacja)
- `thedev.id` (podobnie przez PR)
- `pp.ua` (darmowe ukraińskie – wymaga dodatkowych kroków)

#### Kroki podłączenia domeny (np. is-a.dev)
1. Fork repozytorium projektu domeny (np. is-a-dev/register).
2. Dodaj plik JSON z nazwą subdomeny i rekordami (A lub CNAME wskazującymi na GitHub Pages). CNAME docelowy: `twoj_user.github.io`.
3. Zrób PR.
4. W swoim repo dodaj plik `CNAME` w root z treścią: `twoja-subdomena.is-a.dev`.
5. W panelu Pages włącz HTTPS po propagacji DNS.

#### Rekordy DNS dla GitHub Pages
Jeśli używasz apex domeny (np. `example.eu.org`):
- A rekordy: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`

Subdomena (np. `cv.example.eu.org`):
- CNAME: `twoj_user.github.io`

## Dostępność (A11y)
- Kontrast kolorów pomarańczowy #ff9d42 na ciemnym tle jest wysoki.
- Fokus dla linków (outline).
- Tekst alternatywny dla zdjęcia.

## Modyfikacja pod Event
Zmień nagłówki:
- Imię → Nazwa Eventu
- Doświadczenie → Agenda / Atrakcje
- Umiejętności → Co oferujemy / prelegenci
- Kontakt → Rejestracja / bilety

## Pomysły na rozbudowę (opcjonalne)
- Dodaj animację wejścia elementów (CSS `@keyframes` / `opacity` + `translateY`).
- Wersje jasna/ciemna (prefers-color-scheme).
- Formularz zapisu (Netlify form / Formspree).

## Licencja
Public Domain / CC0. Możesz kopiować i modyfikować bez ograniczeń.
