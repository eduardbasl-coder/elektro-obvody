# 📟 Elektronika - Teorie

# Popisky součástek

## Rezistor

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
