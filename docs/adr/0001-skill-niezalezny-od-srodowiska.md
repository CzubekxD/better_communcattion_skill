# Jeden SKILL.md dla Claude i Gemini

Skill ma działać tam, gdzie zostanie wgrany, a docelowe środowiska to Claude (claude.ai, Claude Code) i Gemini (skills w aplikacji Gemini i Workspace). Oba czytają ten sam otwarty format Agent Skills, czyli folder z SKILL.md (YAML frontmatter + Markdown) i plikami pomocniczymi. Dlatego utrzymujemy jeden zestaw plików bez osobnej wersji pod Gemini. Rdzeń nie zakłada konkretnego narzędzia ani konektora: korzysta z nich, gdy środowisko je ma, a w przeciwnym razie przechodzi na tryb tekstowy. Claude jest środowiskiem podstawowym i to na nim testujemy jako pierwszym.

Odrzucone alternatywy: wersja szyta tylko pod claude.ai z konektorem Gmaila (nie przeniosłaby się do Gemini) oraz osobny Gem (Google wygasza Gemy na rzecz skills).
