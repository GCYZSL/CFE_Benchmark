# Licensing and provenance of CFE-Bench



## Summary

CFE-Bench is assembled from problems published on the open web by universities,
departments and competition organisers. Every one of the 449 released rows has a recorded
source URL; the full per-item mapping is in [`PROVENANCE.csv`](PROVENANCE.csv) and the
per-domain roll-up is in [`SOURCES.csv`](SOURCES.csv).

| | rows | share |
|---|---:|---:|
| MIT OpenCourseWare — CC BY-NC-SA 4.0 | 228 | 50.8% |
| Sources stating no licence | 221 | 49.2% |
| **Total** | **449** | |

## Why the dataset is CC BY-NC-SA 4.0

228 rows (50.8%) derive under
[CC BY-NC-SA 4.0]. The **ShareAlike** term requires that
derivative works be distributed under the same licence, and the **NonCommercial** term
forbids commercial use. Because those items are interleaved with the rest of the
benchmark rather than separable into a distinct file, the licence propagates to the
release as a whole:

> **CFE-Bench is released under CC BY-NC-SA 4.0.**
> <https://creativecommons.org/licenses/by-nc-sa/4.0/>

Attribution for the MIT OCW portion is given per item in `PROVENANCE.csv`
(`source_url`, `license`, `license_terms_url`).


## The 221 rows with no stated licence

The remaining rows come from 53 domains — individual instructor course pages,
departmental qualifying-exam archives, and physics/mathematics olympiad papers. For six
of these domains we checked the publisher's own terms page directly (covering 302 rows in
total, including MIT OCW); none of the five non-OCW verified domains states a licence,
reuse grant or redistribution restriction:

| Domain | Rows | Terms page checked |
|---|---:|---|
| ocw.mit.edu | 228 | <https://ocw.mit.edu/terms/> — CC BY-NC-SA 4.0 |
| knzhou.github.io | 34 | <https://knzhou.github.io/> — no licence stated |
| ipho.olimpicos.net | 14 | <https://ipho.olimpicos.net/> — no licence stated |
| galois.math.ucdavis.edu | 12 | <https://galois.math.ucdavis.edu/doku.php?id=start> — no licence stated |
| www.aapt.org / aapt.org | 14 | <https://www.aapt.org/physicsteam/PT-exams.cfm> — no licence stated |

"No licence stated" means the material remains under its authors' default copyright. We
redistribute it for non-commercial academic research, in transformed form (OCR'd text and
cropped figures rather than the source PDFs), with per-item attribution to the original
URL.