# p53 IHC Helper Pro - Changelog v2.0 Fixed

## 🔴 CRITICAL FIXES

### Ovaio (HGSOC) Threshold Correction
- **Old:** strong: 70% (incorrectly low)
- **New:** strong: 80% (Köbel 2016 standard)
- **Impact:** Eliminates false positive OE diagnoses
- **Source:** Köbel M, et al. J Pathol 2016;240:360-371

### "Any Intensity" Threshold Removed
- **Old:** any: 85-88% (inappropriate, includes weak 1+ staining)
- **New:** Removed (not supported by Köbel/Singh literature)
- **Impact:** Prevents over-sensitivity

### H-Score Display Cleaned Up
- **Old:** Display as "1.70" (normalized, confusing)
- **New:** Display as "170" (raw H-score, 0-300 range, clear)
- **Impact:** Cosmetic but eliminates confusion

---

## 🟠 ENHANCEMENTS

### Cytoplasmic Pattern Logic Refined
- **Old:** "Cytoplasmic aberrant if >30% any nuclei positive"
- **New:** "Pure cytoplasmic only if ≤20% nuclei positive (nuclei-negative/weak)" 
- **Impact:** Correctly distinguishes pure cyto (aberrant) from mixed (nuclei-predominant)
- **Source:** Köbel 2019 pattern-based interpretation

### POLE-Mutated Context Flag Added
- **New:** Alert if POLE-mutated AND p53-OE (rare ~5% coexistence)
- **Message:** "⚠️ CONFLITTO MOLECOLARE: POLE-mut + p53-OE raro. Verificare NGS."
- **Impact:** Flags clinically implausible combinations for verification

---

## 📋 MINOR IMPROVEMENTS

- Ovaio option label now specifies "(HG sieroso)" for clarity
- Cytoplasmic localization hint clarified
- Report footer updated with v2.0 changelog tracking
- Bibliography section updated with Köbel 2016 ovaio validation

---

## 📚 BIBLIOGRAPHY UPDATES

**Added:**
- Köbel M, et al. Optimized p53 immunohistochemistry is an accurate predictor of TP53 mutation in ovarian carcinoma. J Pathol 2016;240:360-371 ⭐ (ovaio HGSC threshold standard)
- BAGP/UKNEQAS p53 Interpretation Guidance 2016 (>80% strong pattern validation)

**Validated:**
- Singh N, et al. J Pathol 2020: Endometrio threshold ≥75% ✓ (unchanged, correct)

---

## ✅ BACKWARD COMPATIBILITY

- No breaking changes
- Existing histories/presets work unchanged
- All form fields preserved
- localStorage intact

---

## 🎯 TESTING PERFORMED

- [x] Ovaio 80% threshold triggers OE correctly
- [x] Endometrio 75% unchanged
- [x] POLE-mut + OE produces warning
- [x] Cyto pure (≤20%) triggers aberrant
- [x] Cyto mixed (>20% nuclei) → nucleare-predominant
- [x] H-score displays as integer
- [x] All presets functional
- [x] Mobile responsive
- [x] Report generation updated

---

**Version:** 2.0 Fixed  
**Date:** November 2025  
**Status:** Production Ready  
**Clinical Validation:** Singh 2020 (Endometrio), Köbel 2016/2019 (Ovaio/General)
