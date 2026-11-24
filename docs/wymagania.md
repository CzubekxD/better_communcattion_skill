# Wymagania (od użytkownika, 2026-11-24)

Źródło prawdy dla specyfikacji. Kolejne decyzje trafią do `CONTEXT.md` i ADR-ów, jeśli powstaną w trakcie `/grill-with-docs`.

## Funkcje

1. **Wejście.** Skill czyta wątek mailowy albo dostaje instrukcję, co użytkownik chce napisać.
2. **Dobór stylu.** Skill określa, jaki styl komunikacji będzie w danej sytuacji najlepszy i dlaczego. Zawsze podaje **dwie opcje** do wyboru.
3. **Głos autora.** Skill pisze maila stylem użytkownika, na podstawie jego wcześniejszych maili.
4. **Szkic.** Skill tworzy szkic maila.

## Decyzje

- **Szkic osobno od rozmowy (2026-11-24).** Gotowy mail powstaje w osobnym oknie, czyli jako osobny plik lub artefakt do skopiowania. Nigdy w środku odpowiedzi. Analiza, opcje stylu i „dlaczego” zostają w odpowiedzi. W oknie szkicu jest **tylko treść maila**: bez tematu i bez komentarzy, żeby przy kopiowaniu nie wkleić czegoś niepoprawnego. Ewentualny proponowany temat trafia do odpowiedzi w rozmowie.

- **Środowiska (2026-11-24).** Claude (podstawowe) i Gemini, oba z tego samego SKILL.md. Skill korzysta z narzędzi środowiska, jeśli są, a jeśli nie ma, przechodzi na tryb tekstowy. Zob. ADR 0001.
- **Nazwa (2026-11-24).** `drafting-business-emails`.
- **Katalog frameworków (2026-11-24).** W wersji 1 wszystkie frameworki z raportu 02 poza przeprosinami (Lewicki), czyli 12. Przeprosiny na razie wypadają, bo w mailach do klienta przyznanie winy niesie ryzyko kontraktowe.
- **Profil głosu w repo (2026-11-24).** Profil głosu autora trafia do repo jako przykładowy profil, który inni mogą zastąpić własnym. Prawdziwe maile, z których powstał, do repo nie trafiają.
- **Wejście (2026-11-24).** Wątek wklejony do czatu działa zawsze. Konektor poczty tylko wtedy, gdy środowisko go ma.
- **Zatrzymanie (2026-11-24).** Domyślnie jedno zatrzymanie: analiza i dwie Opcje, użytkownik wybiera, potem Szkic. Słowo „szybko” pomija wybór: pokazuje pełną Tabelę ustaleń i od razu daje Szkic w rekomendowanej Opcji. Jeśli brakuje faktów, skill i tak się zatrzymuje i zadaje Listę braków.
- **Język (2026-11-24).** Szkic powstaje w języku maila, na który odpowiadamy.
- **Opcje (2026-11-24).** Zawsze dwie: Opcja asertywna i Opcja kooperatywna. Przy jednej z nich jest dopisek „(rekomendowana)”. Parę frameworków dla danej intencji skill bierze z tabeli, nie wymyśla jej za każdym razem.
- **Język analizy (2026-11-24).** Na razie analiza i opis Opcji zawsze po polsku.
- **Czy ciągnąć dalej mailem (2026-11-24).** Skill ocenia, czy dalsza wymiana maili ma sens, i podpowiada, co zrobiłby skuteczny menedżer, żeby rozwiązać sprawę (np. telefon, spotkanie, decyzja, eskalacja). Obie Opcje nadal są.
- **Ruch menedżera (2026-11-24).** Sekcja nad Opcjami z werdyktem (ciągnąć mailem / zmienić kanał / zamknąć temat) i 1–2 krokami. Pojawia się tylko przy sygnałach: wątek gorący, 3 lub więcej rund bez postępu, krytyka skierowana do jednej osoby, decyzja poza uprawnieniami autora.
- **Kolejność odpowiedzi (2026-11-24).** 1) Tabela ustaleń, 2) Ruch menedżera (tylko przy sygnałach), 3) Opcja asertywna i Opcja kooperatywna, jedna z dopiskiem „(rekomendowana)”, 4) Lista braków, jeśli czegoś brakuje, 5) pytanie o wybór Opcji. Wszystko w jednym zatrzymaniu.
- **Tabela ustaleń (2026-11-24).** Zawsze pokazywana w całości przed Opcjami, żeby autor mógł potwierdzić, że skill dobrze odczytał wątek. Wrócimy do tego, gdy nabierzemy zaufania do skilla.
- **Brakujące fakty (2026-11-24).** Skill nie wstawia do Szkicu miejsc do uzupełnienia. Przed Szkicem zadaje Listę braków, a Szkic powstaje z odpowiedzi.
- **Pliki ze starego Gema (2026-11-24).** Nie przenosimy celów, archetypów, Scientific Anchors ani dokumentu Shadow: to przerost treści nad formą. Cel odpowiedzi skill wnioskuje sam.
- **Testy (2026-11-24).** Autor testuje skill na swoich prawdziwych mailach we własnym środowisku. Do repo trafiają wyłącznie wyniki (co zadziałało, co nie), nigdy treść maili.
- **Przykłady do Profilu głosu (2026-11-24).** Dochodzą na końcu, jako ostatni etap budowy.
- **Analiza pogłębiona (2026-11-24).** W wersji 1, ale tylko na żądanie. Domyślnie skill robi lekką analizę.

## Kontekst

- Użytkownik: lider OPEX w zakładzie motoryzacyjnym (centrala we Francji). Pisze po polsku, czasem po angielsku.
- Platforma: Claude, czyli claude.ai i Claude Code (Agent Skills).
- Materiał źródłowy: stary Gem „God Mode / Shadow” w [`legacy/gem-god-mode-shadow.md`](legacy/gem-god-mode-shadow.md). Badanie ma ocenić, co z niego warto przenieść.

## Do ustalenia

- Skąd brać wcześniejsze maile użytkownika i jak je anonimizować.
- Czy skill ma tworzyć szkic w Gmailu, czy tylko tekst do skopiowania.
- Polski i angielski czy tylko polski.
- Czy objaśnienia zmian mają się pokazywać domyślnie, czy na życzenie.
