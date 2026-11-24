# AGENTS.md

Repo z specyfikacją i kodem skilla Claude do pisania maili biznesowych po polsku. Skill czyta wątek, dobiera styl (dwie opcje), pisze głosem autora i robi szkic. Wymagania: `docs/wymagania.md`. Badania: `docs/research/`.

**Prywatność:** repo jest publiczne. Nigdy nie commituj prawdziwych maili, nazwisk ani danych dostawców i klientów. Przykładowe maile muszą być zanonimizowane. Wyjątek: profil głosu autora może być w repo jako przykładowy, ale bez cytatów z prawdziwych maili.

## Agent skills

### Issue tracker

Issues żyją w GitHub Issues repo `CzubekxD/better_communcattion_skill` (gh CLI; w chmurze REST przez `gh api`). See `docs/agents/issue-tracker.md`.

### Triage labels

Domyślne etykiety: `needs-triage`, `needs-info`, `ready-for-agent`, `ready-for-human`, `wontfix`. See `docs/agents/triage-labels.md`.

### Domain docs

Single-context: jeden `CONTEXT.md` i `docs/adr/` w katalogu głównym. See `docs/agents/domain.md`.
