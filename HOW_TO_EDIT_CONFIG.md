# ZwiksBank — Hoe de config aanpassen?

De geheime gegevens zitten **verborgen** in `index.html` als een base64-gecodeerde string.
Dylan kan deze NIET zien in de browser developer tools (het ziet eruit als willekeurige tekens).

## Stap voor stap aanpassen

Open `index.html` in een tekstverwerker en zoek naar deze regel:

```
const _d = atob("eyJjYXJkT...");
```

De lange string tussen de aanhalingstekens is de base64-encoded config.

### Om de config te wijzigen, gebruik deze website:
1. Ga naar: https://www.base64encode.org/
2. Plak de onderstaande JSON in het tekstvak (pas de waarden aan)
3. Klik "Encode"
4. Vervang de lange string in `index.html`

### De JSON die je moet aanpassen:

```json
{
  "cardNumber": "5318 0082 1337 3003",
  "iban": "BE68 5390 0754 7034",
  "expiry": "12/30",
  "clientNumber": "308042",
  "cvc": "330",
  "pin": "3000",
  "cardHolder": "Dylan Gybels",
  "amount": 330,
  "friends": [
    "Amber", "Axel", "Bo", "Bram", "Bryan",
    "Charlotte", "Elien", "Emile", "Fleur", "Jarne",
    "Jonas", "Jolien", "Kevin", "Lander", "Laura",
    "Lena", "Louis", "Maxim", "Nathalie", "Nina",
    "Pieter", "Quinten", "Robbe", "Silke", "Simon",
    "Stan", "Thomas", "Tibo", "Warre", "Wouter"
  ]
}
```

**Tip:** Kies zelf de cijfers voor het kaartnummer, IBAN, etc. en geef Dylan de opdrachten!

---

## GitHub Pages hosten

1. Maak een nieuw repository aan op GitHub (bijv. `zwiks-bank`)
2. Upload `index.html`
3. Ga naar **Settings → Pages → Source: main branch / root**
4. Je website is live op: `https://jouwgebruikersnaam.github.io/zwiks-bank`
