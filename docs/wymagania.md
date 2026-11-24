# Wymagania (od użytkownika, 2026-11-24)

Źródło prawdy dla specyfikacji. Kolejne decyzje trafią do `CONTEXT.md` i ADR-ów, jeśli powstaną w trakcie `/grill-with-docs`.

## Funkcje

1. **Wejście.** Skill czyta wątek mailowy albo dostaje instrukcję, co użytkownik chce napisać.
2. **Dobór stylu.** Skill określa, jaki styl komunikacji będzie w danej sytuacji najlepszy i dlaczego. Zawsze podaje **dwie opcje** do wyboru.
3. **Głos autora.** Skill pisze maila stylem użytkownika, na podstawie jego wcześniejszych maili.
4. **Szkic.** Skill tworzy szkic maila.

## Decyzje

- **Szkic osobno od rozmowy (2026-11-24).** Gotowy mail powstaje w osobnym oknie, czyli jako osobny plik lub artefakt do skopiowania. Nigdy w środku odpowiedzi. Analiza, opcje stylu i „dlaczego” zostają w odpowiedzi. W oknie szkicu jest **tylko treść maila**: bez tematu i bez komentarzy, żeby przy kopiowaniu nie wkleić czegoś niepoprawnego. Ewentualny proponowany temat trafia do odpowiedzi w rozmowie.

## Kontekst

- Użytkownik: lider OPEX w zakładzie motoryzacyjnym (centrala we Francji). Pisze po polsku, czasem po angielsku.
- Platforma: Claude, czyli claude.ai i Claude Code (Agent Skills).
- Materiał źródłowy: stary Gem „God Mode / Shadow” w [`legacy/gem-god-mode-shadow.md`](legacy/gem-god-mode-shadow.md). Badanie ma ocenić, co z niego warto przenieść.

## Do ustalenia

- Skąd brać wcześniejsze maile użytkownika i jak je anonimizować.
- Czy skill ma tworzyć szkic w Gmailu, czy tylko tekst do skopiowania.
- Polski i angielski czy tylko polski.
- Czy objaśnienia zmian mają się pokazywać domyślnie, czy na życzenie.
