# Silent Zagreb Badminton — logo ikona i pocetni ekran

Ova nadogradnja zadrzava postojecu Google prijavu, Firebase konfiguraciju i sve korisnicke podatke.

## Sto je novo
- Nova PWA ikona od originalnog loga: `icons/silent-logo-192.png`, `icons/silent-logo-512.png`.
- Ikona za iPhone: `icons/apple-touch-icon.png`.
- Maskable ikona za Android: `icons/silent-maskable-512.png`.
- Pocetni ekran s logom prilikom pokretanja instalirane aplikacije (kratki prikaz).
- Osvjezen manifest i Service Worker da bi se nove ikone ucitale.

## GitHub objava
Raspakirajte ZIP i prenesite **sadrzaj** mape u korijen repozitorija `myrent-adi/badminton-liga`. Prenesite i mape `icons` i `assets`. Na pitanje o zamjeni datoteka odaberite zamjenu. GitHub Pages potom objavljuje izmjene.

## Na mobitelu
Nakon objave uklonite stari precac/instalaciju i ponovno dodajte aplikaciju sa `https://myrent-adi.github.io/badminton-liga/`.
- Android: Chrome > izbornik > Instaliraj aplikaciju (ako se nudi).
- iPhone: Safari > Dijeli > Dodaj na pocetni zaslon.

**Napomena:** iOS i Android sami kontroliraju vlastitu sistemsku uvodnu animaciju; nas kratki ekran s logom prikazuje se nakon ucitavanja web-aplikacije. Nije moguce jamciti da sustav nikada nece prikazati Chrome oznaku ako je rijec samo o web precacu, a ne instaliranoj PWA aplikaciji.
