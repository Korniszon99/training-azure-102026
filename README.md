# Szkolenie Azure / DevOps — 10.2026

Centralne repozytorium szkolenia Komisji Cyfryzacji SSPW poświęconego wdrażaniu prostej aplikacji Node.js do Azure z użyciem GitHub Actions.

To repo **nie zawiera gotowego workflow deploymentowego**. Celem szkolenia jest samodzielne zbudowanie procesu CI/CD przez uczestników.

## Jak pracujemy

Każdy uczestnik tworzy własne repozytorium w organizacji `kc-sspw`.

Proponowana nazwa:

`training-azure-102026-<github-login>`

Przykład:

`training-azure-102026-korniszon99`

Repozytoria uczestników mogą mieć prosty workflow:

- praca bezpośrednio na `main`,
- bez obowiązkowego code review,
- bez obowiązkowych Pull Requestów,
- nacisk na samodzielne tworzenie GitHub Actions,
- żadnych prawdziwych sekretów w kodzie ani historii Git.

## Co przechowujemy tutaj

To repo służy jako:

- indeks repozytoriów uczestników,
- miejsce na krótkie podsumowania wykonanych wdrożeń,
- archiwum finalnych workflowów po zakończeniu szkolenia,
- dokumentacja organizacyjna danej edycji.

Struktura:

- [participants/](participants/) — wpisy uczestników,
- [archive/](archive/) — finalne artefakty po szkoleniu,
- [organizer-checklist.md](organizer-checklist.md) — checklista dla prowadzących.

## Po szkoleniu

Repozytorium uczestnika może zostać zarchiwizowane w GitHubie. W tym repo zachowujemy wtedy:

- link do repozytorium,
- krótki opis serwisu,
- link lub opis docelowego wdrożenia,
- finalny workflow GitHub Actions napisany przez uczestnika,
- najważniejsze wnioski z ćwiczenia.

Dzięki temu każda edycja szkolenia pozostaje samodzielnym, czytelnym archiwum.
