# CORS-problem og løysingar 🔧

## Problemet

CORS (Cross-Origin Resource Sharing) hindrar nettlesaren i å hente data frå Outlook Calendar direkte. Dette er ein sikkerheitsmekanisme i nettlesaren.

**Feilmelding du kan sjå:**
```
Access to fetch at 'https://outlook.office365.com/...' has been blocked by CORS policy
```

## ✅ Løysingar

### Løysing 1: Automatisk proxy (Implementert)

Systemet prøver no automatisk to metodar:
1. **Direkte tilgang** (prøver først)
2. **Proxy-tilgang** (AllOrigins.win) - fungerer i dei fleste tilfelle

**Korleis teste:**
1. Gå til innstillingarsida
2. Lim inn ICS-URL
3. Klikk "🧪 Test kalender-tilkopling"
4. Sjå resultatet

### Løysing 2: Outlook Web Access URL

I staden for ICS-URL, bruk Outlook Web Access:

**Steg:**
1. Opne Outlook Calendar på nettet
2. Gå til innstillingar (tannhjul)
3. Vel "Vis alle Outlook-innstillingar"
4. Gå til "Kalender" → "Delte kalendrar"
5. Publiser kalenderen og kopier **HTML-lenka**
6. Erstatt "html" med "ics" i URL-en

**Eksempel:**
```
Original: https://outlook.office.com/calendar/published/.../calendar.html
Endra:    https://outlook.office.com/calendar/published/.../calendar.ics
```

### Løysing 3: Google Calendar som mellomledd

Viss Outlook ikkje fungerer:

1. **Importer Outlook til Google Calendar:**
   - Google Calendar → Innstillingar
   - "Importer og eksporter"
   - Importer frå Outlook

2. **Få offentleg URL:**
   - Google Calendar → Innstillingar
   - Vel kalenderen
   - "Integrer kalender"
   - Kopier "Offentleg URL i iCal-format"

3. **Bruk denne URL-en i systemet**

### Løysing 4: Calendly / Cal.com

Bruk ein tredjepartsteneste:
- Calendly (gratis tier)
- Cal.com (open source)
- Disse har ofte betre CORS-støtte

## 🧪 Test kalender-tilkopling

Før du aktiverer kalender-synk:

1. Gå til innstillingarsida
2. Lim inn kalender-URL
3. Klikk "🧪 Test kalender-tilkopling"
4. Sjå om det fungerer:
   - ✅ Grøn = Fungerer!
   - ❌ Raud = Prøv ein annan metode

## 📝 Alternativ: Manuell oppdatering

Viss ingen av løysingane fungerer:

**Bruk manuell modus:**
1. Ikkje aktiver kalender-synk
2. Oppdater status manuelt frå telefonen
3. Bruk tidsstyrt automatikk

**Eksempel:**
- Før møte: Set "I møte" + "Oppteken til: 14:00"
- Status endrar seg automatisk kl 14:00

## 🔍 Feilsøking

### Problem: Proxy fungerer ikkje

**Sjekk:**
1. Er AllOrigins.win tilgjengeleg? (Test: https://api.allorigins.win/raw?url=https://google.com)
2. Er kalender-URL-en offentleg tilgjengeleg?
3. Opne URL-en direkte i nettlesaren - fungerer ho?

### Problem: Ingen hendingar vises

**Sjekk:**
1. Har kalenderen hendingar dei neste 12 timane?
2. Er hendingane offentlege (ikkje private)?
3. Er kalenderen delt som "Kan sjå når eg er oppteken"?

### Problem: Gamle hendingar vises

**Løysing:**
- Oppdater sida (F5)
- Sjekk at oppdateringsfrekvensen er sett riktig
- Sjekk at nettlesarklokka er riktig

## 💡 Beste praksis

### For påliteleg drift:

1. **Test før produksjon:**
   - Bruk test-knappen først
   - Sjekk at hendingar vises riktig
   - Vent minst 5 minutt og sjekk igjen

2. **Vel riktig oppdateringsfrekvens:**
   - **Kvart minutt**: For sanntidsoppdatering (anbefalt for demo/test)
   - **Kvart 5. minutt**: Balanse mellom respons og last
   - **Kvart 10. minutt**: For stabil drift
   - **Kvart 30. minutt**: For minimal last

3. **Ha backup-plan:**
   - Lær deg å bruke manuell modus
   - Lagre innstillingarsida som bokmerke
   - Test at du kan oppdatere frå telefonen

## 🌐 Nettlesarstøtte

**Fungerer best i:**
- Chrome/Edge (beste CORS-handtering)
- Safari (god støtte)
- Firefox (god støtte)

**Kan ha problem i:**
- Eldre nettlesarversjonar
- Nettlesarar med streng CORS-policy
- Bedriftsnettlesarar med ekstra sikkerheit

## 📞 Få hjelp

Viss ingen av løysingane fungerer:

1. **Test-resultat:**
   - Kopier feilmeldinga frå test-knappen
   - Send til IT-støtte

2. **Nettlesarkonsoll:**
   - Trykk F12
   - Gå til "Console"
   - Kopier feilmeldingar

3. **Alternativ løysing:**
   - Bruk manuell modus
   - Be IT-avdelinga om hjelp med ICS-URL
   - Vurder Google Calendar som mellomledd

## ✅ Oppsummering

**Anbefalt rekkefølgje:**
1. Prøv direkte ICS-URL → Test
2. Viss det feiler → Proxy blir brukt automatisk
3. Viss det framleis feiler → Prøv Outlook Web Access URL
4. Viss ingenting fungerer → Bruk Google Calendar mellomledd
5. Siste utveg → Bruk manuell modus med tidsstyrt automatikk

**Viktigast:**
- Test før produksjon
- Ha ein backup-plan
- Lær deg manuell modus

Lukke til! 🚀
