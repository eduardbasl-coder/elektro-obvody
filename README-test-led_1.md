# 6-Kanálový LED Panel s Tlačítkovým Ovládáním - v1.0

Tento projekt popisuje konstrukci paralelně zapojeného indikačního panelu se šesti nezávisle ovládanými LED diodami. Systém využívá centralizovaný ochranný rezistor pro bezpečné napájení 3,3V LED diod z 12V DC napájecího zdroje a sdílenou zemní sběrnici.

## 🛠️ Seznam Součástek (BOM)

### Elektronika a Indikace
* **6×** Spínací tlačítko (Push button - čtyřpinové)
* **12×** LED dioda (5mm, různé barvy pro vizuální rozlišení: 2× červená, 2× hnědá/oranžová, 2× žlutá, 2× šedá/bílá, 2× zelená, 2× modrá - zapojené v sériových dvojicích)
* **1×** Výkonový rezistor (Společný předřadný odpor pro celou větev)
* **1×** Napájecí zdroj 12V DC (Laboratorní nastavitelný zdroj nebo síťový adaptér)

### Mechanické díly, vodiče a materiál
* **1×** Nepájivé pole (případně testovací podložka v simulátoru Tinkercad)
* **Sada** Propojovacích vodičů (červené pro kladnou větev, černé pro zemní sběrnici, modré pro propojovací uzly)

---

## 🏗️ Konstrukce a Mechanické Řešení

Projekt představuje modulární indikační matici uspořádanou do šesti samostatných vertikálních kanálů:

* **Ovládací rozhraní:** Každý kanál má své vlastní mechanické mačkací tlačítko, které slouží jako přímý spínač napájení pro danou sekci.
* **Optická signalizace:** Každý kanál obsahuje dvojici LED diod zapojených sériově nad sebou, což umožňuje zvýšit intenzitu světla nebo indikovat více stavů najednou.
* **Bezpečnostní prvek:** Namísto šesti samostatných rezistorů je v hlavní napájecí linii (+12V) umístěn jeden společný rezistor, který chrání aktivované LED diody před proudovým přetížením.

---

## 🔌 Zapojení a Kabeláž v Uzlech

Všechny kanály jsou zapojeny paralelně na společnou napájecí a zemní sběrnici:

1. **Hlavní napájecí linie (+):** Kladný pól zdroje (+12V) vede do společného ochranného rezistoru. Za rezistorem se červený vodič rozvětvuje ke spodnímu levému pinu každého ze 6 tlačítek.
2. **Spínaný uzel:** Horní levý pin každého tlačítka je spojen modrým vodičem s anodou (+) spodní LED diody v daném sloupci.
3. **Sériové propojení diod:** Katoda (-) spodní LED diody je přímo propojena (zelený můstek) s anodou (+) horní LED diody.
4. **Společná zemní sběrnice (-):** Katody (-) všech šesti horních LED diod jsou propojeny černým drátem do jedné dlouhé linie, která se na konci vrací přímo do záporného pólu (GND) 12V zdroje.

---

## 🕹️ Logika Ovládání



| Ovládací prvek | Akce | Výsledek |
| :--- | :--- | :--- |
| **Tlačítko 1 (vlevo)** | Stisknuto | Rozsvítí se **dvojice červených LED** |
| **Tlačítko 2** | Stisknuto | Rozsvítí se **dvojice hnědých/oranžových LED** |
| **Tlačítko 3** | Stisknuto | Rozsvítí se **dvojice žlutých LED** |
| **Tlačítko 4** | Stisknuto | Rozsvítí se **dvojice šedých/bílých LED** |
| **Tlačítko 5** | Stisknuto | Rozsvítí se **dvojice zelených LED** |
| **Tlačítko 6 (vpravo)** | Stisknuto | Rozsvítí se **dvojice modrých LED** |

---

## 🚀 Postup Montáže

1. **Umístění tlačítek:** Osaďte 6 tlačítek vedle sebe v rovnoměrných rozestupech tak, aby překonávala středový dělicí kanál pole.
2. **Osazení LED diod:** Nad každé tlačítko umístěte dvě LED diody nad sebe. Dbejte na správnou orientaci (anoda vždy směrem dolů k tlačítku, katoda nahoru k zemi).
3. **Propojení diod a tlačítek:** Propojte katodu spodní diody s anodou horní diody. Následně propojte spodní anodu s výstupním pinem tlačítka pomocí modrého drátu.
4. **Vytvoření zemní sběrnice:** Propojte všechny horní katody diod jedním souvislým černým vodičem a vyveďte jej na záporný pól zdroje (GND).
5. **Zapojení napájení a rezistoru:** Na kladný výstup zdroje (+12V) připojte ochranný rezistor. Od jeho konce rozveďte červené vodiče ke vstupním pinům všech tlačítek.
6. **Test:** Zapněte zdroj nastavený na 12V. Postupně mačkejte tlačítka a ověřte, že se vždy rozsvítí pouze konkrétní vertikální dvojice diod.

---

## Závěr: ⚠️ Upozornění (Nevýhoda společného rezistoru)
# Projekt úspěšně nasimulován, ale pozor při reálné stavbě! 🛠️
Při stisku **jednoho tlačítka** svítí diody správně. Pokud ale stisknete **více tlačítek najednou**, proud se rozdělí mezi více větví. Kvůli jednomu společnému rezistoru začnou LED diody při současném stisku svítit výrazně méně (pohasnou), a u barev s odlišným provozním napětím (např. červená vs. modrá) se může stát, že se některé větve nerozsvítí vůbec. Pro dokonalou verzi v2.0 by měl mít každý kanál svůj vlastní rezistor.
## Odkaz na schéma: https://www.tinkercad.com/things/ax5VUswUp5t-test-led-1
