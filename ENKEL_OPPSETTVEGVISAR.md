# Enkel Oppsettsvegvisar (Utan Azure) 🚀

## Oversikt

Denne versjonen av Tilgjenge-status krev **IKKJE** Azure-tilgang eller Microsoft-innlogging!

### ✨ Funksjonar
- ✅ **Manuell statuskontroll** - Du vel sjølv når du er tilgjengeleg/oppteken
- ✅ **Snøggvalknappar** - Rask bytting mellom statusar
- ✅ **Tilpassa meldingar** - Legg til eigen tekst
- ✅ **Automatisk oppdatering** - Set tidspunkt for å automatisk endre status
- ✅ **Lagring** - Status blir hugsa når du lukkar og opnar på nytt
- ✅ **Ingen innlogging** - Fungerer direkte utan autentisering
- ✅ **Kvinnherad-design** - Same vakre design med kommunen sin logo

---

## 🚀 Rask start

### Alternativ 1: GitHub Pages (Anbefalt)

#### Steg 1: Opprett GitHub Repository
1. Gå til [GitHub](https://github.com) og logg inn
2. Klikk **+** → **New repository**
3. Namn: `tilgjenge-status`
4. Set til **Public**
5. Klikk **Create repository**

#### Steg 2: Last opp fila
1. I repositoryet, klikk **Add file** → **Upload files**
2. Last opp `index-enkel.html`
3. Gi fila nytt namn til `index.html` (viktig!)
4. Commit changes

#### Steg 3: Aktiver GitHub Pages
1. Gå til **Settings** → **Pages**
2. Source: `main` branch, `/ (root)` folder
3. Klikk **Save**
4. Vent 2-3 minutt

#### Steg 4: Bruk appen!
- URL: `https://DITTBRUKARNAMN.github.io/tilgjenge-status/`
- Opne på iPad/nettbrett
- Vel status og lagre
- Ferdig! 🎉

---

### Alternativ 2: Lokal fil (Enklaste)

#### For iPad/nettbrett:
1. Send `index-enkel.html` til deg sjølv på e-post
2. Opne e-posten på iPad
3. Opne vedlegget i Safari
4. Legg til på heimeskjermen
5. Ferdig!

#### For datamaskin:
1. Dobbeltklikk på `index-enkel.html`
2. Den opnar i nettlesaren
3. Vel status og bruk!

---

### Alternativ 3: Synology NAS

#### Steg 1: Last opp til Web Station
1. Logg inn på Synology DSM
2. Opne **Web Station**
3. Gå til web-mappa (vanlegvis `/web`)
4. Last opp `index-enkel.html`
5. Gi fila nytt namn til `index.html`

#### Steg 2: Opne appen
- URL: `http://din-synology-ip/index.html`
- Eller: `http://din-synology-ip/tilgjenge/` (om du lagar ei undermappe)

---

## 📱 Oppsett på iPad

### Steg 1: Opne i Safari
1. Gå til URL-en (GitHub Pages / lokal fil / Synology)
2. Appen lastar direkte - ingen innlogging!

### Steg 2: Legg til på heimeskjermen
1. Trykk på **Del**-knappen (firkant med pil opp)
2. Vel **Legg til på Heim-skjerm**
3. Namn: "Status" eller "Tilgjenge"
4. Trykk **Legg til**

### Steg 3: Konfigurer Guided Access (Kiosk-modus)
1. **Innstillingar** → **Tilgjenge** → **Guided Access**
2. Slå på **Guided Access**
3. Set passordkode
4. Opne status-appen
5. Trykk tre gonger på Heim/Side-knappen
6. Trykk **Start**

iPad er no låst til berre denne appen!

---

## 💡 Korleis bruke appen

### Snøggval (Raskaste)
Bruk dei tre store knappane:
- **✓ Tilgjengeleg** - Du er ledig
- **● Oppteken** - Du er travelt oppteken
- **○ I møte** - Du er i møte

### Manuelt val
1. Vel status frå nedtrekkslista:
   - Tilgjengeleg
   - Oppteken
   - I møte
   - Lunsjpause
   - Borte frå kontoret

2. Legg til tilpassa melding (valgfritt):
   - "Tilbake kl 14:00"
   - "På kundebesøk"
   - "Ledig frå kl 15:30"

3. Set automatisk oppdatering (valgfritt):
   - **Oppteken til**: Set kva tid du blir ledig
   - **Tilbake kl**: Set kva tid du kjem tilbake

4. Trykk **💾 Lagre innstillingar**

### Eksempel:

**Scenario 1: Du skal i møte frå 10:00 til 11:00**
1. Klikk "○ I møte"
2. Set "Oppteken til: 11:00"
3. Lagre
→ Status endrar seg automatisk til "Tilgjengeleg" kl 11:00!

**Scenario 2: Lunsjpause**
1. Vel "Lunsjpause" frå lista
2. Set "Tilbake kl: 12:30"
3. Lagre
→ Status endrar seg automatisk kl 12:30!

**Scenario 3: Borte heile dagen**
1. Vel "Borte frå kontoret"
2. Tilpassa melding: "Heimekontor - tilgjengeleg på e-post"
3. Lagre

---

## 🔄 Automatisk oppdatering

Appen sjekkar kvart minutt om det er tid for å endre status automatisk.

Eksempel:
- Du set "Oppteken til: 14:00"
- Kl 14:00 endrar statusen seg automatisk til "Tilgjengeleg"
- Tidspunktet blir automatisk sletta

---

## 💾 Lagring

All data blir lagra lokalt i nettlesaren (localStorage):
- Status
- Tilpassa melding
- Automatiske tidspunkt
- Siste oppdatering

**Viktig**: 
- Data blir ikkje delt med nokon
- Data blir hugsa sjølv om du lukkar nettlesaren
- Berre på den eine eininga (iPad/datamaskin)
- Om du vil at fleire enheter skal sjå same status, bruk GitHub Pages

---

## 🔗 Dele med kollegaer

### GitHub Pages-metode:
1. Del URL-en: `https://DITTBRUKARNAMN.github.io/tilgjenge-status/`
2. Kollegaer opnar URL-en i nettlesaren sin
3. Dei ser din status (oppdaterer seg når du endrar)

**Tips**: Skriv ut ein QR-kode til URL-en og heng utanfor kontoret!

### Lokal fil-metode:
- Ikkje mogleg å dele automatisk
- Må oppdatere status manuelt på kvar eininga

---

## 🎨 Tilpassing

### Endre fargar
Finn `:root` i HTML-fila og endre:
```css
--primary-fjord: #0099D8;    /* Hovudfarge */
--status-available: #4CAF8E; /* Grøn */
--status-busy: #D97757;      /* Raud */
```

### Legg til nye statusar
Finn `<select id="statusSelect">` og legg til:
```html
<option value="ferie">På ferie</option>
```

Deretter legg til i `switch(status)` i JavaScript:
```javascript
case 'ferie':
    indicator.textContent = '🏖️';
    statusText.textContent = 'På ferie';
    statusSubtext.textContent = 'Tilbake snart!';
    break;
```

---

## ⚖️ Samanlikning: Enkel vs Azure-versjon

### Enkel versjon (denne)
✅ Ingen Azure-tilgang nødvendig
✅ Fungerer med ein gong
✅ Manuell kontroll
✅ Automatisk tidsstyring
✅ Enklare oppsett
❌ Ikkje integrert med Outlook-kalender
❌ Må oppdatere manuelt

### Azure-versjon
✅ Automatisk frå Outlook-kalender
✅ Alltid oppdatert
✅ Ingen manuell innsats
❌ Krev Azure-tilgang
❌ Meir komplisert oppsett
❌ Krev Microsoft 365-konto

---

## 🆘 Feilsøking

### Problem: Status endrar seg ikkje automatisk
**Løysing**: 
- Sjekk at du har trykka "Lagre innstillingar"
- Sjekk at nettlesaren er open (appen må vere open for å oppdatere)
- Sjekk at tidspunktet er korrekt sett

### Problem: Status forsvinn når eg lukkar nettlesaren
**Løysing**:
- Trykk "Lagre innstillingar" før du lukkar
- Sjekk at nettlesaren tillèt localStorage
- Prøv ein annan nettlesar (Safari, Chrome)

### Problem: Kollegaer ser ikkje min status
**Løysing**:
- Bruk GitHub Pages-metode
- Del riktig URL
- Be kollegaer oppdatere sida (F5 / Command+R)

### Problem: Appen fungerer ikkje offline
**Løysing**:
- Denne versjonen krev ikkje internett etter første lasting
- Lagre sida for offline-bruk (Fil → Lagre som → Komplett nettside)

---

## 📊 Bruksscenario

### Scenario 1: Heimekontor
- Sett opp på heimekontoret ditt
- Oppdater manuelt når du har møte
- Kollegaer sjekkar status før dei ringjer

### Scenario 2: Utanfor kontoret på iPad
- Heng iPad utanfor kontoret
- Oppdater status via telefonen (same GitHub Pages URL)
- Kollegaer ser status når dei passerer

### Scenario 3: Delt kontor
- Alle i teamet opnar same URL
- Kvar person har eigen fane open
- Alle oppdaterer sin eigen status

---

## 🔒 Personvern

- ✅ Ingen data blir sendt til eksterne serverar
- ✅ All lagring er lokal i nettlesaren
- ✅ Ingen cookies eller tracking
- ✅ Open kjeldekode - sjå all koden i HTML-fila
- ✅ Fungerer utan internett (etter første lasting)

---

## 🎓 Tips og triks

### Tips 1: Bruk Siri-snarveier (iOS)
Opprett Siri-snarvegar for:
- "Sett status til oppteken"
- "Sett status til tilgjengeleg"
→ Oppdater status med stemma!

### Tips 2: QR-kode
- Generer QR-kode til GitHub Pages URL
- Skriv ut og heng ved kontoret
- Kollegaer skannar for å sjå status

### Tips 3: Fleire skjermar
- Opne URL-en på fleire iPad/skjermar
- Alle viser same status
- Plasser utanfor kontoret, i møterom, osv.

### Tips 4: Varsel
Sett varsling på telefonen din for:
- 11:45 - "Husk å sette status til lunsjpause"
- 16:45 - "Husk å sette status til heime"

---

## 📚 Vidare utvikling

Framtidige funksjonar du kan legge til sjølv:
- Statushistorikk
- Fleire språk
- Mørkemodus
- Integrasjon med anna system (via API)
- Push-varsel

---

## ✅ Ferdig!

No har du ein enkel statusvisning som fungerer utan Azure!

**Din URL** (GitHub Pages): `https://DITTBRUKARNAMN.github.io/tilgjenge-status/`

Lukke til! 🎉

---

**Versjon**: 1.0 Enkel  
**Dato**: Januar 2026  
**Laga for**: Kvinnherad kommune
