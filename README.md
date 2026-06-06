# t-model-fingerprint-calculator
Calculates number of fingerprint lookalikes for an arrangement of fingerprint ridge features in the relevant population.

T-Model v. 10.0 Fingerprint Calculator
A quantitative-qualitative framework for latent fingerprint identification 
Developed by Henry Templeman

Overview

The T-Model Fingerprint Calculator is a standalone HTML tool that implements the T-Model v. 10.0 — a quantitative, qualitative empirically grounded framework for fingerprint identification developed by Henry Templeman. The calculator allows latent print examiners to compute the estimated number of fingerprint lookalikes in a relevant population based on the discriminating values of matching ridge features, their spatial positions, and the quality of their correspondence.

The T-Model is described in full in: Templeman, H. — T-Model v. 10.0: 
A Quantitative-Qualitative Framework for Latent Fingerprint Identification
(publication pending)

Full title
Author name
Publisher name (or "Self-published" if going through KDP)
Year of publication
ISBN number


What the Calculator Does

Given a set of matching ridge features assessed during latent vs exemplar fingerprint analysis and comparison, the calculator:
Computes the T-Value — the total discriminating value of the matching arrangement
Calculates L — the estimated number of fingerprint arrangements in the relevant population as similar to the one found in correspondence
Returns a sufficiency verdict: Supported (L ≤ 1), Borderline (1 < L ≤ 2), or Insufficient (L > 2)
Displays a sufficiency table showing L across a range of reference populations from 100 people to 10 billion people
Produces a case record summary documenting every input and every computed value for inclusion in the case file
The formula used is: L = 120 × N / (T × log₁₀T)

where N is the number of individual fingerprints in the relevant population, T is the T-Value, and 120 is the exponent of 10^120 — the estimated discriminating value of the average complete flat fingerprint.

How to Use

The calculator is a single self-contained HTML file. No installation, no server, no internet connection required.
Download tmodel_calculator_v4.html
Open it in any modern web browser (Safari, Chrome, Firefox, Edge)
To add it to your iPad or iPhone home screen: open in Safari → Share → Add to Home Screen
To save to desktop: open in browser → File → Save As

Input Fields

Step 1 — Relevant Population 

Enter the number of individual fingerprints in the relevant human population:
Witness-identified suspect in a bounded location: enter the appropriate smaller population
National default (300 million people): enter 3,000,000,000 fingerprints
AFIS database search: enter the documented size of the database searched at the time of the search

Step 2 — Elasticity Threshold Confirmation 

Before entering features, confirm that all corresponding feature pairs have been assessed against the T-Model's elasticity thresholds:
Linear displacement ≤ 20% (measure with millimeter ruler if needed)
Rotational displacement ≤ 10 degrees (measure with protractor if needed)
Features that exceed either threshold must be excluded

An expandable step-by-step measurement guide is available within the calculator.

Step 3 — Feature Pairs 

Enter one matched feature pair per row:
Feature type (latent and exemplar independently)
Intervening ridge count to nearest Level 2 neighbor (IR)
Clarity/Reliability Grade (A through F)
Quality of Agreement (Excellent, Satisfactory, or Unsatisfactory)

Features assigned Grade F or Unsatisfactory agreement are automatically excluded from the calculation.

Feature Types and Values


‡ Value based on frequency of occurrence study only; not validated through close match experiments. Use with appropriate caution and flag in case record.


Position Values (IR)



* Values at 6–8 IR are mathematical extrapolations of the confirmed 3–5 IR pattern and have not been independently validated through close match experiments. Flag in case record when used.


Clarity/Reliability Grade Scale





Quality of Agreement



Connectivity disagreements (one impression shows an ending ridge, the other a bifurcation, at the same spatial location) that are within spatial tolerance should be rated Satisfactory.


Sufficiency Verdicts




Output

After pressing Calculate, the calculator produces:

T-Value (combined conservative):
Formula: L = 120 × N / (T × log₁₀T)
L value: 
Sufficiency table across 9 reference populations (100 people to 10 billion people)
Feature Breakdown
Error direction:
Conclusion:
Printable case record summary


Important Notes

Verification is required. The calculator is an arithmetic tool. The examiner is responsible for verifying that inputs are correct and that the output is consistent with an independent hand calculation. A calculator output accepted without verification is not a T-Model calculation — it is a delegation of forensic judgment to a machine.

The relevant population must be specified before calculation. The choice of population must be grounded in case evidence, documented in the case record, and disclosed in testimony.

Extrapolated position values (6–8 IR) must be flagged. Any calculation incorporating these values should be noted in the case record and the resulting L treated as an estimate pending future close match validation.

The T-Model does not replace examiner judgment. The examiner provides all inputs — ridge feature type identifications, quality assessments, relevant population. The calculator performs the arithmetic. Professional judgment remains the controlling input throughout.

Scientific Basis

The T-Model's discriminating values are derived from:
Frequency of occurrence data based on the reconfigured Osterburg grid of 23,136 ridge unit cells
Thirty-two close match experiments conducted across eight feature type groups using populations of 200 to 1,000 flat fingerprint impressions
Direct skin elasticity measurements from thirty-nine fingers from thirty-nine individuals

The model has been tested against three of the most extensively documented fingerprint lookalikes in the published forensic literature — the Madrid bombing error, the Chesapeake IAFIS lookalike, and the Clark lookalike — and correctly identified all three as insufficient for identification.

Full methodology, experimental results, and theoretical foundation are published in: Templeman, H. — T-Model v. 10.0: A Quantitative-Qualitative Framework for Latent Fingerprint Identification
License and Use

This calculator is made available for independent review, testing, and use by qualified fingerprint examiners, researchers, attorneys, and courts. The methodology is published and open to challenge. Any researcher who conducts close match experiments that confirm or contradict the model's predictions is encouraged to publish their results.
The T-Model's author has no proprietary interest in any specific value. The goal is accuracy. That goal is best served by open science.

This work is released under the Creative Commons Attribution 4.0 International License (CC BY 4.0). Users are free to download, share, and adapt the material provided the following conditions are met:

Attribution: Any use in casework, research, testimony, or publication must credit the T-Model v. 10.0 and its author, Henry Templeman.
Version identification: Any modified version must be clearly identified as a modification and must not be represented as the official T-Model v. 10.0 calculator. Case records and testimony should specify which version was used.
Value integrity: Any modification of the T-Model's discriminating values, position values, or formula produces a different model — not the T-Model v. 10.0 — and must not be presented as such in casework or testimony.

The author makes no warranty, express or implied, regarding the calculator's fitness for any particular purpose. Examiners are responsible for verifying all outputs independently before use in casework or testimony, as described in Chapter 16 of the accompanying book.

Contact
The T-Model's methodology, values, and experimental results are published in full in the accompanying book (book pending publication) . Researchers who wish to test, challenge, or extend the model have all the information needed to do so independently. The author is not available for correspondence.
"Don't blindly believe, trust or accept this model. 
Simply do the same experiments and find out
for yourself if it has any validity or not.”
 
                  — Henry Templeman
