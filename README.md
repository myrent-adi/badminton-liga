# Badminton Liga – Firebase Google prijava

Prva Firebase verzija postojećeg GitHub Pages projekta `myrent-adi/badminton-liga`.

## Što radi
- Google prijava bez dodatne lozinke.
- Prva prijava kreira `users/{UID}` sa statusom `pending`.
- Administrator iz `admins/{UID}` vidi zahtjeve i može odobriti/odbiti korisnike.
- Korisnici automatski vide promjenu statusa.
- PWA manifest i ikone za Android/iPhone.

**Ne sadrži još zajedničke rezultate, rang-listu, treninge ni push obavijesti.** Stara probna aplikacija s lokalnim rezultatima zamjenjuje se ovim ekranom; po želji prethodno sačuvajte staru verziju na računalu.

## Objavljivanje
1. Raspakirajte ZIP i prenesite `index.html`, `manifest.webmanifest`, `sw.js`, `README.md` i mapu `icons` u **korijen** postojećeg javnog repozitorija `myrent-adi/badminton-liga` (potvrdite zamjenu istoimenih datoteka).
2. Provjerite da GitHub Pages i dalje objavljuje `main` / `(root)`.
3. Otvorite https://myrent-adi.github.io/badminton-liga/ i kliknite „Nastavi s Googleom”.
4. U Firebase Console → Authentication → Users provjerite da postoji korisnik, a u Firestore → Data → `users` profil `pending`.

## Postavljanje prvog administratora (samo vlasnik projekta)
1. **Prvo se sami prijavite** Google računom u objavljenoj aplikaciji.
2. U aplikaciji na ekranu profila pronađite UID (možete ga naći i u Authentication → Users).
3. Otvorite Firestore → Data → Start collection, ID kolekcije `admins`.
4. Napravite dokument s **Document ID jednakim baš vašem UID-u**. Dodajte polje `label` (string) = `owner` (sadržaj nije bitan za provjeru; važna je prisutnost dokumenta).
5. Spremite, **odjavite se i ponovno prijavite** ili osvježite aplikaciju. Pojavit će se administratorska ploča.
6. Ne stvarajte administratorski dokument za nepoznate UID-ove. Prijava Googleom ne daje automatski administratorska prava.

## Sigurnosna pravila
Ova verzija očekuje objavljena pravila iz prethodnog koraka: korisnik može kreirati isključivo vlastiti `users/{UID}` dokument sa `displayName`, `email` i `status:'pending'`; samo admin može ažurirati korisnike; `admins` su klijentima samo za čitanje vlastitog zapisa; sve ostalo je zabranjeno. **Ne omogućujte test mode i ne postavljajte `allow read, write: if true`.**

## Napomene
- Google popup može biti blokiran na nekim mobitelima, osobito unutar aplikacijskih preglednika. Testirajte u Chromeu / Safariju. Za produkciju može biti potrebna zasebna prilagodba prijave za iPhone PWA.
- Za ovaj modul potreban je internet i dohvat Firebase SDK-a.
- Firebase web `apiKey` je javna konfiguracija, **nije administratorski ključ**. Zaštitu čine Firestore pravila.
- Preporučeno je prije šire uporabe testirati pravila emulatorom i postaviti App Check/ograničenja API ključa prema potrebi.
