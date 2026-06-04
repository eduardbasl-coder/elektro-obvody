# Drátový Ovladač pro DC Motory (3-Motorový Systém) - v1.0

Tento projekt popisuje ruční ovladač a podvozek se třemi nezávisle ovládanými stejnosměrnými (DC) motory. Systém využívá mechanické konstrukce ze spájených DPS, napájení z externího adaptéru a bezpájecí svorkové propojení kabeláže.

## 🛠️ Seznam Součástek (BOM)

### Elektronika a Motory
* **3×** DC 5V motor (s koly podle schématu: 480mA, 80mA, 240mA)
* **3×** Spínací tlačítko (Push button)
* **3×** Zelená LED dioda (5mm)
* **3×** Rezistor 470 $\Omega$ (předřadné odpory pro LED)
* **1×** Rezistor 15 $\Omega$
* **1×** Rezistor 32 $\Omega$
* **1×** Rezistor 82 $\Omega$
* **1×** DC Jack konektor (samice na šasi/DPS)
* **1×** Napájecí adaptér 12V DC (síťový zdroj)

### Mechanické díly, upevnění a materiál
* **2×** DPS (PCB) o rozměru 6×4 cm
* **2×** DPS (PCB) o rozměru 8×3 cm
* **2×** 3-pinová šroubovací nebo páčková svorka
* **5 m** Propojovací kabel (celková metráž pro vedení a vnitřní spoje)
* **5 g** Pájecí cín (s tavidlem)
* **Sada** Stahovacích pásků (Zip-ties)
* **1×** Lepicí páska (Lepenka)

---

## 🏗️ Konstrukce a Mechanické Řešení

Projekt je rozdělen na dvě hlavní fyzické části vyrobené ze standardních plošných spojů (PCB) s kombinovaným mechanickým upevněním:

* **Ovladač (Kontroler):** Je tvořen ze **dvou slepených DPS o rozměru 6×4 cm**. Slouží jako ergonomická krabička/šasi pro uložení 3 tlačítek, indikačních LED diod, rezistorů a napájecího DC Jacku.
* **Podvozek:** Istalován ze **dvou DPS o rozměru 8×3 cm slepených do tvaru písmene „T“**. Tato konstrukce tvoří pevný nosný rám pro celý model.
* **Uchycení pohonu:** Kola a motory jsou k tomuto T-podvozku pevně a bezpečně fixovány pomocí kombinace **lepicí pásky (lepenky)** a **stahovacích pásků (zip-ties)**, což zajišťuje dostatečnou tuhost při jízdě a tlumí vibrace.

---

## 🔌 Zapojení a Kabeláž ve Svorkách

Propojení mezi ovladačem a jedoucí platformou (podvozkem) je řešeno flexibilně pomocí svorek, což umožňuje snadnou demontáž:

1. **Dlouhé vedení:** Z celkových 5 metrů kabelu je vytvořen **1,5m svazek**, který dává modelu dostatečnou volnost pohybu při jízdě.
2. **Svorkovnice:** Na straně ovladače i podvozku jsou osazeny **2× 3-pinové svorky**.
3. **Napájecí linie:** Tři samostatné napájecí vodiče (pro každý motor jeden) jsou pevně dotaženy ve svorkách, což zajišťuje spolehlivý kontakt bez nutnosti neustálého pájení při přenášení.
4. **Napájení:** Vstupní napětí z **napájecího adaptéru** vstupuje přes **DC jack konektor** rovnou do ovladače.

---

## 🕹️ Logika Ovládání



| Ovládací prvek | Akce | Výsledek |
| :--- | :--- | :--- |
| **Tlačítko 1** | Stisknuto | Roztočí se **1. motor** (480mA) |
| **Tlačítko 2** | Stisknuto | Roztočí se **2. motor** (80mA) |
| **Tlačítko 3** | Stisknuto | Roztočí se **3. motor** (240mA) |

---

## 🚀 Postup Montáže

1. **Slepení šasi:** Slepte k sobě dvě PCB 6×4 (ovladač) a dvě PCB 8×3 do tvaru "T" (podvozek).
2. **Montáž kol a motorů:** Umístěte motory na podvozek z PCB do požadované pozice. Omotejte je **lepenkou** pro prvotní fixaci a následně je pevně stáhněte **zip-ties (stahovacími pásky)** k desce plošného spoje.
3. **Pájení ovladače:** Osaďte tlačítka, LED diody, 470 $\Omega$ rezistory a výkonové rezistory (15 $\Omega$, 32 $\Omega$, 82 $\Omega$) podle schématu.
4. **Instalace svorek:** Připájejte 3-pinové svorky na ovladač i podvozek.
5. **Příprava kabelu:** Odměřte 1,5m přívodní kabel, odizolujte konce drátů a zajistěte je do svorek na obou stranách.
6. **Test:** Zapojte adaptér do DC Jacku a otestujte stiskem tlačítek funkčnost jednotlivých motorů.

##Závěr: Fail (Shořel 15 ohm rezistor u 480mA motoru, zakouřil jsem si pokoj a spálil si ruku..
#Verze v2.0 v přípravě
