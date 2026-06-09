# 📟 Elektronika - Teorie

# Popisky součástek

##  Ω Rezistor

### Základní informace
- Typ: Pasivní elektronická součástka
- Kategorie: Rezistory
- Jednotka: Ohm (Ω)
- Polarita: Ne (lze zapojit libovolným směrem)
- Schématická značka: R
- Hlavní funkce: Omezení proudu a vytvoření úbytku napětí
- Typické hodnoty: 1 Ω až několik MΩ
- Typické výkony: 0,125 W, 0,25 W, 0,5 W, 1 W a více

### Popis
Rezistor omezuje průchod elektrického proudu v obvodu a vytváří úbytek napětí.

### Použití
- Omezení proudu pro LED (aby člověk neodpalil 3,3V LED 12 Volty
- Dělič napětí
- Pull-up a pull-down rezistory u tlačítek
- Ochrana elektronických součástek před příliš velkým proudem
- Nastavení pracovních bodů tranzistorů

### Jak se zapojuje
Rezistor se zapojuje sériově nebo paralelně podle účelu. Nemá polaritu, takže nezáleží na orientaci.

### Důležité parametry
- Odpor: Udává velikost odporu vůči elektrickému proudu (Ω)
- Výkon: Maximální výkon, který může rezistor bezpečně rozptýlit (W)
- Tolerance: Přesnost hodnoty odporu (%)
### Praktické poznámky
- Rezistor nemá polaritu.
- Při překročení maximálního výkonu se zahřívá a může shořet.
- Před zapojením LED je potřeba vypočítat vhodný rezistor.
- Hodnotu lze určit podle barevného kódu nebo změřit multimetrem.
- Začátečníci často podcení výkonovou ztrátu na rezistoru.

### Příklady použití

- Omezení proudu pro LED diodu (např. 220 Ω u 5V)
- Pull-up rezistor u tlačítek (např. 10 kΩ)
- Pull-down rezistor u vstupů mikrokontrolérů (Arduino, ESP32)
- Dělič napětí (např. pro snížení 12V na 5V signál)
- Nastavení pracovního bodu tranzistoru (biasování)
- Ochrana vstupů IC (Integrated Circuit = integrovaný obvod) před přepětím

### Vzorečky
### Vzorečky

#### Ohmův zákon
U = R × I  
R = U / I  
I = U / R  

- U = napětí (V)
- R = odpor (Ω)
- I = proud (A)

---

#### Elektrický výkon
P = U × I  
P = I² × R  
P = U² / R  

- P = výkon (W)

---

#### Sériové zapojení rezistorů
R = R₁ + R₂ + R₃ + ...

---

#### Paralelní zapojení rezistorů
1/R = 1/R₁ + 1/R₂ + 1/R₃ + ...

pro dva rezistory:
R = (R₁ × R₂) / (R₁ + R₂)

## ⚡ Kondenzátor

### Základní informace
- Typ: Pasivní elektronická součástka
- Kategorie: Kondenzátory
- Jednotka: Farad (F)
- Polarita: Záleží (elektrolytické ano, keramické ne)
- Schématická značka: C
- Hlavní funkce: Skladování elektrické energie v elektrickém poli
- Typické hodnoty: pF až mF (velmi malé až střední kapacity)
- Typické napětí: od několika V po stovky V (dle typu)

### Popis
Kondenzátor ukládá elektrickou energii v elektrickém poli mezi dvěma elektrodami oddělenými dielektrikem.

### Použití
- Filtrace napájení (vyhlazení napětí)
- Zpožďovací obvody (RC časování)
- Oddělení stejnosměrné složky signálu (AC coupling)
- Stabilizace napájení mikrokontrolérů (decoupling)
- Tlumicí obvody a potlačení šumu

### Jak se zapojuje
Kondenzátor se zapojuje paralelně nebo sériově podle aplikace. U elektrolytických kondenzátorů je nutné dodržet polaritu (+ a -).

### Důležité parametry
- Kapacita: Množství uloženého náboje (F)
- Napětí: Maximální dovolené napětí
- Tolerance: Přesnost kapacity (%)
- ESR (Equivalent Series Resistance): Vnitřní odpor kondenzátoru

### Praktické poznámky
- Elektrolytické kondenzátory mají polaritu (mohou explodovat při špatném zapojení).
- Keramické kondenzátory polaritu nemají.
- Při zapnutí napájení pomáhají stabilizovat napětí.
- Často se dávají co nejblíže k IC (integrovaný obvod).
- V RC obvodu se nabíjí a vybíjí exponenciálně.

### Příklady použití
- 100nF kondenzátor u každého mikrokontroléru (decoupling)
- 10µF – 1000µF pro vyhlazení napájení
- RC časovače (např. zpoždění zapnutí LED)
- Audio filtry (oddělení DC složky)
- Reset obvody mikrokontrolérů

### Vzorečky

#### Základní vztah kapacity
C = Q / U  

- C = kapacita (F)
- Q = náboj (C)
- U = napětí (V)

---

#### Energie v kondenzátoru
E = 1/2 × C × U²  

- E = energie (J)

---

#### RC časová konstanta
τ = R × C  

- τ = časová konstanta (s)
- R = odpor (Ω)
- C = kapacita (F)

---

#### Nabíjení / vybíjení (základní idea)
U(t) = U₀ × (1 - e^(-t/RC))  (nabíjení)  
U(t) = U₀ × e^(-t/RC)        (vybíjení)

## 🎚️ Potenciometr

### Základní informace
- Typ: Pasivní elektronická součástka (proměnný rezistor)
- Kategorie: Rezistory
- Jednotka: Ohm (Ω)
- Polarita: Ne
- Schématická značka: VR / R (s šipkou)
- Hlavní funkce: Nastavitelný odpor (dělič napětí)
- Typické hodnoty: 1 kΩ až 1 MΩ
- Typické výkony: 0,1 W – 1 W

### Popis
Potenciometr je nastavitelný rezistor, který mění odpor pomocí mechanického otočného kontaktu (nebo posuvníku).

### Použití
- Regulace hlasitosti (audio)
- Nastavení jasu LED
- Dělič napětí (analogový vstup pro Arduino/ESP32)
- Kalibrace obvodů
- Ovládací prvky (knoflíky)

### Jak se zapojuje
Má tři vývody:
- krajní piny = pevný odpor
- střední pin = jezdec (wiper)

Použití:
- jako dělič napětí (3 piny)
- jako proměnný rezistor (2 piny: jezdec + jeden krajní)

### Důležité parametry
- Odpor: celkový odpor mezi krajními piny
- Výkon: maximální ztrátový výkon
- Tolerance: přesnost odporu
- Lineární / logaritmická charakteristika

### Praktické poznámky
- Nejčastěji selhává mechanickým opotřebením
- Logaritmické potenciometry se používají v audiu
- Lineární se používají pro měření (Arduino analog input)
- Špatné zapojení může způsobit „skokové“ hodnoty
- Při použití jako dělič nikdy nepřetěžovat proudem

### Příklady použití
- Ovládání jasu LED
- Ovládání hlasitosti zesilovače
- Analogový vstup (Arduino A0)
- Nastavení referenčního napětí
- Trimry pro ladění obvodů

### Vzorečky

#### Dělič napětí (potenciometr)
Uout = Uin × (R2 / (R1 + R2))

- Uout = výstupní napětí
- Uin = vstupní napětí
- R1, R2 = části odporu

---

#### Ohmův zákon (platí i pro část potenciometru)
U = R × I  

---

#### Výkon ztráty
P = U × I  
P = I² × R  
P = U² / R

## 💡 LED dioda (3,3V)

### Základní informace
- Typ: Aktivní polovodičová součástka
- Kategorie: Dioda / LED
- Jednotka: Volt (V) – dopředné napětí
- Polarita: Ano (anoda +, katoda -)
- Schématická značka: LED (dioda se šipkami ven)
- Hlavní funkce: Přeměna elektrické energie na světlo
- Typické napětí: ~3,0 V – 3,3 V (bílá/modrá LED)
- Typický proud: 5 mA – 20 mA

### Popis
LED dioda (Light Emitting Diode) je polovodičová součástka, která svítí při průchodu elektrického proudu v propustném směru.

### Použití
- Indikace stavu (ON/OFF)
- Osvětlení (např. pásky, lampy)
- Signalizace v elektronice
- Arduino/ESP32 projekty
- Debugging (vizuální kontrola obvodu)

### Jak se zapojuje
LED se zapojuje vždy **v sérii s rezistorem**, který omezuje proud.

- Anoda (+) → napájení přes rezistor
- Katoda (-) → GND (zem)

⚠️ Nikdy nepřipojuj přímo na napětí bez rezistoru.

### Důležité parametry
- Dopředné napětí (Vf): ~3,3 V (pro bílou/modrou LED)
- Proud (If): obvykle 10–20 mA
- Svítivost: mcd (millicandela)
- Úhel svitu: např. 30°–120°
- Maximální proud: nesmí být překročen

### Praktické poznámky
- LED má polaritu → obrácené zapojení nesvítí
- Bez rezistoru se velmi rychle zničí
- Modré a bílé LED mají vyšší napětí (~3,0–3,3 V)
- Červené LED mají nižší napětí (~1,8–2,2 V)
- Jas se dá řídit PWM (Pulse Width Modulation = řízení výkonu pulzy)
- Přehřátí zkracuje životnost
- Delší nožička = katoda | Kratší = anoda

### Příklady použití
- Stavová LED na mikrokontroléru
- Indikace napájení (power LED)
- RGB LED indikace
- Blikání (debug signály)
- Osvětlení v DIY projektech

### Vzorečky

#### Výpočet rezistoru pro LED
R = (Uin - Vf) / I

- R = odpor rezistoru (Ω)
- Uin = napájecí napětí (V)
- Vf = dopředné napětí LED (V)
- I = proud LED (A)

---

#### Ohmův zákon (pro LED obvod)
U = R × I  

---

#### Výkon rezistoru v LED obvodu
P = (Uin - Vf) × I

## 🔀 Tranzistor

### Základní informace
- Typ: Aktivní polovodičová součástka
- Kategorie: Tranzistory
- Jednotka: Beze specifické jednotky (řídicí prvek)
- Polarita: Záleží (NPN/PNP nebo N/MOSFET)
- Schématická značka: Q / T
- Hlavní funkce: Spínání a zesilování elektrického signálu
- Typické napětí: jednotky V až desítky V (dle typu)
- Typický proud: mA až A (dle typu)

### Popis
Tranzistor je elektronický spínač nebo zesilovač, který ovládá velký proud pomocí malého řídicího signálu.

### Použití
- Elektronické spínání (ON/OFF)
- Zesilovače signálu
- Řízení motorů (DC motor, ventilátory)
- PWM řízení (PWM = Pulse Width Modulation, řízení výkonu pulzy)
- Logické obvody (digitální elektronika)
- Řízení výkonových zátěží

### Jak se zapojuje

#### BJT (Bipolar Junction Transistor)
- Vývody: B (báze), C (kolektor), E (emitor)
- Malý proud do báze řídí větší proud mezi kolektorem a emitorem
- Použití jako spínač nebo zesilovač

#### MOSFET (Metal-Oxide Semiconductor Field-Effect Transistor)
- Vývody: G (gate), D (drain), S (source)
- Napětí na gate řídí proud mezi drain a source
- Vhodný pro vyšší proudy a účinné spínání

### Důležité parametry
- Vce / Vds: maximální napětí mezi vývody
- Ic / Id: maximální proud
- Hfe (BJT): zesílení proudu
- Rds(on) (MOSFET): odpor v sepnutém stavu
- Gate threshold voltage (MOSFET): napětí pro sepnutí

### Praktické poznámky
- Špatné zapojení může tranzistor zničit okamžitě
- MOSFET je efektivnější pro spínání výkonu než BJT
- BJT potřebuje proud do báze, MOSFET jen napětí
- Při spínání indukčních zátěží (motor) je nutná ochranná dioda
- Často se používá rezistor na bázi/gate pro omezení proudu

### Příklady použití
- Spínání LED pásků
- Ovládání DC motorů
- Relé driver (ovládání relé)
- Logické zesílení signálu z mikrokontroléru
- PWM regulace ventilátorů

### Vzorečky

#### Základní zesílení BJT
Ic = β × Ib  

- Ic = kolektorový proud
- Ib = proud báze
- β = zesílení tranzistoru

---

#### Ohmův zákon (pro řídicí obvody)
U = R × I  

---

#### Výkon ztráty
P = U × I  
P = I² × R  
P = U² / R

## 🔋 Dioda

### Základní informace
- Typ: Aktivní polovodičová součástka
- Kategorie: Dioda
- Jednotka: Volt (V) – dopředné napětí (Uf)
- Polarita: Ano (anoda +, katoda -)
- Schématická značka: D
- Hlavní funkce: Propouští proud pouze jedním směrem
- Typické napětí: ~0,7 V (křemíková), ~0,2–0,3 V (Schottky)
- Typický proud: mA až A (dle typu)

### Popis
Dioda je polovodičová součástka, která vede elektrický proud pouze v jednom směru a blokuje proud v opačném směru.

### Použití
- Ochrana proti přepólování napájení
- Usměrnění AC na DC (usměrňovače)
- Ochrana proti zpětnému napětí (např. motory, relé)
- Signálové oddělení
- Spínací obvody

### Jak se zapojuje
- Anoda (+) → vstup napětí
- Katoda (-) → výstup / GND

⚠️ Dioda musí být zapojená správně polaritně, jinak nevede proud.

### Důležité parametry
- Uf (forward voltage): úbytek napětí v propustném směru
- If: maximální proud v propustném směru
- Vr: maximální zpětné napětí
- Recovery time: rychlost přepínání (u rychlých diod)

### Praktické poznámky
- Špatné zapojení = dioda nefunguje (nebo se poškodí při přepětí)
- Vždy má úbytek napětí (~0,7 V u křemíku)
- Používá se jako ochrana proti „reverse polarity“
- U motorů se používá flyback dioda (ochrana proti indukčnímu napětí)
- LED je speciální typ diody (svítí)

### Příklady použití
- Ochrana napájení (proti přepólování baterie)
- Usměrňovací můstek (AC → DC)
- Ochrana relé a motorů (flyback dioda)
- Signálové obvody
- Logické OR spojování signálů (diodová logika)

### Vzorečky

#### Úbytek napětí na diodě
Uout = Uin - Uf  

---

#### Výkon na diodě
P = Uf × I  

- P = výkon (W)
- Uf = úbytek napětí
- I = proud

---

#### Proud v propustném směru (ideální model)
I ≈ 0 (v závěrném směru)
I > 0 (v propustném směru)

## 🧲 Cívka (Induktor)

### Základní informace
- Typ: Pasivní elektronická součástka
- Kategorie: Induktory
- Jednotka: Henry (H)
- Polarita: Ne
- Schématická značka: L
- Hlavní funkce: Ukládání energie do magnetického pole
- Typické hodnoty: µH až H
- Typický proud: mA až desítky A (dle typu)

### Popis
Cívka je součástka, která ukládá energii do magnetického pole při průchodu elektrického proudu. Brání rychlým změnám proudu v obvodu.

### Použití
- DC-DC měniče (Buck/Boost Converter)
- Filtrace napájení
- Potlačení šumu
- Relé a elektromagnety
- Transformátory
- Rádiové a vysokofrekvenční obvody

### Jak se zapojuje
Cívka se zapojuje sériově nebo paralelně podle účelu. Nemá polaritu, takže ji lze zapojit libovolným směrem.

### Důležité parametry
- Indukčnost: Schopnost ukládat energii do magnetického pole (H)
- Maximální proud: Proud, který může cívkou protékat bez poškození
- DC odpor (DCR): Odpor vinutí cívky
- Saturační proud: Proud, při kterém se jádro začne magneticky saturovat

### Praktické poznámky
- Cívka nemá polaritu.
- Brání rychlým změnám proudu.
- Při náhlém odpojení proudu může vytvořit vysoké napětí.
- Proto se u relé a motorů používá ochranná dioda (flyback dioda).
- Ve spínaných zdrojích je jednou z nejdůležitějších součástek.

### Příklady použití
- Buck Converter (12V → 5V)
- Boost Converter (5V → 12V)
- Relé
- Elektromagnetický zámek
- Filtrace napájení mikrokontrolérů
- Potlačení elektromagnetického rušení (EMI)

### Vzorečky

#### Indukčnost
U = L × (dI/dt)

- U = napětí (V)
- L = indukčnost (H)
- dI/dt = rychlost změny proudu

---

#### Energie uložená v cívce
E = 1/2 × L × I²

- E = energie (J)
- L = indukčnost (H)
- I = proud (A)

---

#### Reaktance cívky (AC)
XL = 2 × π × f × L

- XL = induktivní reaktance (Ω)
- f = frekvence (Hz)
- L = indukčnost (H)

## 🔘 Tlačítko

### Základní informace
- Typ: Elektromechanická součástka
- Kategorie: Spínače
- Jednotka: Nemá
- Polarita: Ne
- Schématická značka: SW
- Hlavní funkce: Dočasné spojení nebo rozpojení obvodu po stisku
- Typické napětí: dle typu
- Typický proud: dle typu

### Popis
Tlačítko je spínací prvek, který po stisku změní stav obvodu. Po uvolnění se vrátí do původního stavu.

### Použití
- Uživatelský vstup
- Reset tlačítka
- Ovládání mikrokontrolérů
- Spouštění funkcí zařízení
- Nouzové vypínače

### Jak se zapojuje
Tlačítko se nejčastěji zapojuje s pull-up nebo pull-down rezistorem, aby vstup neměl nedefinovaný stav.

### Důležité parametry
- Maximální napětí
- Maximální proud
- Počet kontaktů
- Životnost (počet sepnutí)

### Praktické poznámky
- Nemá polaritu.
- Bez pull-up nebo pull-down rezistoru může být stav vstupu nestabilní.
- Mechanická tlačítka často trpí zákmity kontaktů (debouncing).
- Většina mikrokontrolérů má interní pull-up rezistory.

### Příklady použití
- Reset tlačítko na Arduino
- Zapnutí LED po stisku
- Ovládání menu na displeji
- Spuštění programu na ESP32

### Vzorečky

Tlačítko samo o sobě nemá vlastní důležité vzorce.
Nejčastěji se používá s Ohmovým zákonem a pull-up/pull-down rezistory.

## 🎚️ Přepínač

### Základní informace
- Typ: Elektromechanická součástka
- Kategorie: Spínače
- Jednotka: Nemá
- Polarita: Ne
- Schématická značka: SW
- Hlavní funkce: Trvalé spojení nebo rozpojení obvodu
- Typické napětí: dle typu
- Typický proud: dle typu

### Popis
Přepínač umožňuje ručně měnit stav obvodu a po přepnutí zůstává ve zvolené poloze.

### Použití
- Hlavní vypínače zařízení
- Volba režimu zařízení
- Zapnutí a vypnutí napájení
- Přepínání mezi obvody

### Jak se zapojuje
Přepínač se zapojuje sériově s obvodem, který má ovládat. Nemá polaritu.

### Důležité parametry
- Maximální napětí
- Maximální proud
- Počet pólů a pozic
- Typ kontaktů (SPST, SPDT, DPDT)

### Praktické poznámky
- Nemá polaritu.
- Musí být dimenzován na očekávaný proud.
- Pro vyšší proudy se používají výkonové přepínače.
- Mechanické kontakty se mohou časem opotřebovat.

### Příklady použití
- ON/OFF vypínač napájení
- Přepnutí mezi bateriovým a síťovým napájením
- Volba provozního režimu zařízení
- Ovládání ventilátoru

### Vzorečky

Přepínač nemá vlastní důležité vzorce.
Při návrhu obvodu se používá Ohmův zákon a výpočty proudu zátěže.
