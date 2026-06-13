---
title: "Search Strategy"
tags: [reference]
date: 2026-06-04
---

The weekly search runs one PubMed query per topic area, filtered to the **trailing 7 days** by entry date (`edat`). Queries below are stored machine-readably in `Resources/.search-queries.json`.

### [[AI & Machine Learning]]
```
(chronic rhinosinusitis OR rhinology OR sinusitis OR nasal polyps OR skull base) AND (artificial intelligence OR machine learning OR deep learning OR convolutional neural network OR radiomics OR large language model)
```

### [[Robotics, Automation & Ergonomics]]
```
(endoscopic sinus surgery OR skull base surgery OR rhinology OR endonasal) AND (robot OR robotic OR robotics OR automation OR autonomous OR ergonomics)
```

### [[Navigation, AR/VR, Simulation & 3D Printing]]
```
(sinus surgery OR endonasal OR skull base) AND (image-guided navigation OR augmented reality OR virtual reality OR mixed reality OR surgical simulation OR 3D printing OR computer-assisted surgery)
```

### [[Devices, Implants & Procedures]]
```
(chronic rhinosinusitis OR nasal polyps) AND (drug eluting stent OR sinus implant OR steroid eluting OR balloon sinuplasty OR mometasone implant OR device)
```

### [[Biologics & Medical Therapy]]
```
(chronic rhinosinusitis with nasal polyps) AND (dupilumab OR omalizumab OR mepolizumab OR tezepelumab OR stapokibart OR TSLP OR biologic OR monoclonal antibody)
```

### [[Endotypes, Biomarkers & Diagnostics]]
```
(chronic rhinosinusitis) AND (endotype OR biomarker OR phenotype OR proteomics OR eosinophil OR precision)
```

### [[Skull Base Surgery & Reconstruction]]
```
(endoscopic skull base OR endonasal) AND (reconstruction OR CSF leak OR nasoseptal flap OR outcomes OR complications)
```

### [[Outcomes, Guidelines & Epidemiology]]
```
(chronic rhinosinusitis OR sinus surgery) AND (patient reported outcome OR SNOT-22 OR quality of life OR registry OR guideline OR randomized)
```

## Supplementary sources (manual / web)

PubMed under-indexes pure-engineering and industry material. Each weekly run also scans:

- **arXiv / IEEE Xplore / Int J CARS** — surgical robotics, vision-guided navigation, foundation models for endoscopy
- **FDA 510(k)/De Novo database & manufacturer press** — new sinus/skull base device clearances
- **Google Scholar** — preprints, conference proceedings, and cross-disciplinary work
- **Society guidance** — ARS, EAACI/EPOS, AAO-HNS

---
*Primary index: PubMed (NCBI E-utilities).*
