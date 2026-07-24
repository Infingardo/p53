# p53 IHC Helper - Quando richiederla e come interpretarla v2.4.3

**Tool diagnostico per supporto decisionale in displasia epiteliale — interpretazione pattern-based**

🔗 **[Apri il tool](https://infingardo.github.io/calcolatore-p53/)**

📖 **[Scarica "p53 for dummies" (PDF)](https://github.com/Infingardo/p53/blob/main/p53%20for%20dummies.pdf)** — Manuale pratico per patologi (Bianchi F, 2025)

---

## 🎯 Scopo

Supporto al patologo per due domande pratiche:

1. **"Devo fare la p53 IHC?"** → Decision helper con calcolo orientativo di utilità diagnostica
2. **"Come interpreto il risultato?"** → Cutoff operativi organo-specifici + pattern recognition

**⚠️ Scope:** DISPLASIE epiteliali (stomaco, colon, vescica, esofago, laringe). Per carcinomi sierosi e gliomi IDH-wt, p53 è obbligatoria ma con logica/cutoff diversi (vedi bibliografia).

---

## 🔬 Organi supportati

- Stomaco (displasia gastrica)
- Colon (displasia colonica + IBD-associated)
- Vescica (displasia uroteliale)
- Esofago (Barrett's)
- Laringe (displasia laringea)

---

## 📊 Features principali

### 🤔 Tab 1: "Devo fare la p53?"

**Input:** organo, dubbio diagnostico, citologia nucleare, contesto clinico (infiammazione, H. pylori, IBD, post-terapia)

**Output:**
- Raccomandazione: 🟢 SÌ / 🟡 OPZIONALE / 🔴 NO
- Orientatività (3 livelli euristici, non probabilità statistica)
- Ragionamento trasparente per scenario
- Guida interpretativa anticipata
- Alternativa consigliata (eradica H. pylori, tratta IBD, ripeti biopsia)

**Esempi:**
- *Vescica, reattivo vs LGD, nuclei borderline, no infiammazione* → 🟢 **RACCOMANDATO**
- *Colon IBD attiva, indefinite, nuclei borderline* → 🔴 **NON RACCOMANDATO ORA**
- *Stomaco, H. pylori+, reattivo vs LGD, nuclei borderline* → 🟡 **OPZIONALE** — eradica prima

---

### 🔬 Tab 2: "Interpreto il risultato"

**Input:** organo, % nuclei positivi, intensità, distribuzione, controllo interno, pattern speciale, Ki67 (opzionale), morfologia EE

**Output:**
- Pattern grading: Wild-type / Accumulo lieve / Over-expression / Null / Citoplasmatico
- Visualizzazione grafica cutoff **organo-specifica** (dinamica via JS)
- Testo referto copiabile con formulazione pattern-based
- Integrazione Ki67 (zona grigia)
- Nota morfologia EE (gold standard dichiarato)
- Note organo-specifiche (pannello vescica, caveat Barrett, IBD attiva)

**Cutoff operativi organo-specifici:**

| Organo | Wild-type | Zona grigia | Over-expression | Note |
|--------|-----------|-------------|-----------------|------|
| Stomaco | <10% | 10-60% | >60% diffuso | Fassan 2014, WHO 2022 |
| Colon | <20% | 20-60% | >60% diffuso | IBD: 20-50% può essere stress |
| Vescica | <10% | 10-50% | >50% diffuso | Pannello p53+CK20+CD44 |
| Esofago | <10% | 10-60% | >60% diffuso | Criteri Barrett non uniformati |
| Laringe | <10% | 10-50% | >50% full-thickness | |

**⚠️ Nota metodologica cutoff:** Il grado di validazione varia per organo. Stomaco e colon-retto hanno la base di evidenza più robusta (Fassan 2014, Osakabe 2025). Barrett/esofago e laringe hanno cutoff operativi pragmatici, non ancora standardizzati a livello internazionale. Osakabe 2025 riporta 91.3% concordanza IHC/NGS nei carcinomi colorettali con cutoff missense OE a >80% — i cutoff di questo tool per le displasie restano conservativi e orientativi.

---

### 📚 Tab 3: "Reference rapido"

- Tabelle cutoff tutti gli organi con note metodologiche
- Decision matrix (quando fare p53)
- Pattern recognition rapido (WT / OE / null / citoplasmatico / rim-like)
- Nota pannello vescica con AMACR (meta-analisi 2023)
- Ki67 integrazione organo-specifica
- Le 7 trappole della p53
- Discordanza immuno/molecolare
- AI e p53 (stato 2025)
- Bibliografia essenziale

---

## 🚀 Uso

1. Apri il tool
2. **Tab 1** → Decidi se fare p53
3. **Tab 2** → Interpreta il risultato
4. **Tab 3** → Reference al bisogno

Tool **standalone**, nessuna dipendenza esterna, funziona **offline**.

---

## 💡 Use case tipici

### Caso 1: Vescica — iperplasia vs LGD
1. **Tab 1:** vescica + reattivo vs LGD + nuclei borderline → 🟢 RACCOMANDATO
2. p53: 55% diffuso 2+/3+
3. **Tab 2:** Over-expression (>50% cutoff vescica) → pattern aberrante, interpreto nel pannello p53+CK20+CD44
4. Copia referto

### Caso 2: Colon IBD — indefinite
1. **Tab 1:** colon-IBD + indefinite + IBD attiva → 🔴 NON RACCOMANDATO ORA
2. Tratto IBD → remissione → biopsia → se atipia persiste → Tab 2

### Caso 3: Stomaco zona grigia + Ki67
1. **Tab 2:** p53 35% focale + Ki67 >30% esteso → accumulo lieve MA Ki67 concordante → LGD probabile, follow-up stretto

---

## 📚 Bibliografia essenziale

- **Bianchi F.** p53 for dummies. Manuale pratico per patologi. 2025 [[PDF](https://github.com/Infingardo/p53/blob/main/p53%20for%20dummies.pdf)]
- **Fassan M, et al.** p53 and Ki67 expression profiles identify clinically relevant gastric dysplasia. *Mod Pathol* 2014;27:1409-1417
- **Köbel M, et al.** Interpretation of P53 Immunohistochemistry in Endometrial Carcinomas: Toward Increased Reproducibility. *Int J Gynecol Pathol* 2019;38:S123-S131
- **Vermij L, et al.** p53 immunohistochemistry in endometrial cancer: clinical and molecular correlates in the PORTEC-3 trial. *Mod Pathol* 2022;35:1475-1483
- **Osakabe M, et al.** The pattern-based interpretation of p53 IHC as a surrogate marker for TP53 mutations in colorectal cancer. *Virchows Arch* 2025;486:333-341 [concordanza 91.3%, cutoff missense OE >80% in CRC]
- **WHO Classification of Tumours.** Digestive System Tumours. 5th ed. IARC, 2019/2022
- **WHO Classification of Tumours.** Central Nervous System Tumours. 5th ed. IARC, 2021
- **Rugge M, et al.** MAPS II. *Gut* 2019;68:1743-1752
- **de Haan LM, et al.** Real-world TP53 mutational analysis in B-cell lymphomas. *Virchows Arch* 2024;485:643-654
- **Ma Y, et al.** Artificial intelligence in diagnostic pathology. *Diagn Pathol* 2023;18:109
- **Kobayashi S, et al.** AI Program to Predict p53 Mutations in UC-Associated Cancer or Dysplasia. *Am J Pathol* 2022;192:1121-1129

---

## ⚠️ Disclaimer

Tool per supporto decisionale. La diagnosi finale rimane responsabilità del patologo con correlazione clinico-patologica completa.

Non validato prospetticamente su casistica locale. Cutoff operativi derivati da revisione sistematica della letteratura (Fassan 2014, Köbel 2019, Osakabe 2025, WHO 2022).

---

## 🔄 Changelog

### v2.4.2 (2025)
- **FIX:** `resetDecision()` ora opera solo sui checkbox del Tab 1 — non azzera più `int-ibd-active` nel Tab 2
- **FIX:** `posttreat` (post-terapia/radioterapia) ora attivo nella logica decisionale: abbassa utility in `reactive-vs-lgd` e compare nel reasoning
- **FIX:** Etichetta dropdown "citoplasmatico" uniformata alla reference: "positività citoplasmatica prevalente ± nuclei variabili"

### v2.4.1 (2025)
- **FIX:** "cutoff organo-specifici validati" → "cutoff operativi organo-specifici" (header e disclaimer)
- **FIX:** Etichetta `ctx-ibd` corretta: "Storia/contesto di IBD attiva"
- **FIX:** `toggleIbdActive()` non resetta più il giudizio morfologico EE al cambio organo
- **FIX:** Ramo cytoplasmic >20%: rimossa deduzione di intensità relativa non raccolta dall'input
- **ADD:** Nota AMACR nella sezione pannello vescica (meta-analisi 2023)

### v2.4.0 (2025)
- **FIX:** Barra cutoff organo-specifica (gradient dinamico via JS — non più statico al 65% per tutti)
- **FIX:** `goToInterpret()` chiama `toggleIbdActive()` — IBD group visibile arrivando da Tab 1
- **FIX:** `generateAlternatives()` non restituisce più box giallo vuoto
- **FIX:** IBD implicita per `colon-ibd` — comportamento coerente indipendentemente dal checkbox
- **FIX:** Pattern citoplasmatico: soglia alzata a 20%, ammesso staining nucleare variabile
- **FIX:** Output referto: "Displasia confermata" → formulazione pattern-based in tutti i rami aberranti
- **ADD:** Disclamer cutoff pragmatici in header e reference
- **ADD:** Pannello vescica p53+CK20+CD44 con nota su Ki67 defilato
- **ADD:** Caveat Barrett (criteri non uniformati) nella nota organo
- **ADD:** Nota Osakabe concordanza e cutoff missense >80% nella tabella reference

### v2.3.2 e precedenti
→ Vedi archivio repository

---

**Versione:** 2.4.3 "p53 for dummies edition" (con Ki67)
**Autore:** Filippo Bianchi (SC Anatomia Patologica, ASST Fatebenefratelli-Sacco, Milano)
**License:** MIT
