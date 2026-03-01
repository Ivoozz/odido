# Odido Datalek Informatie

Een complete, informatieve Nederlandstalige website over het Odido datalek van 2026, inclusief een volledig geautomatiseerd installatiescript voor Debian/Nginx.

![Screenshot placeholder](https://via.placeholder.com/900x500/1a1a2e/4a90d9?text=Odido+Datalek+Informatie)

---

## 🚀 Snelle installatie (één commando)

```bash
curl -sL https://raw.githubusercontent.com/Ivoozz/odido/main/install.sh | bash
```

> Vereist root-toegang op een Debian 11/12 server of LXC-container.

---

## 📋 Vereisten

- Debian 11 (Bullseye) of Debian 12 (Bookworm) — ook geschikt voor Proxmox LXC-containers
- Root-toegang (of `sudo`)
- Poort 80 open (HTTP)
- Internetverbinding (voor `apt-get`)

---

## 🔧 Wat doet het installatiescript?

- ✅ Controleert of het script als root wordt uitgevoerd
- ✅ Voert `apt-get update && apt-get upgrade -y` uit
- ✅ Installeert `nginx` en `curl`
- ✅ Maakt de webroot `/var/www/odido/` aan
- ✅ Schrijft de volledige `index.html` naar de webroot (ingebouwd in het script)
- ✅ Maakt een Nginx server block aan op poort 80 met gzip-compressie
- ✅ Activeert de site en verwijdert de standaard Nginx-site
- ✅ Test de Nginx-configuratie (`nginx -t`)
- ✅ Herstart en schakelt Nginx in via `systemctl`
- ✅ Stelt correcte bestandsrechten in (`www-data`)
- ✅ Toont het IP-adres van de server na succesvolle installatie

---

## 📁 Bestandsstructuur

```
odido/
├── index.html      ← Nederlandstalige single-page website (Tailwind CSS CDN)
├── install.sh      ← Volledig geautomatiseerd Debian/Nginx installatiescript
└── README.md       ← Dit bestand
```

---

## 🌐 Website-inhoud

De website bevat de volgende secties (volledig in het Nederlands):

1. **Navigatiebalk** — Responsief met hamburgermenu op mobiel
2. **Hero** — Waarschuwingsbanner en twee call-to-action knoppen
3. **Situatie Overzicht** — Wat is er uitgelekt, statistieken, achtergrond
4. **Wat staat er online** — Risico's en omvang van de gepubliceerde data
5. **Actiepunten** — 10 stappen om jezelf te beschermen
6. **Have I Been Pwned** — Directe link om te controleren of jouw data uitgelekt is
7. **Veelgestelde Vragen** — FAQ met accordion (pure JavaScript)
8. **Bronnen & Referenties** — Alle relevante bronnen
9. **Footer** — Disclaimer en navigatielinks

---

## 📰 Bronnen

1. [NOS – Odido hackers publiceren resterende klantdata](https://nos.nl/artikel/2604461-odido-hackers-publiceren-resterende-klantdata-ook-miljoenen-id-nummers)
2. [Consumentenbond – Datalekken: de gevaren en wat moet je doen](https://www.consumentenbond.nl/veilig-internetten/datalekken-de-gevaren-en-wat-moet-je-doen)
3. [Odido Officieel – odido.nl/veiligheid](https://www.odido.nl/veiligheid)
4. [RTL Nieuws – Wat moet je doen als jouw gegevens zijn gelekt?](https://www.rtl.nl/nieuws/economie/artikel/5566879/wat-moet-je-doen-als-jouw-gegevens-zijn-gelekt-bij-odido)
5. [RTL Nieuws – Check gelekte data](https://www.rtl.nl/nieuws/binnenland/artikel/5572982/odido-hackers-check-gelekte-data)
6. [Have I Been Pwned](https://haveibeenpwned.com/)
7. [Check je Hack – Politie.nl](https://www.politie.nl/informatie/checkjehack.html)

---

## ⚠️ Disclaimer

Deze website is een onafhankelijke, informatieve bron over het Odido datalek en is op geen enkele wijze gelieerd aan of goedgekeurd door Odido of T-Mobile Nederland. De informatie op deze site is uitsluitend bedoeld ter informatie en vormt geen juridisch of financieel advies.