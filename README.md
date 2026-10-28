# Hospoda

Hospodské hry proti robotovi v jedné aplikaci pro iPhone: **prší**, **žolíky**, **kostky (farma)** (tři soupeři: Danek, Martin, Kokeš) a **herzky** (32 karet, proti třem robotům) a **mariáš** (volený, ve třech, zatím beta).
Všechny hry mají společnou peněženku (na začátku 100 grošů), hudbu na akordeon a nastavitelnou velikost písma. Hru o groše jde v menu úplně vypnout.

**Reputace a úrovně:** za každou výhru (prší 20, kostky 30, žolíky a herzky 40) a za splněné úkoly přibývají body reputace. Úroveň je vidět v Hospodě, každá další je náročnější (100, 150, 200 … bodů) a nejvyšší je úroveň 100.

**Úkoly od hospodského:** každý den 3 nové úkoly a jeden týdenní, s odměnou do peněženky. Úkoly se losují z data ze 79 šablon s náhodnými čísly, takže fungují i bez internetu a na všech telefonech vyjdou ve stejný den stejné. Stejný druh úkolu se vrátí nejdřív po 10 dnech a úplně stejné zadání nejdřív po měsíci. Kdo splní všechny tři úkoly několik dní po sobě, dostane rostoucí bonus.

**Hra na sekeru:** když dojdou peníze, hospodský půjčí 100 grošů a udělá čárku na tabuli. Dokud dluh trvá, jde polovina každé výhry na splátku. Nejvíc jsou tři čárky; kdo si půjčí počtvrté, tomu hospodský dluh odpustí, ale vynuluje skóre ve všech hrách.

## Soubory

| Soubor | K čemu je |
|---|---|
| `index.html` | celá aplikace (hry, úkoly, grafika, zvuky) |
| `manifest.webmanifest` | název a ikona, když se aplikace přidá na plochu |
| `sw.js` | uloží aplikaci do telefonu, takže jde hrát i bez internetu |
| `icon-192.png`, `icon-512.png`, `maskable-512.png`, `apple-touch-icon.png` | ikony aplikace |
| `launch-….png` (13 souborů) | úvodní obrázky pro různé iPhony, aby aplikace při spuštění neblikala bíle |

## Zveřejnění na GitHub Pages

1. Na GitHubu vytvoř nový veřejný repozitář, třeba `hospoda`.
2. Nahraj do něj všechny soubory: `Add file → Upload files`, vyber je všechny najednou (žádné složky nejsou potřeba), pak `Commit changes`. Pokud už repozitář máš, soubory jen přepiš. Staré složky `icons` a `splash` z dřívějška můžeš nechat i smazat, aplikace je už nepoužívá.
3. V repozitáři otevři `Settings → Pages`. U *Build and deployment* vyber *Source: Deploy from a branch*, větev `main` a složku `/ (root)`, ulož.
4. Po minutě až dvou bude aplikace na adrese `https://<tvoje-jméno>.github.io/<repozitář>/`.

## Instalace na iPhone

1. Adresu otevři v **Safari** (jiné prohlížeče na iPhonu na plochu přidávat neumí).
2. Klepni na tlačítko **Sdílet** (čtvereček se šipkou) → **Přidat na plochu** → **Přidat**.
3. Na ploše se objeví ikona Hospoda. Aplikace se otevírá přes celou obrazovku a po prvním spuštění jde i bez internetu.

## Úpravy a nové verze

Když změníš `index.html`, zvyš v `sw.js` číslo verze (`hospoda-v20` → `hospoda-v21`) a nahraj oba soubory. Telefon si novou verzi stáhne při dalším otevření s internetem (někdy je potřeba aplikaci zavřít a otevřít dvakrát).

Postup (peníze, reputace, skóre, sekera, úkoly, rozehrané hry) se ukládá jen v daném telefonu. Verze z Claude a verze z GitHubu mají každá svůj vlastní postup.
