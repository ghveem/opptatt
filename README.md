# Tilgjengeleg? - Status Display System 🟢

Eit enkelt og elegant system for å vise din tilgjenge til kollegaer.
Laga for å bli vist på ein [iPad i begrensa tilgangsmodus](https://support.apple.com/no-no/guide/ipad/ipada16d1374/ipados), men du kan bruke kva skjerm som helst. 

## 📋 To separate sider

1. **index.html** - Hovudvisning (viser status)
2. **innstillingar.html** - Kontrollpanel (opnast på same eining som hovudvisninga)

> ⚠️ **Viktig:** Alle innstillingar blir lagra i nettlesaren (`localStorage`) på eininga du brukar.
> Endringar gjort på telefonen kjem **ikkje** fram til iPaden. Vil du at statusen skal endre seg
> utan at du rører iPaden, bruk Outlook-synk – då hentar iPaden statusen frå kalenderen din.

## ✨ Funksjonar

- 🟢 **Fem statusar**: tilgjengeleg, i møte, oppteken, lunsjpause, ikkje her no
- 📅 **Komande møte** - Viser klokkesletta for dei neste møta (utan titlar, av omsyn til personvern)
- 🔄 **Outlook-synk** - Automatisk frå delt kalender, inkl. gjentakande møte
- ⏰ **Tidsstyrt** - Automatisk statusendring
- 👆 **Overstyr på iPaden** - Trykk på statussirkelen og vel status og kor lenge
- 🎨 **Kvinnherad-design** - Vakre fjord- og fjellfargar

## Demo ##
Sjå https://ghveem.github.io/opptatt/

## 🚀 Rask start

### 1. GitHub Pages (Anbefalt)
```
1. Klon dette repoet "opptatt"
2. Last opp index.html og innstillingar.html
3. Settings → Pages → Aktiver
4. Ferdig!
```

### 2. Bruk
```
Hovudvisning (iPad): https://dittbrukarnamn.github.io/opptatt/
Innstillingar (same iPad, langt trykk på sirkelen): https://dittbrukarnamn.github.io/opptatt/innstillingar.html
```

## 📱 Oppsett

### iPad-visning (utanfor kontoret)
1. Opne hovudvisning på iPad
2. Legg til på heimeskjermen
3. [Konfigurer Guided Access for kiosk-modus på ein iPad](https://support.apple.com/no-no/guide/ipad/ipada16d1374/ipados) 
4. Monter utanfor kontoret

### Overstyre status på iPaden
1. Trykk på statussirkelen
2. Vel status (tilgjengeleg, oppteken, i møte, lunsjpause, ikkje her no)
3. Vel kor lenge: 30 min, 1 time, 2 timar eller resten av dagen
4. Når tida er ute, tek kalenderen (eller manuell status) over att av seg sjølv

Overstyringa går føre kalenderen. Vil du avslutte ho tidleg, trykk på sirkelen og vel «↺ Avslutt overstyring».
Panelet lukkar seg sjølv etter 15 sekund utan trykk. Dette fungerer i Guided Access.

### Innstillingar
Hald fingeren på statussirkelen i 1,5 sekund for å opne innstillingane (kalender-URL og standardstatus).
Det finst ingen synleg innstillingsknapp, så forbipasserande kjem ikkje til innstillingane ved eit uhell.

## 🎯 Tre bruksmåtar

### 1. Manuell (Enklast)
- Opne innstillingarsida på iPaden
- Klikk på snøggknapp
- Lagre

### 2. Tidsstyrt
- Set "Oppteken til: 14:00"
- Status endrar seg automatisk kl 14:00

### 3. Outlook-synk (Mest automatisk)
- Lim inn ICS-URL frå Outlook
- Aktiver kalender-synk
- Alt skjer automatisk!

Kalendersynken handterer:
- Gjentakande møte (dagleg, vekentleg, månadleg, årleg – med unntak og flytta forekomstar)
- Avlyste møte og hendingar merka som «Ledig» blir ignorerte
- Tider i UTC og i lokal tidssone

Merk: Når kalender-synk er aktiv, overstyrer kalenderen manuell status. Viss direkte henting
blir blokkert av CORS, blir kalender-URL-en sendt via den eksterne tenesta `api.allorigins.win`.
Kalender-URL-en gir lesetilgang til kalenderen din, så vurder om det er greitt.

## 📅 Outlook-integrering

Korleis få ICS-URL:
### Alternativ 1: 
1. Outlook Calendar → Høgreklikk på kalender
2. "Delingsinnstillingar" → "Publiser"
3. Vel "Kan sjå når eg er oppteken"
4. Kopier ICS-lenka
5. Lim inn i innstillingarsida

### Alternativ 2: 
1. Rett over kalenderen på nett, trykk Kalender-innstillingar
2. Trykk Delte kalenderar
3. Publiser ein kalender
4. Velg kalenderen du vil bruke, velg "Kan vise når eg er oppteken"
5. Trykk publiser. 
6. Kopier lenka som sluttar med .ICS.


## 🎨 Statusar

| Status | Farge | Melding |
|--------|-------|---------|
| Eg er tilgjengeleg | 🟢 | Bank på og vent på svar. |
| Eg er i møte | 🔵 | Ikkje forstyrr – kom igjen etter møtet. |
| Eg er oppteken | 🔴 | Ikkje forstyrr. |
| Eg har lunsjpause | 🔵 | Kom igjen seinare. |
| Eg er ikkje her no | 🟡 | Send ei melding på Teams. |

## 🆘 Feilsøking

**Status oppdaterer seg ikkje:**
- Sjekk at innstillingar er lagra
- Oppdater sida (F5)

**Kalendersynk fungerer ikkje:**
- Sjekk at ICS-URL er riktig
- Test URL direkte i nettlesar

**Endra status på telefonen, men iPaden viser gammal status:**
- Det er forventa – innstillingar blir lagra per eining. Endre på iPaden, eller bruk kalender-synk.

## 📝 Lisens

Open kjeldekode - bruk fritt! Føreslå gjerne forbetringar.

---

**Versjon:** 2.0 | **Laga av:** mest KI, litt Guttorm. 
