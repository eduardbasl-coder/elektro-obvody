# Tranzistorový Alarm při Přerušení Smyčky - v1.0

Tento projekt popisuje konstrukci jednoduchého zabezpečovacího systému (alarmu), který reaguje na přerušení hlídaného vodiče. Původní koncept navržený pro napětí 3,7V byl úspěšně modifikován pro bezpečný a spolehlivý provoz pod napětím 12V DC bez rizika zničení komponent.

## 🛠️ Seznam Součástek (BOM)

### Elektronika a Indikace
* **1×** Bipolární tranzistor NPN (BC547 nebo univerzální NPN z Tinkercadu)
* **1×** LED dioda (5mm, libovolná barva)
* **1×** Rezistor 100 k$\Omega$ (horní odpor napěťového děliče)
* **1×** Rezistor 1 k$\Omega$ (původně 10 k$\Omega$, upraveno pro stabilizaci báze při 12V)
* **1×** Rezistor 1 k$\Omega$ (nově přidaný předřadný odpor pro ochranu LED)
* **1×** Napájecí adaptér 12V DC (nebo laboratorní zdroj)

### Mechanické díly, vodiče a materiál
* **1×** Nepájivé pole (případně univerzální vrtaná DPS)
* **1×** Tenký propojovací vodič pro detekční smyčku (černý drát)
* **Sada** Propojovacích vodičů pro napájení a vnitřní spoje na poli
* **5 g** Pájecí cín (s tavidlem - volitelně pro finální verzi)

---

## 🏗️ Konstrukce a Mechanické Řešení

Projekt je navržen jako kompaktní poplašný modul, který hlídá celistvost připojené smyčky (např. drát natažený přes dveře, okno či chráněný objekt):

* **Detekční zóna:** Je tvořena fyzickou smyčkou z tenkého vodiče. Její narušení (přetrhnutí, přestřižení) okamžitě aktivuje poplachový stav.
* **Spínací centrum:** Srdcem obvodu je tranzistor BC547 pracující v režimu elektronického spínače, který nahrazuje složité řídicí mikroprocesory.
* **Úprava na 12V:** Oproti původnímu low-voltage návrhu (3,7V) obsahuje tato verze dodatečné ochranné prvky zabraňující destrukci indikační LED diody vysokým proudem a zajišťující plné zavírání tranzistoru.

---

## 🔌 Zapojení a Kabeláž v Uzlech

Celý obvod je postaven na principu napěťového děliče a řízení proudu do báze tranzistoru:

1. **Vstupní uzel napájení:** Kladný pól (+12V) je připojen na nově přidaný **1 k$\Omega$ ochranný rezistor**.
2. **Rozbočovací uzel:** Za tímto rezistorem se větev dělí přímo do **delší nožičky (anody) LED diody** a zároveň do **100 k$\Omega$ rezistoru**.
3. **Řízení báze (Napěťový dělič):** Proud z 100 k$\Omega$ rezistoru teče do prostřední nožičky (báze) tranzistoru. Z tohoto místa vede také **spodní 1 k$\Omega$ rezistor** spojený s černou detekční smyčkou.
4. **Uzavření obvodu:** Kratší nožička LED diody (katoda) je spojena s levou nožičkou tranzistoru (kolektor). Pravá nožička tranzistoru (emitor) a konec detekční smyčky jsou ukotveny na společné zemi (- / GND).

---

## 🕹️ Logika Ovládání


| Stav detekční smyčky | Chování tranzistoru BC547 | Výsledek (LED dioda) |
| :--- | :--- | :--- |
| **Smyčka je SPOJENÁ** | Napětí na bázi je staženo k nule, tranzistor je **ZAVŘENÝ** | **NESVÍTÍ** (Klidový stav) |
| **Smyčka je PŘERUŠENÁ** | Proud teče do báze, napětí stoupne nad 0,6V, tranzistor se **OTEVŘE** | **SVÍTÍ** (Poplachový stav) |

---

## 🚀 Postup Montáže

1. **Příprava pole / simulátoru:** Umístěte tranzistor BC547 (NPN) do nepájivého pole a identifikujte nožičky Kolektor (vlevo), Báze (uprostřed) a Emitor (vpravo).
2. **Instalace ochrany LED:** Zapojte první rezistor 1 k$\Omega$ na kladnou napájecí větev (+12V) a jeho druhý konec spojte s delší nožičkou (+) LED diody.
3. **Propojení indikační větve:** Kratší nožičku (-) LED diody propojte s kolektorem tranzistoru.
4. **Sestavení děliče:** Mezi delší nožičku LED diody a bázi tranzistoru zapojte rezistor 100 k$\Omega$.
5. **Zapojení smyčky:** Na bázi tranzistoru připojte druhý rezistor 1 k$\Omega$ a do série s ním zapojte hlídaný černý drát vedoucí na společnou zem (GND).
6. **Uzemnění:** Emitor tranzistoru propojte drátem přímo na hlavní mínus pól (- / GND) zdroje.
7. **Test:** Zapojte napájení 12V. LED dioda musí zůstat zhasnutá. Přerušte (odpojte) černý drát – LED dioda se musí okamžitě jasně rozsvítit.

---

## Závěr: 🎉 Úspěch (Verze 1.0 plně funkční bez kouře a popálenin!)
# Projekt úspěšně dokončen 🛠️
