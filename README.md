# Calcolatore p53 v1.0

**Tool diagnostico unificato per p53 IHC pattern-based interpretation + displasia gastrica e colonica**

---

## 📋 Indice

1. [Cos'è](#cosè)
2. [Modalità](#modalità)
3. [Guida rapida](#guida-rapida)
4. [p53 IHC - Criteri e interpretazione](#p53-ihc---criteri-e-interpretazione)
5. [Displasia Gastrica - Criteri WHO 2022](#displasia-gastrica---criteri-who-2022)
6. [Displasia Colonica - Criteri WHO/SCENIC 2019](#displasia-colonica---criteri-whoscenic-2019)
7. [Disclaimer e limitazioni](#disclaimer-e-limitazioni)
8. [Bibliografia essenziale](#bibliografia-essenziale)

---

## Cos'è

**Calcolatore p53** è un tool interattivo per l'interpretazione diagnostica di:

- **p53 IHC** (Immunoistochimica) in carcinomi (modalità neoplastica)
- **Displasia gastrica** (preneoplastico) secondo WHO 2022
- **Displasia colonica** (preneoplastico) secondo WHO/SCENIC 2019

Il tool implementa **pattern-based interpretation** con:
- Input strutturato (morfologia, architettura, immunofenotipo, contesto clinico)
- Grading automatico secondo standard internazionali
- Risk stratification e raccomandazioni di management
- Generazione di testo referto copiabile

**Uso dichiarato:** supporto diagnostico e didattico. **Non sostituisce la valutazione clinico-patologica completa.**

---

## Modalità

### 🧬 p53 IHC (Neoplastico)

**Quando usare:**
- Carcinomi con diagnosi istologica già confermata
- Valutazione dello stato mutazionale TP53 tramite pattern immunoistochimico
- Endometrio, ovaio (HGSC), colon, mammella, polmone, stomaco, pancreas, sarcomi

**Parametri:**
- Quantificazione nucleare (% a 4 livelli di intensità: 0, 1+, 2+, 3+)
- H-score calcolato automaticamente
- Pattern di distribuzione (mosaico, diffuso, focale, zonale)
- Localizzazione subcellulare (nucleare, citoplasmatica, mista)
- Pattern aberranti specifici (rim-like, speckled, esclusione nucleare)
- Contesto molecolare (MMR, POLE, grado)
- Controlli tecnici (interno, qualità)

**Output:**
- **Grading:** Wild-type / Over-expression / Null / Citoplasmatico aberrante / Non interpretabile
- **Confidence:** Alta / Moderata / Bassa
- **Azione:** Pattern di riferimento (criteri confermati)
- **Testo referto:** copiabile negli appunti

---

### 🔬 Displasia Gastrica (Preneoplastico - WHO 2022)

**Quando usare:**
- Biopsie gastriche da endoscopia (routine screening o follow-up)
- Valutazione del rischio neoplastico
- Pazienti con gastrite cronica, metaplasia intestinale, atrofia

**Parametri:**
- Contesto H. pylori, metaplasia intestinale, atrofia
- Morfologia nucleare (6 criteri: pleomorfismo, crowding, ipercromatismo, contorni, nucleoli, mitosi)
- Architettura ghiandolare (integra / disrupzione basale / cribriformo / infiltrante)
- Stratificazione citoplasmatica
- Immunofenotipo (p53, Ki67) se disponibile
- Estensione e profondità della lesione

**Output:**
- **Grading WHO 2022:** Non displasia / LGD / HGD / Carcinoma / Non interpretabile
- **Risk stratification:** Basso / Intermedio / Alto / Molto alto
- **Management specifico:**
  - LGD: ripetere biopsia in 2-3 mesi, surveillance
  - HGD: ESD (endoscopic submucosal dissection) o chirurgia
  - Carcinoma: urgente staging e oncologia
- **Testo referto:** WHO 2022 validated

---

### 🔍 Displasia Colonica (Preneoplastico - WHO/SCENIC 2019)

**Quando usare:**
- Biopsie coloniche (polipectomia, screening, IBD surveillance)
- Pazienti con e senza IBD (Crohn, rettocolite ulcerosa)
- Risk stratification per progressione a carcinoma

**Parametri:**
- IBD status, durata e attività infiammatoria
- Morfologia nucleare (6 criteri)
- Architettura ghiandolare (normale / distorta / disrupzione basale / cribriformo / infiltrante)
- Stratificazione citoplasmatica
- Infiammazione associata e polipoid growth (endoscopico)
- p53 e Ki67 se disponibili
- Margini di polipectomia (negativo / compromesso / positivo)
- Profondità e desmoplasia

**Output:**
- **Grading WHO/SCENIC 2019:** Negativo / LGD / Indefinite / HGD / Carcinoma / Non interpretabile
- **Risk stratification IBD-specific:**
  - Negativo: surveillance ogni 1-3 anni (dipende durata IBD)
  - LGD/Indefinite: ripetere biopsia + surveillance ravvicinata
  - HGD: polipectomia/ESD se possibile; colectomia se multicentrica
- **Management diferenziato:** IBD-associated vs sporadic
- **Testo referto:** WHO/SCENIC 2019 compliant

---

## Guida rapida

### 1. Seleziona modalità
Clicca uno dei tre pulsanti: **p53 IHC** / **Displasia Gastrica** / **Displasia Colonica**

### 2. Quick entry (opzionale)
- Se conosci il pattern grossolano, usa i **preset button** (es. "Classic OE" per p53)
- Il form si popola automaticamente con valori tipici
- Personalizza i campi che ti servono

### 3. Compila il form
- **Sezione dati:** ID caso, campione, localizzazione
- **Contesto:** H. pylori, MMR/POLE, IBD status, ecc.
- **Morfologia:** checkbox per criteri istologici
- **Immunofenotipo:** se disponibile (p53, Ki67)
- **Note libere:** osservazioni cliniche/endoscopiche

### 4. Analizza
Clicca **"🔬 Analizza"** oppure **Ctrl+Enter**

### 5. Leggi il risultato
- **Badge colore:** tipo di risposta (verde=wild-type, giallo=HGD, rosso=carcinoma)
- **Motivazione:** perché quel grading
- **Azione:** cosa fare dopo
- **Risk stratification:** probabilità progressione
- **Testo referto:** copiabile

### 6. Copia testo referto
Clicca **"📋 Copia testo"** per copiagli in clipboard

---

## p53 IHC - Criteri e interpretazione

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
- **Contesto:** POLE-mutato (eccellente prognosi) / MMR-deficient (basso rischio se p53-WT)
- **Azione:** no molecular testing necessario

#### 🟡 Over-expression (Mutazione stabilizzante)
- **Criteri soddisfatti:** ≥% soglia forte O H-score ≥soglia
- **Distribuzione:** diffusa/uniforme (contrasto con WT)
- **Localizzazione:** nucleare prevalente
- **p53 molecolare:** tipicamente missense hotspots (R175, R248, R273)
- **Azione:** pattern aberrante confermato, prognosi aggressiva

#### 🔴 Null (Perdita completa)
- **Criteri:** 0% nuclei positivi + controllo interno FORTE
- **Molecolare:** mutazioni inattivanti (nonsense, frameshift, delezioni)
- **Azione:** pattern aberrante definitivo
- **⚠️ Attenzione:** se controllo interno weak → RIPETERE (possibile falso negativo tecnico)

#### 🟣 Citoplasmatico aberrante (Sequestro nucleare)
- **Criteri:** sequestro citoplasmatico con nuclei negativi/deboli (<20%)
- **Specifico:** pattern rim-like, speckled, esclusione nucleare
- **Molecolare:** mutazioni NLS (Nuclear Localization Signal)
- **Azione:** pattern aberrante definitivo

#### ⚪ Non interpretabile
- **Cause:** qualità tecnica scarsa, controllo interno assente, artefatti gravi
- **Azione:** RIPETERE con controlli appropriati

### Contesto molecolare (ProMisE classification)

| Stato | p53 pattern | MMR/POLE | Prognosi | Note |
|-------|------------|----------|----------|------|
| POLE-mutated | Wild-type | WT | Eccellente | ⚠️ Se p53-OE raro (~5%) |
| MMR-deficient | Wild-type | Deficient | Buona (se p53-WT) | Cattiva se p53-abn |
| p53-abnormal | OE/Null/Cyto | Any | Cattiva | Chemiosensibile platino |
| NSMP | Wild-type | Proficient | Intermedia | No specifiche alterazioni |

---

## Displasia Gastrica - Criteri WHO 2022

### 🟢 Non displasia
- Nuclei piccoli, basali, basso N/C ratio
- Architettura integra
- Polarità nucleare preservata
- Ki67 basale (<10%)
- p53 wild-type

### 🔵 LGD (Low-Grade Dysplasia)
**Almeno 1 criterio:**
- Nuclei moderatamente aumentati (N/C 1:1-2:1) con crowding focale
- Ipercromatismo lieve (non marcato)
- **Architettura INTEGRA** (NO disrupzione basale)
- Mitosi <5/10HPF
- p53 wild-type o lieve accumulo
- Ki67 10-30%, esteso nella base ma NON oltre 1/3

**Azione:** ripetere biopsia in 2-3 mesi (confermamento). Se confermato: surveillance endoscopica ogni 6-12 mesi.

### 🟡 HGD (High-Grade Dysplasia)
**Almeno 2 criteri + DISRUPZIONE BASALE:**
- Nuclei marcatamente aumentati (N/C >2:1), pleomorfi
- Ipercromatismo marcato, contorni irregolari
- **⚠️ DISRUPZIONE LAMININA BASALE** (criterio chiave WHO 2022):
  - Pattern cribriformo
  - Micropapille fuse
  - Fusione ghiandolare focale
  - Foci infiltranti SENZA invasione profonda
- Mitosi >5/10HPF incluse figure atipiche
- p53 over-expression (>30%) o null
- Ki67 >30% o esteso oltre 1/3 basilare
- Perdita totale polarità

**Azione:** **URGENTE**
- ESD (Endoscopic Submucosal Dissection) se no invasione sottomucosa
- Altrimenti gastrectomia parziale
- Follow-up endoscopico 6-12 mesi post-intervento
- Oncologia se carcinoma invasivo

### 🔴 Carcinoma
- HGD + invasione confermata (lamina propria profonda, sottomucosa, oltre)
- Reazione desmoplastica marcata
- Necrosi tumorale focale

**Azione:** **URGENTE - STAGING - CHIRURGIA - ONCOLOGIA**

---

## Displasia Colonica - Criteri WHO/SCENIC 2019

### 🟢 Negativo per displasia
- Architettura normale (cripte ordinate)
- Citologia benigna
- Polarità preservata

**Surveillance:**
- **IBD:** endoscopia ogni 1-2 anni (dipende durata, attività infiammatoria)
- **Sporadic:** colonscopia standard (10 anni se polipo <10mm, 3-5 anni se precedente)

### 🔵 LGD (Low-Grade Dysplasia)
- Nuclei moderatamente aumentati, crowding focale
- Architettura distorta ma NO disrupzione basale
- Stratificazione parziale
- Mitosi regolarmente situate
- Ki67 esteso nei 2/3 inferiori
- p53 wild-type

**Azione:**
- **IBD:** ripetere biopsia in 2-3 mesi, surveillance ogni 6-12 mesi, considerare p53
- **Sporadic in polipo:** polipectomia completa + margini, altrimenti surveillance

### 🟠 INDEFINITE per dysplasia
**Categoria intermedia importante in IBD:**
- Atipia borderline (2+ criteri morfologici)
- Architettura distorta senza disrupzione basale chiara
- Infiammazione attiva moderata-marcata (IBD)

**Azione:**
- **IBD:** ripetere biopsia in 2-3 mesi, correlazione endoscopica, p53/Ki67 se dubbio persiste
- **Non-IBD:** ripetere biopsia, se confermato → resezione, follow-up

### 🟡 HGD (High-Grade Dysplasia)
**Almeno 2 criteri + DISRUPZIONE BASALE:**
- Nuclei marcatamente aumentati, pleomorfi, ipercromatici
- Contorni irregolari, nucleoli prominenti
- **Disrupzione laminina basale:**
  - Cribriformo/micropapille
  - Pattern infiltrante (senza invasione mucosa profonda)
- Mitosi atipiche >5/10HPF
- Stratificazione completa (perdita polarità)
- p53 over-expression o null
- Ki67 >30% diffuso
- Desmoplasia moderata

**Azione:**
- **IBD-HGD:** polipectomia/ESD se localizzato e resecabile; **COLECTOMIA se multicentrica**
- **Sporadic-HGD:** polipectomia completa + margini negativi
- Resezione se margini positivi
- Surveillance post-intervento endoscopica 6-12 mesi
- Oncologia se invasione confermata

### 🔴 Carcinoma
- HGD + invasione sottomucosa o muscolaris mucosae
- Desmoplasia marcata
- Reazione stromale definitiva

**Azione:** **URGENTE - STAGING TNM - CHIRURGIA - ONCOLOGIA**

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

3. **p53 IHC è pattern-based, non molecolare**
   - La positività/negatività IHC correla con mutazione TP53 ma non è diagnostica
   - NGS rimane standard per diagnosi molecolare definitiva
   - Eccezioni: null pattern + controllo forte = alta specificità

4. **Displasia è soggettiva**
   - Reproducibilità per HGD ~76-85%
   - Reproducibilità per LGD ~50-60% (confine difficile)
   - Ripetere biopsia in caso di dubbio clinico

5. **IBD-associated dysplasia è ambigua**
   - Infiammazione attiva complica distinzione displasia/iperplasia reattiva
   - Categoria "Indefinite" esiste per questo
   - Correlazione endoscopica + biopsia ripetuta consigliata

### 📊 Parametri non inclusi

Il tool **non include:**
- MSI/dMMR testing (deferisce a MMR status input)
- BRAF, KRAS, POLE sequencing (solo contesto clinico)
- EBV in situ hybridization
- Profili genomici/transcriptomici
- Grading Fuhrman (tumori renali)
- Grade istologico con fattori di rischio compositi

Per questi parametri: **consultare linee guida specifiche e/o molecular pathologist**

---

## Bibliografia essenziale

### p53 IHC Validation
- **Singh N, et al.** p53 immunohistochemistry is an accurate surrogate for TP53 mutational analysis in endometrial carcinoma. *J Pathol* 2020;250:336-345 [⭐ 207 cases, 90.7% accuracy]
- **Köbel M, et al.** Optimized p53 immunohistochemistry is an accurate predictor of TP53 mutation in ovarian carcinoma. *J Pathol* 2016;240:360-371 [⭐ HGSC standard, >80% strong]
- **Köbel M, Ronnett BM, Singh N, et al.** Interpretation of P53 Immunohistochemistry in Endometrial Carcinomas. *Int J Gynecol Pathol* 2019;38:S123-S131
- **van den Heerik ASVM, et al.** PORTEC-3 molecular validation. *Mod Pathol* 2022;35:1475-1483

### Gastric Dysplasia - WHO 2022
- **Nagtegaal ID, Odze RD, Klimstra D, et al.** WHO Classification of Tumours of the Digestive System. 5th ed. 2019/2022
- **Rugge M, et al.** MAPS Consensus on Early Gastric Neoplasia. *Gut* 2016;65:1133-1143
- **Schlemper RJ, et al.** Consensus on the histopathology of gastric intestinal metaplasia-dysplasia continuum. *Gut* 2000;47:S1-S24
- **Fassan M, et al.** Gastric dysplasia: Transition to carcinoma. *Dig Dis* 2016;34:306-312

### Colonic Dysplasia - WHO/SCENIC 2019
- **Nagtegaal ID, et al.** WHO Classification of Tumours of the Digestive System. 5th ed. 2019/2022
- **Loughrey MB, et al.** SCENIC International Consensus Classification of Gastrointestinal Neuroendocrine Neoplasms. *Histopathology* 2020;77:335-346
- **ASGE Standards of Practice Committee.** Screening and surveillance of premalignant conditions of the colon. *Gastrointest Endosc* 2006
- **Eaden JA, et al.** Cancer risk in inflammatory bowel disease: estimation and limitations of current evidence. *Gut* 2002;50:85-86

### ProMisE Endometrial Classification
- **Kommoss S, et al.** Final validation of the ProMisE molecular classifier. *Ann Oncol* 2018;29:1180-1188
- **ESGO/ESTRO/ESP Endometrial Carcinoma Guidelines 2021**
- **CAP Cancer Protocols 2024**

---

## Versione e changelog

**v1.0** (November 2025)
- ✅ p53 IHC pattern-based interpretation (Singh 2020, Köbel 2016/2019)
  - Organ-specific thresholds (endometrio 75%, ovaio 80%, colon/mammella/polmone/stomaco 80%, pancreas/sarcoma 85%)
  - Pattern wild-type, over-expression, null, cytoplasmic aberrant
  - POLE/MMR context flags
  - H-score display corrected (integer 0-300)
- ✅ Gastric dysplasia (WHO 2022, Rugge MAPS 2016)
  - Grading: negative/LGD/HGD/carcinoma
  - Disrupzione basale criterio HGD chiave
  - Risk stratification MAPS
  - Management specifico
- ✅ Colonic dysplasia (WHO/SCENIC 2019)
  - Grading: negative/LGD/indefinite/HGD/carcinoma
  - IBD-associated vs sporadic management
  - Margini polipectomia
  - Risk stratification IBD-specific
- ✅ Unified codebase: 3 modalità, shared infrastructure
- ✅ Quick presets per pattern comuni
- ✅ Report generation copiabile

---

## Contatti e feedback

Tool sviluppato come supporto diagnostico per anatomia patologica.

**Limitazioni note e feedback:** contattare autore tramite GitHub repository.

**Ultimo aggiornamento:** November 2025

---

**Disclaimer finale:** *This tool is provided for educational and diagnostic support purposes only. Clinical diagnostic decisions must always be based on complete clinicopathologic correlation and expert review. The authors assume no liability for clinical decisions made based on tool output.*
