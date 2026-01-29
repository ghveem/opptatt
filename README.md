# Tilgjengeleg? - Status Display System 🟢

Eit enkelt og elegant system for å vise din tilgjenge til kollegaer.

## 📋 To separate sider

1. **index.html** - Hovudvisning (viser status)
2. **innstillingar.html** - Kontrollpanel (endre status eksternt)

## ✨ Funksjonar

- 🟢 **Fire statusar**: Tilgjengeleg, Oppteken, I møte, Ute
- 📅 **Komande møte** - Viser dei neste 12 timane
- 🔄 **Outlook-synk** - Automatisk frå delt kalender
- ⏰ **Tidsstyrt** - Automatisk statusendring
- 📱 **Ekstern kontroll** - Endre frå telefon/datamaskin
- 🎨 **Kvinnherad-design** - Vakre fjord- og fjellfargar

## 🚀 Rask start

### 1. GitHub Pages (Anbefalt)
```
1. Opprett GitHub repository "tilgjenge-status"
2. Last opp index.html og innstillingar.html
3. Settings → Pages → Aktiver
4. Ferdig!
```

### 2. Bruk
```
Hovudvisning (iPad): https://dittbrukarnamn.github.io/tilgjenge-status/
Innstillingar (telefon): https://dittbrukarnamn.github.io/tilgjenge-status/innstillingar.html
```

## 📱 Oppsett

### iPad-visning (utanfor kontoret)
1. Opne hovudvisning på iPad
2. Legg til på heimeskjermen
3. Konfigurer Guided Access for kiosk-modus
4. Monter utanfor kontoret

### Ekstern kontroll (telefon/PC)
1. Lagre innstillingarsida som bokmerke
2. Opne når du vil endre status
3. Vel status og lagre
4. iPad oppdaterer seg automatisk!

## 🎯 Tre bruksmåtar

### 1. Manuell (Enklast)
- Opne innstillingarsida
- Klikk på snøggknapp
- Lagre

### 2. Tidsstyrt
- Set "Oppteken til: 14:00"
- Status endrar seg automatisk kl 14:00

### 3. Outlook-synk (Mest automatisk)
- Lim inn ICS-URL frå Outlook
- Aktiver kalender-synk
- Alt skjer automatisk!

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
| Tilgjengeleg | 🟢 | Bank gjerne på |
| Oppteken | 🔴 | Ikkje forstyrr |
| I møte | 🔵 | Prøv igjen etter møtet |
| Ute | 🟡 | Send gjerne ein e-post |

## 🆘 Feilsøking

**Status oppdaterer seg ikkje:**
- Sjekk at innstillingar er lagra
- Oppdater sida (F5)

**Kalendersynk fungerer ikkje:**
- Sjekk at ICS-URL er riktig
- Test URL direkte i nettlesar

**Kollegaer ser ikkje oppdatering:**
- Be dei oppdatere sida

## 📝 Lisens

Open source - bruk fritt!

---

**Versjon:** 2.0 | **Laga av:** mest KI, litt Guttorm. 
