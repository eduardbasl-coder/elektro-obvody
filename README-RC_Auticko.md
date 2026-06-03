# Drátový Ovladač pro DC Motory (3-Motorový Systém)

Tento projekt popisuje zapojení a princip fungování jednoduchého ručního ovladače pro nezávislé ovládání tří stejnosměrných (DC) motorů pomocí tlačítek. Systém je napájen z jednoho centrálního zdroje přes napájecí konektor.

## 🛠️ Technické Specifikace

### Napájení
* **Vstupní napájení:** 12V DC (přes 12V DC Jack)
* **Pracovní napětí motorů:** 5V DC

### Komponenty
* **1. motor:** DC 5V motor s kolem (Odběr: **480 mA**)
* **2. motor:** DC 5V motor s kolem (Odběr: **80 mA**)
* **3. motor:** DC 5V motor se 2 koly (Odběr: **240 mA**)
* **Ovládací prvky:** 3× spínací tlačítko (Push button) s indikační LED diodou a rezistorem
* **Kabeláž:** Propojovací kabel o délce **1,5 m** (zajišťuje manipulační prostor pro jízdu)

---

## 🕹️ Logika Ovládání

Každé tlačítko na ovladači ovládá právě jeden konkrétní motor. Motor je v provozu pouze po dobu fyzického stisknutí příslušného tlačítka.


| Ovládací prvek | Akce | Výsledek |
| :--- | :--- | :--- |
| **Tlačítko 1** | Stisknuto | Roztočí se **1. motor** (480mA) |
| **Tlačítko 2** | Stisknuto | Roztočí se **2. motor** (80mA) |
| **Tlačítko 3** | Stisknuto | Roztočí se **3. motor** (240mA) |

---

## 🔌 Schéma Zapojení

Celý systém sdílí společnou zem (GND) a napájecí větve. Detaily zapojení:

1. **Napájecí uzel:** Hlavní přívod energie je realizován přes `12V DC Jack`.
2. **Indikace a ochrana:** U každého tlačítka je zapojena indikační LED dioda s ochranným předřadným rezistorem, která signalizuje sepnutí okruhu.
3. **Dlouhé vedení:** Mezi ovládacím panelem (tlačítky) a samotnými motory je zařazen `1,5m kabel`, který funguje jako pupeční šňůra pro zachování mobility modelu.

---

## 🚀 Zprovoznění

1. Připojte stabilizovaný napájecí zdroj do **12V DC Jacku**.
2. Rozviňte **1,5m kabel**, aby měl model dostatek prostoru pro pohyb.
3. Stisknutím jednotlivých tlačítek otestujte funkčnost a směr otáčení každého motoru.
