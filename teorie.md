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
