# Silent Zagreb Badminton – faza 1 (novi izgled)

Ovo je nadogradnja postojećeg projekta `myrent-adi/badminton-liga`, a NE nova Firebase baza.

## Što radi
- Originalni logo iz dostavljene slike i nove PWA ikone.
- Mobilni dizajn prve slike: početna, kartice sljedećeg treninga/dolaznosti, prečaci i posljednji rezultati.
- Automatski tamni/svijetli prikaz prema postavkama sustava.
- Navigacija: Početna, Treninzi, Rezultati, Igrači, Više.
- Postojeća Google prijava, Firestore registracija, čekanje odobrenja i administratorsko odobravanje korisnika u izborniku Više.

## Što još NE radi
- Unos treninga i stvarno glasanje o dolasku.
- Unos rezultata, rang-lista, zajednička statistika i push obavijesti.
- Zato su ovi dijelovi označeni kao 'u pripremi' i nisu prikazani izmišljeni podaci.

## Sigurna objava
1. Na GitHubu napravite rezervnu kopiju postojeće verzije ili koristite prethodnu verziju u povijesti Git commita.
2. Raspakirajte ovaj ZIP; prenesite **sadržaj mape** `silent-zagreb-badminton-v1` u korijen postojećeg repozitorija, ne dodatnu ugniježđenu mapu.
3. Zamijenite `index.html`, `manifest.webmanifest`, `sw.js`, `icons/icon-192.png`, `icons/icon-512.png`, `README.md` i dodajte `assets/silent-zagreb-logo.jpg`.
4. GitHub: Commit changes. Pričekajte novu uspješnu Pages objavu.
5. Otvorite https://myrent-adi.github.io/badminton-liga/ i osvježite stranicu; na mobitelu po potrebi zatvorite i ponovno otvorite PWA kako bi se obnovila predmemorija.

## Sigurnost
- Ostaju postojeće Firebase postavke i projekt `badminton-liga-8d4ec`.
- Ovo izdanje ne mijenja Firestore Rules niti briše dokumente.
- Ne objavljujte privatne servisne ključeve; Firebase web konfiguracija je javna po dizajnu.
- Prije iduće faze proširite Firestore pravila ciljano za treninge i dolaznost, tako da statusi treninga budu vidljivi samo odobrenim članovima, a osobne agregirane statistike ostanu privatne.
