# Tilgjenge-status 🟢

Ein enkel og vakker webapp som viser din tilgjenge basert på Outlook-kalenderen din. Perfekt for å vise til kollegaer på eit nettbrett eller iPad utanfor kontoret ditt!

![Status Display](https://img.shields.io/badge/Status-Tilgjengeleg-green)
![Language](https://img.shields.io/badge/Spr%C3%A5k-Nynorsk-blue)
![Platform](https://img.shields.io/badge/Platform-Web-orange)

## ✨ Funksjonar

- 🟢 **Sanntidsstatus** - Viser om du er tilgjengeleg, oppteken eller snart oppteken
- 📅 **Outlook-integrering** - Hent status direkte frå Microsoft 365-kalenderen din
- 🔒 **Trygg innlogging** - Bruk Microsoft sin sikre innlogging (OAuth 2.0)
- 🎨 **Kvinnherad-inspirert design** - Designa med kommunevåpenet og naturen som inspirasjon
- 🌊 **Bølgjande vassdrag** - Logo og fargar inspirert av Hattebergselvi og Melselvi
- 📱 **Responsiv** - Fungerer perfekt på iPad, nettbrett, mobil og desktop
- 🔄 **Automatisk oppdatering** - Status oppdaterer seg kvart minutt
- 👁️ **Valgfrie detaljar** - Vel om du vil vise møtetittel og tid
- 🌐 **Ingen server nødvendig** - Alt køyrer i nettlesaren

## 🖼️ Slik ser det ut

### Tilgjengeleg
```
    ✓
Tilgjengeleg
Ingen møte akkurat no
```

### Oppteken
```
    ●
Oppteken
Tilgjengeleg om 25 minutt
[Møtetittel og tid hvis valt]
```

### Snart oppteken
```
    ○
Snart oppteken
Møte om 10 minutt
[Møtetittel og tid hvis valt]
```

## 🚀 Rask start med GitHub Pages

### 1. Registrer app i Azure Portal
- Gå til [Azure Portal](https://portal.azure.com)
- Opprett ein ny App Registration
- Hent Client ID
- Legg til Redirect URI: `https://DITTBRUKARNAMN.github.io/tilgjenge-status/`

### 2. Opprett GitHub Repository
- Opprett nytt repository: `tilgjenge-status`
- Last opp filene frå dette prosjektet
- Set repository til Public

### 3. Konfigurer appen
- Rediger `index.html` på GitHub
- Byt ut `YOUR_CLIENT_ID_HERE` med din Client ID frå Azure

### 4. Aktiver GitHub Pages
- Gå til Settings → Pages
- Vel `main` branch og `/ (root)` folder
- Vent 2-3 minutt på deployment

### 5. Test appen
- Gå til `https://DITTBRUKARNAMN.github.io/tilgjenge-status/`
- Logg inn med Microsoft-kontoen din
- Sjå statusen din! 🎉

### 6. Sett opp på iPad
- Opne URL-en i Safari
- Legg til på heimeskjermen
- Bruk Guided Access for kiosk-modus

## 📖 Fullstendig dokumentasjon

Sjå [GITHUB_OPPSETTVEGVISAR.md](GITHUB_OPPSETTVEGVISAR.md) for detaljert steg-for-steg oppsettvegvisar.

## 🎨 Tilpassing

### Endre fargar
Endre fargane i `:root` CSS-variablane:
```css
--status-available: #7CAA7C;  /* Grøn */
--status-busy: #C97F6F;       /* Raud */
--status-meeting: #8B9DC9;    /* Blå */
```

### Endre oppdateringsfrekvens
```javascript
setInterval(getCalendarStatus, 60000); // Endre 60000 (1 minutt)
```

## 🎨 Design

Appen er designa med inspirasjon frå Kvinnherad kommune:

### Kommunevåpen
- **Symbol**: To bølgjande elvar som renn saman (Hattebergselvi og Melselvi)
- **Fargar**: Blå fjordtonar på kvit/sølv bakgrunn
- **Logo**: SVG-ikon viser to vassdrag som møtest

### Fargepalett
- **Fjordblå** (#2563A8) - Hardangerfjorden
- **Himmelblå** (#4A90C8) - Klår vestlandsluft
- **Snøkvit** (#F8FAFB) - Folgefonna-breen
- **Isblå** (#E5EFF7) - Vinterlandskap

Sjå [DESIGN_DOKUMENTASJON.md](DESIGN_DOKUMENTASJON.md) for fullstendig designforklaring.

## 🛠️ Teknologi

- **Frontend**: Vanilla HTML, CSS, JavaScript
- **Autentisering**: MSAL.js (Microsoft Authentication Library)
- **API**: Microsoft Graph API
- **Design**: Scandinavisk-inspirert, responsiv design

## 🔐 Tryggleik

- Ingen data blir lagra på server
- All databehandling skjer i nettlesaren
- Trygg OAuth 2.0 innlogging
- Berre lesestilgang til kalenderen din
- Token blir lagra lokalt i nettlesaren

## 📋 Krav

- Microsoft 365 / Outlook-konto
- Azure AD tilgang for app-registrering
- Moderne nettlesar (Chrome, Safari, Edge, Firefox)
- Internettilkopling

## 🌍 Hosting med GitHub Pages

GitHub Pages er den **anbefalte** hosting-metoden fordi det er:
- ✅ Gratis
- ✅ Automatisk HTTPS
- ✅ Enkelt å sette opp
- ✅ Automatisk oppdatering ved endringar

### Sett opp GitHub Pages
```bash
# 1. Opprett repository på GitHub
# 2. Last opp filene
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/DITTBRUKARNAMN/tilgjenge-status.git
git push -u origin main

# 3. Aktiver GitHub Pages i Settings → Pages
# 4. Din app er no live på: https://DITTBRUKARNAMN.github.io/tilgjenge-status/
```

Sjå [GITHUB_OPPSETTVEGVISAR.md](GITHUB_OPPSETTVEGVISAR.md) for detaljert guide!

## 🌍 Alternative hosting-alternativ

### Synology NAS
```bash
# Opprett repo og push fila
git init
git add tilgjenge-status.html
git commit -m "Initial commit"
git push origin main

# Aktiver GitHub Pages i repo settings
```

### Docker
```yaml
version: '3'
services:
  tilgjenge-status:
    image: nginx:alpine
    ports:
      - "8080:80"
    volumes:
      - ./tilgjenge-status.html:/usr/share/nginx/html/index.html:ro
```

### Lokal testing
```bash
python3 -m http.server 8000
```

## 🎯 Bruksområde

- Vis status utanfor kontoret ditt
- La kollegaer sjå om du er tilgjengeleg
- Kiosk-modus på nettbrett/iPad
- Statusdisplay i møterom
- Heimekontor-statusindikator

## 🤝 Bidrag

Dette er eit open source-prosjekt. Føl deg fri til å:
- Forke prosjektet
- Lage pull requests
- Melde frå om bugs
- Foreslå nye funksjonar

## 📝 Lisens

Dette prosjektet er open source og tilgjengeleg under MIT-lisensen.

## ❓ Spørsmål og støtte

Viss du har spørsmål eller treng hjelp:
1. Sjekk [OPPSETTVEGVISAR.md](OPPSETTVEGVISAR.md)
2. Sjå på feilsøkingsdelen
3. Opne eit issue på GitHub

## 🔄 Oppdateringar

**Versjon 1.0** (Januar 2026)
- Initial release
- Grunnleggjande statusvisning
- Outlook-integrering
- Responsiv design
- Automatisk oppdatering

## 🙏 Takk til

- Microsoft Graph API dokumentasjon
- MSAL.js biblioteket
- Google Fonts (DM Serif Display & Work Sans)

---

Laga med ❤️ for å gjere kontorhverdagen litt enklare!
