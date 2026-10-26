<div align="center">

# 🐷 Purcel Overflow

**Un tower defense în browser în care porci roz invadează biroul unui programator.**
Pune capcane lângă hol, ține bullshit-ul jos și ai grijă ce aprobi când Claude vrea să ruleze comenzi.

### [▶ Joacă acum](https://cosminflrn.github.io/purcel-overflow/)

![Purcel Overflow, meniul principal](screenshots/meniu.png)

</div>

## Cum arată

| În joc | Alegerea nivelului |
|:---:|:---:|
| ![În joc](screenshots/joc.png) | ![Nivele](screenshots/nivele.png) |

<p align="center"><img src="screenshots/tutorial.png" alt="Tutorial" width="49%"></p>

## Ce găsești în joc

- 🏢 **6 nivele**, fiecare cu harta lui: Open Space, Sala de ședințe, Camera serverelor (cu lifturi), Bucătăria (cu podea udă), Team building (cu tiroliană și ring de dans) și Biroul CEO-ului
- 🪤 **8 capcane** cu câte 2 upgrade-uri:
  - de atac: Capsator, Imprimantă, Ventilator, Firewall, Feliator, Aspirator
  - de ajutor: Balonașe (îi prind în bule de săpun) și Espressor (face capcanele din jur mai rapide și mai puternice)
- ⏱️ **Contra cronometru**: ai timp limitat între runde, iar dacă pornești runda mai repede primești bonus de viteză
- 📊 **Statistici la final de nivel**: porci opriți, lei câștigați, răspunsuri corecte la Claude, timp și capcana vedetă
- ⏩ **Viteză 2x** pentru rundele în care apărarea ține, plus „Reia runda” și „Reia nivelul” din pauză
- ⏸️ **Pauză automată** când schimbi tabul; muzica merge mai departe (o oprești din butonul de sunet)
- 🐖 **10 tipuri de porci**, de la Porcul de birou până la Porcul Rege, care face pământul să tremure
- 💥 **Fiecare capcană are animația ei** când doboară un porc. Uneori sare și câte o friptură
- 🤖 **Claude Code** cere aprobare pentru comenzi. Aprobi ce e util, refuzi prostiile, iar bara de bullshit îți spune cum te descurci
- 🎵 **Muzică și sunete** diferite pe fiecare nivel, generate în întregime din cod
- 📱 **Merge pe orice ecran**: desktop, tabletă sau telefon. Pe telefon ocupă tot ecranul, iar butoanele stau departe de notch și de colțurile rotunjite

> **Pe iPhone:** Share → *Adaugă pe ecranul principal*, ca să-l ai pe tot ecranul, ca pe o aplicație.

## Cum e făcut

Tot jocul stă într-un singur fișier, [`index.html`](index.html), scris în **HTML + JavaScript simplu**, fără framework-uri, librării sau imagini externe.

- **Grafica** e desenată din cod pe un `<canvas>` HTML5, la fiecare cadru: porcii, programatorii, capcanele, hărțile și animațiile.
- **Muzica și efectele sonore** sunt sintetizate în timp real cu **Web Audio API**: oscilatoare, zgomot filtrat și un mic secvențiator pentru melodii.
- **Fontul** e [Nunito](https://fonts.google.com/specimen/Nunito), ales pentru diacriticele românești.
- **Progresul** se salvează în `localStorage`, în browser: doar hărțile deblocate și volumul. Fiecare nivel reluat pornește ca la prima joacă.
- **Hostingul** e gratuit, pe GitHub Pages. Fiecare push pe `main` actualizează jocul.
- **Balansul** a fost testat cu un bot care joacă singur nivelele în browser (Playwright), cu strategii „deștepte” și „naive”.

Jocul a fost construit de Cosmin împreună cu Claude, pornind de la un `.exe` simplu în C pentru Windows și ajungând la versiunea web de acum.

## Versiuni

Versiunea curentă apare în colțul din dreapta-jos al meniului. Fiecare versiune are și o ramură salvată (`versiune-v1.0` … `versiune-v10.0`).

| Versiune | Ce a adus |
|---|---|
| **v10.0** | Statistici la final de nivel, buton 2x, „Reia runda” / „Reia nivelul” în pauză, panou de upgrade mai aerisit, sunete noi (cronometru, upgrade maxim, porc nou, bonus de viteză), margine mai mică în dreapta pe telefon |
| v9.0 | Un singur mod de joc (cu cronometru), joc pe tot ecranul pe telefon cu butoanele în zona sigură, butonul de fullscreen ascuns când jocul e deja aplicație pe ecranul principal, „capcane de atac / de ajutor”, muzica se schimbă instant |
| v8.0 | Mod greu implicit și rebalansat, pauză automată la schimbarea tabului, tutorialul se închide la click în afară, explicații la Atac/Ajutor, Porcul Rege mai mic, progres simplificat, pluraluri corecte („20 de lei”, „1 porc”) |
| v7.0 | Mod greu (timp limitat între runde, bonus pentru start rapid, jocul merge și cu alt tab deschis), muzica se oprește la pauză, porc gurmand în meniu, balonașe și pentru Porcul Rege, lanțul regelui refăcut |
| v6.0 | Animații de moarte diferite pentru fiecare capcană, friptura, balonașe mai echilibrate, margini sigure pe telefon, fullscreen din meniu, tutorial mai rapid |
| v5.0 | Panou de upgrade nou, animații pentru balonașe, hărți refăcute, rebalansare |
| v4.0 | Capcane noi (Ventilator, Feliator, Aspirator), nivelul 6, muzică de final |
| v3.0 | Tutorial, slider de volum, diacritice, prompturi Claude fără repetări |
| v2.0 | Muzică pe nivele, tipuri noi de porci, buton de fullscreen |
| v1.0 | Prima versiune web |

**Rollback:** GitHub → Branches → alegi versiunea, sau `git checkout versiune-v5.0 -- index.html`, apoi commit și push pe `main`.

<p align="center">© Cosmin Florian</p>
