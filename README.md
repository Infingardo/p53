# p53 IHC - Quando richiederla e come interpretarla v2.1

**Tool diagnostico per decisione clinica e interpretazione pattern-based in displasia epiteliale**

🔗 **[Apri il tool](https://infingardo.github.io/calcolatore-p53/)**

📖 **[Scarica "p53 for dummies" (PDF)](https://github.com/infingardo/p53-for-dummies/raw/main/p53_for_dummies.pdf)** - Manuale pratico per patologi (Bianchi F, 2025)

---

## 🎯 Scopo

Questo tool aiuta il patologo a rispondere a due domande pratiche:

1. **"Devo fare la p53 IHC?"** → Decision helper con calcolo utilità diagnostica
2. **"Come interpreto il risultato?"** → Cutoff organo-specifici validati + pattern recognition

---

## 🔬 Organi supportati

- **Stomaco** (displasia gastrica)
- **Colon** (displasia colonica + IBD-associated)
- **Vescica** (displasia uroteliale)
- **Esofago** (Barrett's)
- **Laringe** (displasia laringea)

---

## 📊 Features principali

### 🤔 Tab 1: "Devo fare la p53?"

**Input:**
- Organo + dubbio diagnostico (reattivo vs LGD, LGD vs HGD, etc.)
- Citologia nucleare (normale/borderline/atipia)
- Contesto clinico (infiammazione, H. pylori, IBD, etc.)

**Output:**
- Raccomandazione (🟢 SÌ / 🟡 OPZIONALE / 🔴 NO)
- Calcolo utilità diagnostica (%)
- Guida interpretativa anticipata per ogni scenario
- Context-aware warnings (IBD attiva, H. pylori, etc.)

**Esempi:**
- *Vescica, iperplasia vs LGD, nuclei borderline, no infiammazione* → 🟢 **p53 RACCOMANDATO (75%)**
- *Colon IBD attiva, indefinite, nuclei borderline, infiammazione marcata* → 🔴 **p53 NON RACCOMANDATO ORA (20%)**
- *Stomaco, H. pylori+, reattivo vs LGD, nuclei borderline* → 🟡 **p53 OPZIONALE (50%)** - eradica prima

---

### 🔬 Tab 2: "Interpreto il risultato"

**Input:**
- Organo
- % nuclei positivi (slider 0-100%)
- Intensità (1+/2+/3+/misto)
- Distribuzione (mosaico/focale/diffuso)
- Controllo interno (forte/debole/assente)
- Pattern speciale (null/citoplasmatico/rim-like)
- **Ki67** (opzionale, per disambiguare zona grigia)

**Output:**
- Pattern grading (Wild-type / Accumulo lieve / Over-expression / Null / NI)
- **Visualizzazione grafica** con cutoff organo-specifico
- Interpretazione correlata al dubbio iniziale
- **Integrazione Ki67** (se disponibile)
- Testo referto copiabile
- Confidence score (0-100%)

**Cutoff organo-specifici validati:**

| Organo | Wild-type | Zona grigia | Over-expression |
|--------|-----------|-------------|-----------------|
| Stomaco | <10% | 10-60% | **>60%** diffuso |
| Colon | <20% | 20-60% | **>60%** diffuso |
| Vescica | <10% | 10-50% | **>50%** diffuso |
| Esofago | <10% | 10-60% | **>60%** diffuso |
| Laringe | <10% | 10-50% | **>50%** full-thickness |

**Ki67 - Criteri supportivi (zona grigia p53):**

| Organo | Normale | Favorisce displasia |
|--------|---------|---------------------|
| Stomaco | <10% basale | **>30% esteso ai 2/3 superiori** |
| Colon | Basale (cripta profonda) | **Estensione ai 2/3 medi-superficiali** |
| Vescica | Superficiale | **Full-thickness** |
| Esofago/Laringe | Basale | **Full-thickness** |

---

### 📚 Tab 3: "Reference rapido"

- Tabelle cutoff tutti gli organi
- Decision matrix (quando fare p53)
- Pattern recognition rapido (WT/OE/null/citoplasmatico)
- Ki67 integrazione
- Le 7 trappole della p53
- Discordanza immuno/molecolare
- Bibliografia essenziale

---

## 🚀 Uso

1. Apri il tool (link sopra)
2. **Tab 1** → Decidi se fare p53 (inserisci scenario clinico)
3. **Tab 2** → Interpreta il risultato (dopo aver fatto p53)
4. **Tab 3** → Consulta reference al bisogno

Tool **standalone**, nessuna dipendenza, funziona **offline**.

---

## 💡 Use case tipici

### Caso 1: Vescica - iperplasia vs LGD
*Hai dubbio tra iperplasia reattiva e displasia uroteliale*

1. **Tab 1:** Inserisci vescica + "reattivo vs LGD" + nuclei borderline → Output: 🟢 **p53 RACCOMANDATO (75%)**
2. Ordini p53 → risultato: 55% nuclei positivi 2+/3+, diffuso
3. **Tab 2:** Inserisci i dati → Output: 🟠 **Over-expression** (>50% cutoff vescica) → "Displasia confermata su base di iperplasia reattiva"
4. Copi il testo referto → fatto!

### Caso 2: Colon IBD - indefinite per displasia
*IBD attiva, atipia borderline, vuoi sapere se p53 aiuta*

1. **Tab 1:** Inserisci colon IBD + "indefinite" + nuclei borderline + IBD attiva → Output: 🔴 **p53 NON RACCOMANDATO ORA (20%)** - "Infiammazione può dare accumulo stress, ripeti dopo remissione"
2. Non ordini p53 → tratti IBD → ripeti biopsia
3. Se dopo remissione persiste atipia → **ALLORA** fai p53

### Caso 3: Stomaco - zona grigia p53 + Ki67 alto
*p53 35% focale, dubbio se displasia o stress*

1. **Tab 2:** Inserisci p53 35% + Ki67 >30% esteso → Output: "Accumulo lieve MA Ki67 concordante favorisce displasia"
2. Diagnosi: LGD probabile, follow-up stretto

---

## 📚 Bibliografia essenziale

- **Bianchi F.** p53 for dummies. Manuale pratico per patologi. 2025 [[Scarica PDF](https://github.com/infingardo/p53-for-dummies/raw/main/p53_for_dummies.pdf)] [*Fonte primaria per trappole interpretative, workflow pratico*]
- **Fassan M, et al.** p53 and Ki67 expression profiles identify clinically relevant gastric dysplasia. *Mod Pathol* 2014;27:1409-1417 [*Cutoff gastrico, Ki67 integrazione*]
- **Köbel M, Ronnett BM, Singh N, et al.** Interpretation of P53 Immunohistochemistry in Endometrial Carcinomas: Toward Increased Reproducibility. *Int J Gynecol Pathol* 2019;38:S123-S131 [*Pattern-based standard*]
- **Vermij L, et al.** p53 immunohistochemistry in endometrial cancer: clinical and molecular correlates in the PORTEC-3 trial. *Mod Pathol* 2022;35:1475-1483 [*Correlazione IIC/molecolare in carcinomi, 408 casi*]
- **Osakabe M, et al.** The pattern-based interpretation of p53 immunohistochemical expression as a surrogate marker for TP53 mutations in colorectal cancer. *Virchows Arch* 2025;486:333-341 [*Validazione colon-retto, 91.3% concordanza*]
- **WHO Classification of Tumours Editorial Board.** Digestive System Tumours. 5th ed. Lyon: IARC, 2019/2022 [*Standard classificazione displasie*]
- **Rugge M, et al.** MAPS II: Management of precancerous conditions and lesions in the stomach. *Gut* 2019;68:1743-1752 [*Management gastrico*]

---

## ⚠️ Disclaimer

**Tool per supporto diagnostico.** La diagnosi finale rimane responsabilità del patologo con correlazione clinico-patologica completa.

**Nota sulla validazione:** Questo tool è basato su revisione sistematica della letteratura e best practices pubblicate. Non è stato validato prospetticamente su casistica locale. I cutoff e le raccomandazioni derivano da studi validati (Fassan 2014, Köbel 2019, Osakabe 2024, WHO 2022).

---

## 🔄 Changelog

### v2.1 (November 2025)
- **NUOVO:** Integrazione Ki67 per disambiguare zona grigia p53
- Ki67 cutoff organo-specifici (Fassan 2014, WHO 2022)
- Pattern concordanti/discordanti p53+Ki67
- Sezione discordanza immuno/molecolare aggiornata
- Disclaimer validazione esplicito
- Link a "p53 for dummies" (Bianchi 2025)

### v2.0 (November 2025)
- Tool completamente rifatto
- Focus su "quando richiedere p53" (decision tree)
- Interpretazione con cutoff organo-specifici validati
- Rimosso: vecchio tool grading displasia/carcinomi (inutilizzato)

### v1.0 (November 2025)
- Tool displasia + carcinomi
- Guida visuale pattern p53

---

**Versione:** 2.1  
**Autore:** Filippo Bianchi (SC Anatomia Patologica, ASST Fatebenefratelli-Sacco, Milano)  
**License:** MIT  
**Ultimo aggiornamento:** November 2025
