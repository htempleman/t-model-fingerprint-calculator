[README.md](https://github.com/user-attachments/files/29391705/README.md)
# t-model-fingerprint-calculator
Calculates number of fingerprint lookalikes for an arrangement of fingerprint ridge features in the relevant population.

T-Model v. 10.1 Fingerprint Calculator
A quantitative-qualitative framework for latent fingerprint identification 
Developed by Henry Templeman

## Overview

The T-Model Fingerprint Calculator is a standalone HTML tool that implements the T-Model v. 10.1 — a quantitative, qualitative empirically grounded framework for fingerprint identification developed by Henry Templeman. The calculator allows latent print examiners to compute the estimated number of fingerprint lookalikes in a relevant population based on the discriminating values of matching ridge features, their spatial positions, and the quality of their correspondence.

The T-Model is described in full in:

Templeman, H. — *T-Model v. 10.1: A Quantitative-Qualitative Framework for Latent Fingerprint Identification*

The T-Model A Quantitative-Qualitative Framework for Latent Fingerprint Identification, Henry Templeman, Self-published through KDP, 2026, ISBN: 9798180412881.

## What the Calculator Does

Given a set of matching ridge features assessed during latent vs exemplar fingerprint analysis and comparison, the calculator:

- Computes the T-Value — the total discriminating value of the matching arrangement
- Calculates L — the estimated number of fingerprint arrangements in the relevant population as similar to the one found in correspondence
- Returns a sufficiency verdict: Supported (L ≤ 1), Borderline (1 < L ≤ 2), or Insufficient (L > 2)
- Displays a sufficiency table showing L across a range of reference populations from 100 people to 10 billion people
- Produces a case record summary documenting every input and every computed value for inclusion in the case file

The formula used is: **L = 120 × N / (T × log₁₀T)**

where N is the number of individual fingerprints in the relevant population, T is the T-Value, and 120 is the exponent of 10^120 — the estimated discriminating value of the average complete flat fingerprint.

## How to Use

The calculator is a single self-contained HTML file. No installation, no server, no internet connection required.

1. Download `tmodel_calculator.html`
2. Open it in any modern web browser (Safari, Chrome, Firefox, Edge)
3. To add it to your iPad or iPhone home screen: open in Safari → Share → Add to Home Screen
4. To save to desktop: open in browser → File → Save As

## Input Fields

### Step 1 — Relevant Population

Enter the number of individual fingerprints in the relevant human population:

- Witness-identified suspect in a bounded location: enter the appropriate smaller population
- National default (300 million people): enter 3,000,000,000 fingerprints
- AFIS database search: enter the documented size of the database searched at the time of the search

### Step 2 — Elasticity Threshold Confirmation

Before entering features, confirm that all corresponding feature pairs have been assessed against the T-Model's elasticity thresholds:

- Linear displacement ≤ 20% (measure with millimeter ruler if needed)
- Rotational displacement ≤ 10 degrees (measure with protractor if needed)
- Features that exceed either threshold must be excluded

An expandable step-by-step measurement guide is available within the calculator.

### Step 3 — Feature Pairs

Enter one matched feature pair per row:

- Feature type (latent and exemplar independently)
- Intervening ridge count to nearest Level 2 neighbor (IR)
- Clarity/Reliability Grade (A through F)
- Quality of Agreement (Excellent, Satisfactory, or Unsatisfactory)

Features assigned Grade F or Unsatisfactory agreement are automatically excluded from the calculation.

When connectivity is ambiguous — that is, when a feature cannot be determined to be either an ending ridge or a bifurcating ridge — select the ending ridge value appropriate to the feature's pattern force context (In Funnel or Not in Funnel) and note the ambiguity in the case record.

## Feature Types and Values

| Feature Type | Shape Value | Validation Basis |
|---|---|---|
| Ending Ridge — In Funnel | 10 | Experimental ✓ |
| Ending Ridge — Not in Funnel | 14.25 | Experimental ✓ |
| Bifurcating Ridge — In Funnel | 18.75 | Experimental ✓ |
| Bifurcating Ridge — Not in Funnel | 26.75 | Experimental ✓ |
| Single Dot | 40 | Experimental ✓ |
| 2 Cluster Dots (<1mm, same furrow) | 100 | Experimental ✓ |
| 3 Cluster Dots (<1mm, same furrow) | 216 | Experimental ✓ |
| 4 Cluster Dots (<1mm, same furrow) | 410 | Experimental ✓ |
| 5 Cluster Dots (<1mm, same furrow) | 1,024 | Experimental ✓ |
| 6 Cluster Dots (<1mm, same furrow) | 2,780 | Experimental ✓ |
| Delta — Y-shaped | 190 | Experimental ✓ |
| Delta — Non-Y-shaped | 570 | Experimental ✓ |
| Core | 209 | Experimental ✓ |
| Continuous Ridge Unit | 1.15 | Frequency only ‡ |
| Pore | 5 | Frequency only ‡ |

‡ Value based on frequency of occurrence study only; not validated through close match experiments. Use with appropriate caution and flag in case record.

## Position Values (IR)

| Intervening Ridge Count | Position Value |
|---|---|
| 0–2 IR | 1 |
| 3 IR | 4 |
| 4 IR | 10 |
| 5 IR | 62 |
| 6 IR | 968 * |
| 7 IR | 37,812 * |
| 8+ IR | 968,000 * |

\* Values at 6–8 IR are mathematical extrapolations of the confirmed 3–5 IR pattern and have not been independently validated through close match experiments. Flag in case record when used.

## Clarity/Reliability Grade Scale

| Grade | Description | Reduction Factor |
|---|---|---|
| A | No distortion — crystal clear, highly reliable | 1.00 |
| B | Low distortion — clear, reliable | 0.75 |
| C | Moderate distortion — somewhat clear, less reliable | 0.50 |
| D | High distortion — mostly obscured, position inferred | 0.25 |
| F | Very high distortion — excluded entirely | 0 |

## Quality of Agreement

| Level | Description | Reduction Factor |
|---|---|---|
| Excellent | Full correspondence, no reservations | 1.00 |
| Satisfactory | Correspondence with minor reservations | 0.50 |
| Unsatisfactory | Correspondence cannot be reliably established — excluded | 0 |

Connectivity disagreements (one impression shows an ending ridge, the other a bifurcation, at the same spatial location) that are within spatial tolerance should be rated Satisfactory.

## Sufficiency Verdicts

| L Value | Verdict |
|---|---|
| L < 1 | Supported — arrangement is sufficient for identification against the stated population |
| 0.5 ≤ L ≤ 2 | Borderline — review all inputs carefully before reporting |
| L > 2 | Insufficient — arrangement does not support identification against the stated population |

## Output

After pressing Calculate, the calculator produces:

- T-Value (combined conservative)
- L value: estimated lookalike count against the stated population
- Formula: L = 120 × N / (T × log₁₀T)
- Sufficiency table across 9 reference populations (100 people to 10 billion people)
- Feature breakdown with per-feature values and exclusion reasons
- Error direction note
- Conclusion statement
- Printable case record summary

## Important Notes

**Verification is required.** The calculator is an arithmetic tool. The examiner is responsible for verifying that inputs are correct and that the output is consistent with an independent hand calculation. A calculator output accepted without verification is not a T-Model calculation — it is a delegation of forensic judgment to a machine.

**The relevant population must be specified before calculation.** The choice of population must be grounded in case evidence, documented in the case record, and disclosed in testimony.

**Extrapolated position values (6–8 IR) must be flagged.** Any calculation incorporating these values should be noted in the case record and the resulting L treated as an estimate pending future close match validation.

**Features with sub-one combined values must be excluded.** If any feature's combined per-feature value (shape × position × latent grade × exemplar grade × agreement) falls below 1.00, that feature must be excluded from the calculation. A sub-one value reduces T rather than increasing it, producing a less conservative result.

**The T-Model does not replace examiner judgment.** The examiner provides all inputs — ridge feature type identifications, quality assessments, relevant population. The calculator performs the arithmetic. Professional judgment remains the controlling input throughout.

## Scientific Basis

The T-Model's discriminating values are derived from:

- Frequency of occurrence data based on the reconfigured Osterburg grid of 23,136 ridge unit cells
- Thirty-two close match experiments conducted across eight feature type groups using populations of flat fingerprint impressions
- Direct skin elasticity measurements from thirty-nine fingers from thirty-nine individuals

The model has been tested against three of the most extensively documented fingerprint lookalikes in the published forensic literature — the Madrid bombing error, the Chesapeake IAFIS lookalike, and the Clark lookalike — and correctly identified all three as insufficient for identification.

Full methodology, experimental results, and theoretical foundation are published in:

Templeman, H. — *T-Model v. 10.1: A Quantitative-Qualitative Framework for Latent Fingerprint Identification*

## License and Use

This calculator is made available for independent review, testing, and use by qualified fingerprint examiners, researchers, attorneys, and courts. The methodology is published and open to challenge. Any researcher who conducts close match experiments that confirm or contradict the model's predictions is encouraged to publish their results.

The T-Model's author has no proprietary interest in any specific value. The goal is accuracy. That goal is best served by open science.

This work is released under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**. Users are free to download, share, and adapt the material provided the following conditions are met:

- **Attribution:** Any use in casework, research, testimony, or publication must credit the T-Model v. 10.1 and its author, Henry Templeman.
- **Version identification:** Any modified version must be clearly identified as a modification and must not be represented as the official T-Model v. 10.1 calculator. Case records and testimony should specify which version was used.
- **Value integrity:** Any modification of the T-Model's discriminating values, position values, or formula produces a different model — not the T-Model v. 10.1 — and must not be presented as such in casework or testimony.

The author makes no warranty, express or implied, regarding the calculator's fitness for any particular purpose. Examiners are responsible for verifying all outputs independently before use in casework or testimony, as described in the accompanying book.

## Contact

The T-Model's methodology, values, and experimental results are published in full in the accompanying book. Researchers who wish to test, challenge, or extend the model have all the information needed to do so independently. The author is not available for correspondence.

---

*"Don't blindly believe, trust or accept this model.*
*Simply do the same experiments and find out*
*for yourself if it has any validity or not."*

— Henry Templeman
