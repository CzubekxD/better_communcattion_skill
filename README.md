# better_communcattion_skill

Skill dla Claude (Agent Skills: claude.ai + Claude Code) do pisania maili biznesowych po polsku. Czyta wątek, dobiera styl komunikacji i pisze szkic głosem autora.

> Status: **specyfikacja w budowie**. Kodu skilla jeszcze nie ma.

## Co skill ma robić

1. **Wejście.** Wczytuje wątek mailowy albo instrukcję użytkownika, co chce napisać.
2. **Dobór stylu.** Wybiera najlepszy styl komunikacji (NVC, BLUF, SBI, DESC, Minto…) i podaje **dwie opcje** z uzasadnieniem.
3. **Głos autora.** Odwzorowuje styl pisania użytkownika na podstawie jego wcześniejszych maili.
4. **Szkic.** Tworzy szkic maila gotowy do edycji i wysłania.

Szczegóły: [`docs/wymagania.md`](docs/wymagania.md).

## Struktura repo

```
docs/
  wymagania.md          # wymagania użytkownika (źródło prawdy)
  research/             # raporty z badań (deep research)
  legacy/               # stary Gem "God Mode / Shadow" — materiał źródłowy do oceny
```

## Badania

| # | Raport | Status |
|---|---|---|
| 01 | [Przegląd gotowych skilli](docs/research/01-przeglad-gotowych-skilli.md) | gotowy |
| 02 | [Dobór stylu komunikacji maila](docs/research/02-dobor-stylu-komunikacji.md) | gotowy |
| 03 | [Ocena starego Gema God Mode / Shadow](docs/research/03-ocena-gema-god-mode-shadow.md) | gotowy |
