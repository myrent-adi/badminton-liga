# Badminton Liga — PWA demonstracija

Probna aplikacija s 21 izmišljenim igračem, ručnim unosom rezultata i lokalnom rang-listom.

## Objavljivanje na GitHub Pages

1. Na GitHubu izradite **novi javni repozitorij** `badminton-liga`.
2. Odaberite **Add file → Upload files** i prenesite **sadržaj ove ZIP datoteke** (index.html, manifest.webmanifest, sw.js i mapu icons). Datoteke moraju biti u korijenu repozitorija, ne unutar dodatne mape.
3. Kliknite **Commit changes**.
4. Otvorite **Settings → Pages → Build and deployment**; za Source odaberite **Deploy from a branch**, a zatim **main** i **/(root)** te spremite.
5. Otvorite `https://myrent-adi.github.io/badminton-liga/` (ako su korisničko ime i naziv repozitorija upravo takvi).
6. iPhone: otvorite u Safariju → Dijeli → Dodaj na početni zaslon. Android: Chrome → izbornik ⋮ → Instaliraj ili Dodaj na početni zaslon.

## Važno

- Ovo je **demo bez Firebasea**. Rezultati ostaju samo na uređaju na kojem su uneseni, u localStorage.
- Drugi igrači ne vide unesene rezultate.
- Primjer prikazuje **pojedinačne mečeve** (1 na 1), standardne setove do 21 / 30 i 3 boda za pobjedu.
- Za zajedničku ligu treba dodati Firebase Authentication, Firestore i sigurnosna pravila.
- GitHub Pages objavljuje izvorni kod javno. Ne unosite osobne podatke ili lozinke u repozitorij.
