# Design-dokumentasjon 🎨

## Designinspirasjonen frå Kvinnherad kommune

Appen sin visuelle identitet er inspirert av Kvinnherad kommune sitt kommunevåpen, natur og profil.

---

## 🌊 Kommunevåpenet - Kjerna i designet

Kvinnherad sitt kommunevåpen viser **ein blå gaffelkross** (Y-form) med **bølgjesnitt** på kvit/sølv bakgrunn.

### Symbolikk:
- **To elvar** som renn saman til éin elv
- **Hattebergselvi** og **Melselvi** som møtest ved Rosendal
- **Bølgjesnitt** symboliserer vassdraga sitt flytande, organiske form

### Korleis det er brukt i appen:
✅ **Logo**: Den offisielle Kvinnherad kommune-logoen (KK_Logo_20cm.png)
✅ **Plassering**: Sentrert over tittelen, 120px breidde
✅ **Format**: Embedded som base64 i HTML for enkel distribusjon
✅ **Fargepalett**: Blåtonar frå den offisielle logoen (#0099D8)

---

## 🎨 Fargepalett

### Primærfargar (Fjord og himmel)
```css
--primary-fjord: #0099D8    /* Offisiell Kvinnherad-blå frå logoen */
--primary-sky: #33ADE3      /* Lys himmelblå */
```
**Inspirasjon**: Hardangerfjorden, offisiell kommunefarge

### Nøytrale fargar (Snø og is)
```css
--neutral-snow: #F8FAFB     /* Snøkvit bakgrunn */
--neutral-ice: #E5F4FA      /* Isblå highlight - tilpassa logo */
```
**Inspirasjon**: Folgefonna-isbreen, vinterlandskap, rein snø

### Tekstfargar (Fjell og stein)
```css
--text-dark: #1E3A5F        /* Mørk fjellblå */
--text-mid: #4A6B8A         /* Mellomblå stein */
```
**Inspirasjon**: Rosendalsalpane, mektige fjellformasjonar

### Accentfarge (Isbre)
```css
--accent-glacier: #66BFEB   /* Isbre-blå - lysare variant av logo-blå */
```
**Inspirasjon**: Folgefonna-isbreen, blått isglitter, kommunefarge

### Statusfargar
```css
--status-available: #4CAF8E /* Grøn - friske dalar */
--status-busy: #D97757      /* Oransje - varme */
--status-meeting: #5B8FBF   /* Blå - roleg fjord */
```
**Inspirasjon**: 
- Grøn = Grøderike u-dalar i Hardanger
- Oransje = Varme, engasjement
- Blå = Roleg fjord, fokusert arbeid

---

## 🏔️ Designprinsipp

### 1. Naturinspirert
- Organiske former og bølgjande linjer
- Mjuke overgangar og gradienter
- Flytande animasjonar (som vassdrag)

### 2. Profesjonell kommuneprofil
- Rein og moderne
- Lett å lese og forstå
- Tilgjengeleg for alle brukarar

### 3. Lokalt forankra
- Reflekterer Kvinnherad sin natur
- Viser stoltheit over lokalmiljøet
- Kjenneteiknar kommunen sin identitet

---

## 📐 Typografi

### Display (Overskrifter)
**DM Serif Display** - Elegant, klassisk serif
- Brukt til: `<h1>` hovudtittel "Tilgjenge"
- Symboliserer: Tradisjon, tillit, kvalitet
- Inspirasjon: Baroniet Rosendal (1665), historisk arv

### Body (Brødtekst)
**Work Sans** - Moderne, lesbar sans-serif
- Brukt til: All brødtekst, knappar, detaljar
- Symboliserer: Moderne, effektiv kommune
- Inspirasjon: Samtidskunst, framtidsretta

---

## 🌊 Bølgjande vassdrag-effekt

Bakgrunnen har **to radielle gradienter** som flyt mjukt:
- Ein frå topp-høgre (primær)
- Ein frå botn-venstre (sekundær)
- Animerte med `floatBackground` (20s / 25s)

**Symbolikk**: Vassdraga i Kvinnherad som stadig er i rørsle

---

## ✨ Logo/Ikon

**Design**:
- Offisiell Kvinnherad kommune-logo (KK_Logo_20cm.png)
- Viser kommunevåpenet med to elvar som møtest
- Y-form (gaffelkross) med bølgjande kant
- Lyseblå farge (#0099D8) på kvit bakgrunn

**Teknisk implementasjon**:
- Embedded som base64 data-URI i HTML
- Ingen eksterne biletfileavhengigheiter
- Optimal for GitHub Pages deployment
- Skalerer responsivt

**Dimensjonar**: 120px breidde, auto høgde
**Plassering**: Sentrert over tittelen
**Opacity**: 0.95 for mjuk integrasjon

---

## 🎯 Statusindikatorar

### Tilgjengeleg (Grøn)
```css
background: linear-gradient(135deg, #4CAF8E 0%, #6AC5A3 100%);
```
**Symbol**: ✓ (sjekk)
**Assosiasjon**: Friske grøne dalar, vekst, tilgjenge

### Oppteken (Oransje/raud)
```css
background: linear-gradient(135deg, #D97757 0%, #E68A6E 100%);
```
**Symbol**: ● (fylt sirkel)
**Assosiasjon**: Varme, aktivitet, engasjement

### Snart oppteken (Blå)
```css
background: linear-gradient(135deg, #5B8FBF 0%, #7AA8D1 100%);
```
**Symbol**: ○ (open sirkel)
**Assosiasjon**: Roleg fjord, førebuing, overgang

---

## 🔄 Animasjonar

### 1. Slide Up (Kortet dukkar opp)
```css
@keyframes slideUp {
    from: translateY(30px), opacity: 0
    to: translateY(0), opacity: 1
}
```
**Timing**: 0.6s ease-out
**Formål**: Mjuk introduksjon når sida lastar

### 2. Pulse (Statusindikator)
```css
@keyframes pulse {
    0%, 100%: scale(1)
    50%: scale(1.05)
}
```
**Timing**: 2s ease-in-out infinite
**Formål**: Levande status, merksemd

### 3. Float Background (Bakgrunn)
```css
@keyframes floatBackground {
    0%, 100%: translate(0, 0) scale(1)
    50%: translate(-10%, 5%) scale(1.1)
}
```
**Timing**: 20s / 25s ease-in-out infinite
**Formål**: Simulerer flytande vassdrag

### 4. Fade In (Tekst)
```css
@keyframes fadeIn {
    from: translateY(10px), opacity: 0
    to: translateY(0), opacity: 1
}
```
**Timing**: 0.5s ease-out, staggered delays
**Formål**: Gradvis avdekking av innhald

### 5. Slide In (Event details)
```css
@keyframes slideIn {
    from: translateX(-20px), opacity: 0
    to: translateX(0), opacity: 1
}
```
**Timing**: 0.5s ease-out 0.6s both
**Formål**: Naturleg inngliding av detaljar

---

## 📱 Responsivt design

### Desktop/iPad landscape (standard)
- Statusindikator: 180x180px
- Font-størrelse h1: 3.5rem
- Full padding og luft

### Mobil/iPad portrait (<640px)
```css
@media (max-width: 640px) {
    h1 { font-size: 2.5rem; }
    .status-indicator { 
        width: 140px; 
        height: 140px; 
    }
    .auth-card, .status-card { 
        padding: 2rem; 
    }
}
```

---

## ♿ Tilgjengelegheit

### Kontrast
- **WCAG AA**: Alle tekststørrelsar har tilstrekkeleg kontrast
- **Tekst på bakgrunn**: Minimum 4.5:1 ratio
- **Knappar**: Tydeleg visuell feedback

### Interaksjon
- **Hover-states**: Alle klikkbare element har hover-effekt
- **Focus-states**: Tastaturnavigasjon støtta
- **Touch-targets**: Minimum 44x44px (mobilvenleg)

### Lesbarheit
- **Linjehøgde**: 1.5-1.6 for optimal lesbarheit
- **Maksbreidde**: 800px for å unngå for lange linjer
- **Font-størrelse**: Minimum 16px for brødtekst

---

## 🎨 Design-variasjonar (framtidige moglegheiter)

### Vintermodus
- Meir snøkvite tonar
- Lysare blå (is)
- Kristallglitter-effektar

### Sommarmodus
- Varmere grøntonar
- Djupare fjordblå
- Meir dynamikk og liv

### Mørkemodus
- Mørk fjord/natt-palett
- Nordlys-inspirerte accentar
- Redusert lysstyrke for kveldstid

---

## 🏆 Design-mål oppnådde

✅ **Lokal identitet**: Reflekterer Kvinnherad sin natur og identitet  
✅ **Profesjonalitet**: Moderne, rein kommuneprofil  
✅ **Tilgjengelegheit**: Lesbar og brukarvennleg for alle  
✅ **Gjenkjenning**: Brukar kommunevåpenet sitt symbolspråk  
✅ **Vakker**: Estetisk tiltalande, stoltheitsfølelse  

---

## 📝 Krediteringar

**Design-inspirasjon**:
- Kvinnherad kommune sitt kommunevåpen (1982)
- Hardangerfjorden og Folgefonna
- Norsk fjordlandskap og vassdrag
- Baroniet Rosendal (historisk arv)

**Fargepalett**:
- Basert på Kvinnherad sin natur
- Tilpassa moderne UX-prinsipp
- Optimalisert for skjermvisning

**Typografi**:
- DM Serif Display (Google Fonts)
- Work Sans (Google Fonts)

---

**Designa av**: Claude (Anthropic)  
**Versjon**: 2.0 - Kvinnherad-tema  
**Dato**: Januar 2026
