# CLAUDE.md for opptatt

Statusvisning («Eg er tilgjengeleg» osv.) for ein iPad utanfor kontoret. Statiske sider utan byggjesteg, publisert på GitHub Pages (https://ghveem.github.io/opptatt/). Sjå README.md for brukarrettleiing.

## Køyring

- Ingen bygg eller avhengigheiter. Opne `index.html` og `innstillingar.html` direkte, eller server mappa, t.d. `python3 -m http.server`
- Deploy: push til `main` trigger `.github/workflows/static.yml` (GitHub Pages)
- Det finst ingen testar

## Struktur

- `index.html`: hovudvisning med statussirkel, overstyring (trykk på sirkelen) og kalenderhenting. All JS og CSS ligg i fila
- `innstillingar.html`: kalender-URL (ICS), standardstatus, tilpassa melding. Opnast med langt trykk (1,5 s) eller via overstyringspanelet
- `CORS_FEILSØKING.md`: notat om feilsøking av kalenderhenting. Delane om automatisk proxy (AllOrigins) er utdaterte, proxyen er fjerna

## Fallgruver

- Alt blir lagra i `localStorage` på eininga (`calendarUrl`, `refreshInterval`, `tilgjenge-override`, `tilgjenge-status`). Endringar på ein annan eining slår ikkje gjennom på iPaden
- ICS-URL-en gir lesetilgang til kalenderen. Ikkje legg han i repoet eller i commit-meldingar
- Det blir ikkje brukt proxy. Kalenderen blir berre henta direkte frå nettlesaren, og ved CORS-feil viser systemet manuell status med varsel. Ikkje legg til tredjepartstenester for henting. Dokumenter endringar her i README.md
- ICS-parsinga handterer gjentakande møte, unntak, flytta forekomstar, avlyste møte og «Ledig». Test med gjentakande møte etter endringar
- Møtetitlar skal aldri visast på skjermen (personvern), berre klokkeslett
- Overstyring går føre kalender, og kalender går føre standardstatus
- Panelet skal fungere i Guided Access på iPad, så unngå funksjonar som krev systemdialogar

## Reglar

- Bruk git med små, tydelege commits, og aldri push direkte til `main`. Bruk eiga grein og PR
- Trygg .gitignore, ingen hemmelegheiter eller tokens i repoet
- Oppdater README.md når noko endrar seg
- Bruk /ndla-brand for UI der det passar. Fargar og utsjånad her følgjer elles Kvinnherad-designet som er beskrive i README.md
- Skriv nynorsk, utan tankestrek, bruk «me» og «K.I.»
- Gjer berre det som er bede om, kvar endra linje skal følgje av oppgåva
