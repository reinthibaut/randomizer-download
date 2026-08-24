# Rein's Randomizer — Download

Verdeel klastaken eerlijk en willekeurig over het hele schooljaar.

**→ [Downloadpagina](https://reinthibaut.github.io/randomizer-download/)**

Of pak de installer meteen:

- **Windows** — [ReinsRandomizer-Setup.exe](https://github.com/reinthibaut/randomizer-download/releases/latest/download/ReinsRandomizer-Setup.exe) (~80 MB, Windows 10 en 11, 64-bit) — versie 1.0.0
- **Mac** — [ReinsRandomizer.dmg](https://github.com/reinthibaut/randomizer-download/releases/latest/download/ReinsRandomizer.dmg) (~170 MB, macOS 11+, Apple Silicon en Intel) — versie 1.0.0
- **Linux** — [ReinsRandomizer.AppImage](https://github.com/reinthibaut/randomizer-download/releases/latest/download/ReinsRandomizer.AppImage) (elke distributie, zonder installeren) of
  [ReinsRandomizer.deb](https://github.com/reinthibaut/randomizer-download/releases/latest/download/ReinsRandomizer.deb) (Ubuntu, Mint, Debian)

## Wat doet het?

Je vult één keer in wie er in de klas zit en welke taken er te verdelen zijn. Daarna kiest de
app wie wat doet — willekeurig, maar wel eerlijk: hij houdt bij wie al aan de beurt is
geweest, zodat niet altijd dezelfde persoon de vervelende taak krijgt.

- **Naam sets** — lijsten met namen, bijvoorbeeld één per klas
- **Taken** — wat er verdeeld moet worden, zoals bord vegen of afval buitenzetten
- **Templates** — koppelen een naam set aan taken, aan de dagen waarop het telt, en aan de
  vakantieperiodes die overgeslagen worden
- **Volledig schema** — genereert in één keer het rooster voor het hele jaar, exporteerbaar
  als tekstbestand
- **Groepen** — verdeelt de klas in groepjes, met afwezigheden en herschudden

Bij **Tracking** onthoudt de app wie al geweest is en verdeelt hij eerlijk. Bij **Puur
willekeurig** telt elke keuze op zichzelf.

## Windows toont een waarschuwing — dat hoort zo

Als je het bestand opent, laat Windows een blauw kader zien:

> **Windows heeft uw pc beveiligd**
> Microsoft Defender SmartScreen heeft voorkomen dat een onbekende app is gestart.

Dat gebeurt bij elk programma dat niet bij Microsoft geregistreerd is, wat geld kost en de
moeite niet waard is voor een kleine app als deze. Om verder te gaan:

1. Klik op **Meer informatie** — de kleine grijze tekst in dat blauwe kader
2. Klik op **Toch uitvoeren** — de knop die onderaan verschijnt
3. Het gewone installatievenster opent; klik er verder doorheen zoals altijd

Liever niet? Vraag Rein gerust om het voor je te installeren.

## Op een Mac zijn er een paar stappen extra

Apple blokkeert apps die niet bij hen geregistreerd zijn, en laat je niet in één klik
doorgaan zoals Windows dat doet.

1. Open het `.dmg`-bestand en sleep **Rein's Randomizer** naar **Programma's**
2. Open **Programma's** en dubbelklik op **Rein's Randomizer** — macOS weigert:
   > **"Rein's Randomizer" is niet geopend** — Apple kon niet verifiëren of "Rein's
   > Randomizer" vrij is van malware die je Mac kan schaden of je privacy kan schenden.
3. Klik op **Gereed**. Hij moet één keer geweigerd worden voordat Apple je toestemming
   laat geven.
4. Open **Systeeminstellingen** → **Privacy en beveiliging**
5. Scroll naar beneden, naar **Beveiliging**. Klik op **Toch openen** naast "Rein's
   Randomizer is geblokkeerd om je Mac te beschermen."
6. Voer je Mac-wachtwoord in en klik nog een keer op **Toch openen**

Dit doe je maar één keer. Daarna opent hij zoals elke andere app.

**Op macOS Sonoma en eerder** gaat het sneller: rechtsklik op de app → **Open** → **Open**.
Apple heeft die snelkoppeling in nieuwere versies weggehaald.

## Op Linux

Linux heeft geen SmartScreen of Gatekeeper, dus er zijn geen waarschuwingen om door te
klikken. Voor de AppImage moet je hem eenmalig uitvoerbaar maken —
`chmod +x ReinsRandomizer.AppImage`, of rechtsklik → Eigenschappen → *Bestand als programma
uitvoeren toestaan*. De `.deb` installeer je door erop te dubbelklikken.

## Is dit veilig?

Het is een persoonlijk project, geen commercieel product. Het draait volledig op je eigen
computer — er wordt niets geüpload, er is geen account, en er is geen internetverbinding
nodig. Je namenlijsten en roosters staan alleen op je eigen machine.

## Verwijderen

**Windows** — **Instellingen** → **Apps** → **Rein's Randomizer** → **Verwijderen**.

**Mac** — open **Programma's**, sleep **Rein's Randomizer** naar de Prullenmand en leeg die.
Macs hebben geen uninstaller; iets wegslepen is daar de normale manier.

**Linux** — `sudo apt remove classroom-randomizer` voor de `.deb`. Een AppImage gooi je gewoon weg.

Je namenlijsten en roosters worden daarbij **niet** verwijderd — die staan apart, zodat
opnieuw installeren alles terugvindt. Wil je die ook wissen:

- **Windows** — <kbd>Win</kbd>+<kbd>R</kbd>, plak `%APPDATA%\classroom-randomizer`, Enter, verwijder de map
- **Mac** — in Finder <kbd>Cmd</kbd>+<kbd>Shift</kbd>+<kbd>G</kbd>, plak
  `~/Library/Application Support/classroom-randomizer`, Enter, sleep de map naar de Prullenmand
- **Linux** — verwijder de map `~/.config/classroom-randomizer`

Dat wist je namenlijsten, templates en geschiedenis definitief. Exporteer eerst je schema als
je het nog nodig hebt.

---

Deze repository bevat alleen de installer en deze pagina. De broncode van de app is privé.
