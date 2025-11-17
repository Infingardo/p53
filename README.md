# Calcolatore p53 v1.0

**Tool diagnostico unificato per p53 pattern-based interpretation in carcinomi e displasie epiteliali**

---

## 📋 Indice

1. [Cos'è](#cosè)
2. [Struttura e navigazione](#struttura-e-navigazione)
3. [Modalità](#modalità)
4. [Guida rapida](#guida-rapida)
5. [p53 nei Carcinomi - Criteri e interpretazione](#p53-nei-carcinomi---criteri-e-interpretazione)
6. [p53 nella Displasia - Criteri WHO](#p53-nella-displasia---criteri-who)
7. [Disclaimer e limitazioni](#disclaimer-e-limitazioni)
8. [Bibliografia essenziale](#bibliografia-essenziale)

---

## Cos'è

**Calcolatore p53** è un tool interattivo per l'interpretazione diagnostica di:

### 🧬 **p53 nei Carcinomi** (Neoplastico)
- Carcinomi già diagnosticati (endometrio, ovaio, colon, mammella, polmone, stomaco, pancreas, sarcomi)
- Pattern-based interpretation (wild-type, over-expression, null, aberranti)
- Soglie organo-specifiche secondo Singh 2020, Köbel 2016/2019
- Risk stratification molecolare (POLE, MMR, ProMisE classification)

### 🔬 **p53 nella Displasia** (Preneoplastico)
- **Displasia Gastrica** (WHO 2022) - normal/LGD/HGD/carcinoma
- **Displasia Colonica** (WHO/SCENIC 2019) - negative/LGD/indefinite/HGD/carcinoma (IBD-specific)
- **Displasia Esofagea** (Barrett's) - negative/indefinite/LGD/HGD/carcinoma
- **Displasia Vescicale** (Uroteliale) - normal/LGD/HGD/carcinoma invasivo
- **Displasia Laringea** - normal/LGD/HGD/carcinoma

### 📚 **Guida Visuale p53** (Didattica)
- Pattern-based education: come riconoscere wild-type vs over-expression vs null
- Continuum istologico: da mucosa normale → metaplasia → displasia bassa → displasia alta → carcinoma
- Errori comuni e workflow pratico al microscopio
- Organ-specific considerations (gastrica vs colonica)

**Uso dichiarato:** supporto diagnostico, didattica, research. **Non sostituisce la valutazione clinico-patologica completa.**

---

## Struttura e navigazione

### Entry point: 📚 **Guida Visuale p53** (default)
Consigliato per **chi usa il tool la prima volta** o **vuole imparare i pattern p53**

### Poi scelta tra 2 branche:

#### 🧬 **p53 nei Carcinomi**
Form unico per valutare p53 in carcinomi già diagnosticati
- Input: quantificazione nucleare (% per intensità), H-score, pattern, contesto molecolare (MMR/POLE)
- Output: grading (WT/OE/null/cyto/NI), confidence, significato clinico
- Parametri organ-specific (endometrio, ovaio, colon, mammella, etc.)

#### 🔬 **p53 nella Displasia** → Menu organi:
- **🔴 Displasia Gastrica** (WHO 2022)
- **🟠 Displasia Colonica** (WHO/SCENIC 2019, IBD-aware)
- **🟡 Displasia Esofagea** (Barrett's)
- **🟢 Displasia Vescicale** (Uroteliale)
- **🔵 Displasia Laringea**

Ogni organo ha:
- Quick presets (normal/LGD/HGD/carcinoma)
- Form specifico (morfologia, architettura, immunofenotipo, contesto)
- Grading automatico secondo standard internazionali
- Management recommendations organ-specific
- Testo referto copiabile

---

## Modalità

### 📚 **Guida Visuale p53** (Didattica)

**Quando usare:**
- Primo approccio a p53 pattern-based interpretation
- Imparare la differenza tra wild-type (mosaico) vs over-expression (diffuso)
- Capire il continuum normale → metaplasia → displasia → carcinoma
- Evitare errori comuni

**Contenuti:**
- **Mucosa Normale:** p53 wild-type mosaico (<10%), nuclei piccoli basali
- **Metaplasia Intestinale/IM:** wild-type, pre-cancerosa ma p53 ancora normale
- **LGD (Low-Grade Dysplasia):** wild-type mosaico O lieve accumulo 30-50%, architettura integra
- **HGD (High-Grade Dysplasia):** over-expression >60-80% uniforme, architettura cribriforme/infiltrante
- **Carcinoma:** over-expression massivo >80% O null + invasione sottomucosa

**Per organo:**
- Gastrica: p53 pattern in continuum WHO 2022
- Colonica: p53 pattern + confusione IBD infiammata vs displasia (⚠️ immunofenotipo aiuta ma attenzione al contesto)

**Errori comuni:** cosa NON fare, quando ripetere, workflow pratico al microscopio

---

### 🧬 **p53 nei Carcinomi** (Neoplastico)

**Quando usare:**
- Carcinomi con diagnosi istologica già confermata
- Valutazione dello stato mutazionale TP53 tramite pattern immunoistochimico
- Endometrio, ovaio (HGSC), colon, mammella, polmone, stomaco, pancreas, sarcomi

**Parametri:**
- Quantificazione nucleare (% a 4 livelli: 0, 1+, 2+, 3+)
- H-score calcolato automaticamente
- Pattern distribuzione (mosaico, diffuso, focale, zonale)
- Localizzazione subcellulare (nucleare, citoplasmatica, mista)
- Pattern aberranti specifici (rim-like, speckled, esclusione nucleare)
- Contesto molecolare (MMR, POLE, grado)
- Controlli tecnici

**Output:**
- **Grading:** Wild-type / Over-expression / Null / Citoplasmatico aberrante / Non interpretabile
- **Confidence:** Alta / Moderata / Bassa
- **Testo referto:** copiabile negli appunti

---

### 🔬 **p53 nella Displasia - Menu Organi**

Ogni organo ha parametri specifici e standard di riferimento:

#### 🔴 **Displasia Gastrica** (WHO 2022)
- Contesto: H. pylori, metaplasia intestinale, atrofia
- Morfologia: 6 criteri (pleomorfismo, crowding, ipercromatismo, contorni, nucleoli, mitosi)
- **Architettura chiave:** integra (LGD) vs interruzione basale (HGD)
- p53 + Ki67 se disponibili
- **Grading:** Non displasia → LGD → HGD → Carcinoma
- **Management:** LGD ripeti biopsia; HGD ESD/chirurgia; Carcinoma urgente

#### 🟠 **Displasia Colonica** (WHO/SCENIC 2019)
- Contesto: IBD status, durata, attività infiammatoria
- Morfologia: 6 criteri
- Architettura: normale/distorta/cribriforme/infiltrante
- **⚠️ Confusione IBD:** infiammazione marcata può aumentare p53 per stress, NON mutazione TP53
- p53 + Ki67
- **Grading:** Negativo → LGD → Indefinite → HGD → Carcinoma
- **Management IBD-specific:** HGD localizzata ESD vs multicentrica colectomia
- **Management sporadic:** polipectomia completa + margini

#### 🟡 **Displasia Esofagea** (Barrett's)
- Contesto: tipo IM (specializzata = rischio), lunghezza segmento
- Morfologia: 6 criteri
- Architettura: cribriforme/infiltrante HGD
- p53 + Ki67
- **Grading:** Negativo → Indefinite → LGD → HGD → Carcinoma
- **Management:** EMR se HGD, surveillance se LGD

#### 🟢 **Displasia Vescicale** (Uroteliale)
- Contesto: localizzazione, carcinoma concomitante
- Morfologia: 5 criteri (nuclei)
- Architettura: spessore uroteliale (normale/inspessito/displastico)
- **⚠️ p53-OE frequente** in HGD urotelo (40-60%)
- Profondità invasione (epiteliale/lamina propria/muscolare)
- **Grading:** Normale → LGD → HGD → Carcinoma invasivo
- **Management:** cTUR-BT se HGD, surveillance ristretta

#### 🔵 **Displasia Laringea**
- Contesto: localizzazione laringe, smoking, HPV status
- Morfologia: 5 criteri
- Architettura: **maturation pattern** (criterio chiave HGD)
- p53 localizzazione (basale vs full-thickness)
- Profondità invasione
- **Grading:** Normale → LGD → HGD → Carcinoma
- **Management:** laser resection, surveillance ristretta

---

## Guida rapida

### 1. Apri il tool
Vedi **Guida Visuale p53** di default

### 2. Leggi la Guida (opzionale ma consigliato)
- Impara i pattern wild-type vs over-expression
- Scopri errori comuni
- Capisci il workflow microscopico

### 3. Scegli la branca
- **p53 nei Carcinomi** se è già carcinoma diagnosticato
- **p53 nella Displasia** se valuti displasia preneoplastica

### 4. Se Displasia → Scegli organo
Clicca il bottone dell'organo (gastrico, colnico, ecc.)

### 5. Compila il form
- Quick entry (preset) oppure manuale
- Morfologia, architettura, immunofenotipo, contesto

### 6. Analizza
Clicca **"🔬 Analizza"** oppure **Ctrl+Enter**

### 7. Leggi il risultato
- Badge colore (verde=WT, giallo=HGD, rosso=carcinoma)
- Motivazione del grading
- Management specifico per organo
- Testo referto copiabile

---

## p53 nei Carcinomi - Criteri e interpretazione

### Soglie organo-specifiche (v2.0 CORRETTE)

| Organo | % Forte (2+/3+) | H-score |
|--------|-----------------|---------|
| Endometrio | ≥75% | ≥200 |
| Ovaio (HGSC) | **≥80%** | ≥180 |
| Colon | ≥80% | ≥220 |
| Mammella | ≥80% | ≥200 |
| Polmone | ≥80% | ≥200 |
| Stomaco | ≥80% | ≥210 |
| Pancreas | ≥85% | ≥220 |
| Sarcoma | ≥85% | ≥220 |

**Nota:** v1 aveva ovaio 70% → **CORRETTO a 80%** (Köbel 2016 standard)

### Pattern principali

#### 🟢 Wild-type (Funzione normale)
- **Distribuzione:** eterogenea a mosaico (hallmark)
- **Intensità:** variabile (0%, 1+, 2+, 3+ mescolati)
- **% Forte:** <soglia organo-specifica
- **Contesto:** POLE-mutato → eccellente prognosi; MMR-deficient → basso rischio se p53-WT
- **Azione:** no molecular testing necessario

#### 🟡 Over-expression (Mutazione stabilizzante)
- **Criteri:** ≥% soglia forte O H-score ≥soglia
- **Distribuzione:** diffusa/uniforme (contrasto con WT)
- **Localizzazione:** nucleare prevalente
- **p53 molecolare:** tipicamente missense hotspots (R175, R248, R273)
- **Azione:** pattern aberrante confermato, prognosi aggressiva

#### 🔴 Null (Perdita completa)
- **Criteri:** 0% nuclei positivi + controllo interno FORTE
- **Molecolare:** mutazioni inattivanti (nonsense, frameshift, delezioni)
- **Azione:** pattern aberrante definitivo
- **⚠️ Attenzione:** se controllo interno weak → RIPETERE

#### 🟣 Citoplasmatico aberrante (Sequestro nucleare)
- **Criteri:** sequestro citoplasmatico con nuclei negativi/deboli (<20%)
- **Specifico:** pattern rim-like, speckled, esclusione nucleare
- **Molecolare:** mutazioni NLS (Nuclear Localization Signal)
- **Azione:** pattern aberrante definitivo

#### ⚪ Non interpretabile
- **Cause:** qualità tecnica scarsa, controllo interno assente, artefatti gravi
- **Azione:** RIPETERE con controlli appropriati

---

## p53 nella Displasia - Criteri WHO

### 🟢 **Negativo/Normale**
- Nuclei piccoli basali, basso N/C ratio
- Architettura integra
- p53 <10% wild-type mosaico
- Ki67 basale

### 🔵 **LGD** (Low-Grade Dysplasia)
- Nuclei moderatamente aumentati, crowding focale
- **Architettura INTEGRA** (NO interruzione basale)
- p53: wild-type mosaico O lieve accumulo 30-50% (MAI >80%)
- Mitosi <5/10HPF
- Stratificazione parziale

**Azione:** Ripetere biopsia in 2-3 mesi (confermamento). Se confermato: surveillance endoscopica.

### 🟠 **Indefinite** (Colonica - categoria intermedia)
- Atipia borderline
- Infiammazione attiva (IBD)
- Confine difficile vs LGD/iperplasia reattiva

**Azione:** Ripetere biopsia, correlazione endoscopica, p53/Ki67 se dubbio persiste.

### 🟡 **HGD** (High-Grade Dysplasia)
- Nuclei marcatamente aumentati, pleomorfi
- **INTERRUZIONE BASALE** (criterio chiave WHO):
  - Pattern cribriforme
  - Micropapille fuse
  - Foci infiltranti SENZA invasione profonda
- p53 over-expression >60-80% O pattern aberrante
- Mitosi >5/10HPF
- Perdita completa stratificazione

**Azione:** **URGENTE** - ESD, polipectomia, o chirurgia (dipende da organo e contesto). Follow-up ravvicinato.

### 🔴 **Carcinoma**
- HGD + invasione sottomucosa confermata
- Reazione desmoplastica marcata
- p53 massivamente positivo O null

**Azione:** **URGENTE - STAGING - CHIRURGIA - ONCOLOGIA**

---

## Disclaimer e limitazioni

### ⚠️ Disclaimer clinico

1. **Questo tool è per supporto diagnostico e didattico SOLO**
   - Non sostituisce la valutazione clinico-patologica completa
   - La diagnosi finale rimane responsabilità del patologo
   - Correlazione clinico-radiologica essenziale

2. **Qualità del campione è critica**
   - Orientamento pessimo, autolisi, artefatti → risultati inaffidabili
   - Controlli tecnici insufficienti → ripetere sempre
   - Il tool segnala "non interpretabile" se qualità grave

3. **p53 è pattern-based, non molecolare**
   - La positività/negatività IHC correla con mutazione TP53 ma non è diagnostica
   - NGS rimane standard per diagnosi molecolare definitiva
   - Eccezioni: null pattern + controllo forte = alta specificità

4. **Displasia è soggettiva**
   - Reproducibilità HGD ~76-85%
   - Reproducibilità LGD ~50-60% (confine difficile)
   - Ripetere biopsia in caso di dubbio clinico

5. **IBD-associated dysplasia è ambigua**
   - Infiammazione attiva complica distinzione displasia/iperplasia reattiva
   - Categoria "Indefinite" esiste per questo
   - Correlazione endoscopica + biopsia ripetuta consigliata
   - **⚠️ p53 accumulo in IBD infiammata NON significa mutazione TP53**

---

## Bibliografia essenziale

### p53 nei Carcinomi - Validation
- **Singh N, et al.** p53 immunohistochemistry is an accurate surrogate for TP53 mutational analysis in endometrial carcinoma. *J Pathol* 2020;250:336-345 [⭐ 207 cases, 90.7% accuracy]
- **Köbel M, et al.** Optimized p53 immunohistochemistry is an accurate predictor of TP53 mutation in ovarian carcinoma. *J Pathol* 2016;240:360-371 [⭐ HGSC standard, >80% strong]
- **Köbel M, Ronnett BM, Singh N, et al.** Interpretation of P53 Immunohistochemistry in Endometrial Carcinomas. *Int J Gynecol Pathol* 2019;38:S123-S131
- **van den Heerik ASVM, et al.** PORTEC-3 molecular validation. *Mod Pathol* 2022;35:1475-1483

### p53 nella Displasia - WHO 2022/2019
- **Nagtegaal ID, Odze RD, Klimstra D, et al.** WHO Classification of Tumours of the Digestive System. 5th ed. 2019/2022
- **Rugge M, et al.** MAPS Consensus on Early Gastric Neoplasia. *Gut* 2016;65:1133-1143
- **Schlemper RJ, et al.** Consensus on the histopathology of gastric intestinal metaplasia-displasia continuum. *Gut* 2000;47:S1-S24
- **Fassan M, et al.** p53 and Ki67 expression profiles identify clinically relevant gastric dysplasia. *Mod Pathol* 2014

### Colonic Dysplasia & IBD
- **ASGE Standards of Practice Committee.** Screening and surveillance of premalignant conditions of the colon. *Gastrointest Endosc* 2006
- **Eaden JA, et al.** Cancer risk in inflammatory bowel disease: estimation and limitations of current evidence. *Gut* 2002;50:85-86

### ProMisE Endometrial Classification
- **Kommoss S, et al.** Final validation of the ProMisE molecular classifier. *Ann Oncol* 2018;29:1180-1188

---

## Versione e changelog

**v1.0** (November 2025)
- ✅ **Guida Visuale p53** (didattica pattern-based, organ-specific)
- ✅ **p53 nei Carcinomi** (Singh 2020, Köbel 2016/2019)
  - Organ-specific thresholds
  - Pattern: wild-type, over-expression, null, cytoplasmic aberrant
  - POLE/MMR context flags
  - H-score corrected (integer 0-300)
- ✅ **p53 nella Displasia** (5 organi):
  - 🔴 **Gastrica** (WHO 2022) - LGD/HGD distinzione per interruzione basale
  - 🟠 **Colonica** (WHO/SCENIC 2019) - IBD management specifico, Indefinite category
  - 🟡 **Esofagea** (Barrett's) - EMR management
  - 🟢 **Vescicale** (Uroteliale) - cTUR-BT, p53-OE frequent in HGD
  - 🔵 **Laringea** - maturation pattern criterio chiave
- ✅ **Unified codebase:** 3 modalità (guida + carcinomi + displasie), quick presets
- ✅ **Report generation** copiabile per ogni organo
- ✅ **Navigazione intuitiva:** Guida → Carcinomi vs Displasia → Organi specifici

---

## Contatti e feedback

Tool sviluppato come supporto diagnostico per anatomia patologica.

**Limitazioni note e feedback:** contattare autore tramite GitHub repository.

**Ultimo aggiornamento:** November 2025

---

**Disclaimer finale:** *This tool is provided for educational and diagnostic support purposes only. Clinical diagnostic decisions must always be based on complete clinicopathologic correlation and expert review. The authors assume no liability for clinical decisions made based on tool output.*
