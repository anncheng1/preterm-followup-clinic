# Preterm Infant Follow-Up Clinic

**Hospital Miri (Miri General Hospital) · Department of Neonatology / NICU**  
Developed by: Dr. Wong Ann Cheng, Neonatologist  


---

## Overview

A single-file, offline-capable web application for structured follow-up of preterm infants discharged from the NICU. Designed for use at point of care in the Preterm Follow-Up Clinic, Miri General Hospital, Sarawak, Malaysia.

## Features

| Feature | Detail |
|---|---|
| **Auto Corrected Age** | Calculated from DOB, birth gestation, and visit date. Displays corrected age, PMA, chronological age, and prematurity correction as colour-coded chips. |
| **Growth Charts** | Fenton 2013 (22–50 weeks PMA) transitioning to WHO 2006 (0–24 months CA). Corrected age used for plotting until 2 years CA, then chronological age. Weight, length/height, and head circumference charts. |
| **HINE Scoring Tool** | Full 26-item Hammersmith Infant Neurological Examination. Real-time domain subscores and total out of 78 with automatic interpretation (Normal / Suboptimal / High-risk). |
| **GMA Assessment** | Writhing and fidgety stage classification with interpretation guidance. |
| **Developmental Milestones** | Age-tabbed checklists (3–24 months CA) across 4 domains. Auto-selected based on corrected age. |
| **Red Flags** | Dedicated checklist of 10 developmental red flags across any visit age. |
| **Medical Systems Review** | Structured review of 7 organ systems (Respiratory/BPD, Cardiac, Neurology, Vision/ROP, Hearing, Endocrine, Medications). |
| **Plan & Referrals** | Therapy referrals, investigations, counselling checklist, follow-up scheduling, and clinical impression. |
| **Data & Analytics** | LocalStorage-based visit record logging, summary statistics, and CSV export for QI/audit. |

## Usage

No installation or internet connection required after the first load (Google Fonts are the only external dependency and are optional — the app degrades gracefully without them).

1. Open `index.html` in any modern browser (Chrome, Edge, Firefox, Safari).
2. Fill in patient details on the **Patient** tab — corrected age calculates automatically.
3. Enter anthropometry on the **Growth** tab — measurements plot automatically on the growth chart.
4. Complete **HINE**, **GMA**, **Development**, **Medical**, and **Plan** tabs as appropriate.
5. Click **Save** to log the visit record to browser localStorage.
6. Export records as CSV from the **Data** tab.
7. Print or save as PDF using the **Print/PDF** button (print-optimised CSS included).

## Clinical References

- **Fenton TR, Kim JH.** A systematic review and meta-analysis to revise the Fenton growth chart for preterm infants. *BMC Pediatrics* 2013;13:59.
- **WHO Multicentre Growth Reference Study Group.** WHO Child Growth Standards. Geneva: WHO, 2006.
- **Haataja L, et al.** Optimality score for the neurologic examination of the infant at 12 and 18 months of age. *J Pediatr* 1999;135(2):153–161. (HINE)
- **Einspieler C, Prechtl HFR.** Prechtl's assessment of general movements: a diagnostic tool for the functional assessment of the young nervous system. *MRDD Research Reviews* 2005.

## Scoring Reference — HINE

| Score | Interpretation |
|---|---|
| > 57 | Normal |
| 40 – 57 | Suboptimal |
| < 40 | High-risk for motor impairment |

*Interpretation is validated at 3–6 months corrected age and should always be integrated with clinical findings and developmental history.*

## Data & Privacy

All visit data is stored in the browser's **localStorage** only. No data is transmitted to any server. Data persists on the same browser/device between sessions and can be cleared from the Data tab. Suitable for use on a dedicated clinic workstation.

## File Structure

```
preterm-followup-clinic/
├── index.html        # Complete single-file application (HTML + CSS + JS)
└── README.md         # This file
```

## Deployment

### GitHub Pages (recommended)
1. Push to a GitHub repository.
2. Go to **Settings → Pages**.
3. Set source to `main` branch, root directory.
4. The app will be available at `https://<username>.github.io/<repo-name>/`.

### Local use
Simply open `index.html` directly in a browser — no web server required.

### Intranet / hospital network
Place `index.html` on any web server or shared network drive accessible to clinic computers.

## Version History

| Version | Date | Notes |
|---|---|---|
| v1.0 | 2025 | Initial build — patient details, medical review, development, plan, data export |
| v2.0 | 2025 | Added auto corrected age calculation, Fenton 2013 + WHO 2006 growth charts, full 26-item HINE scoring tool |

## Licence

For clinical and educational use within Hospital Miri and affiliated institutions. Not for commercial redistribution.

---

*Developed as part of quality improvement and clinical education initiatives in the NICU, Hospital Miri, Sarawak, Malaysia.*
[README.md](https://github.com/user-attachments/files/27313961/README.md)
