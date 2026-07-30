# Licensing and provenance of CFE-Bench

**Status: proposed — requires author sign-off before release.** This file records what the
provenance audit established and the licence that follows from it. It is not yet a
ratified licence grant.

> **Supersedes the declared licence.** The public HuggingFace dataset
> (<https://huggingface.co/datasets/analogyai/CFE_Benchmark>) declares `apache-2.0`. That
> declaration is incorrect and must be replaced. Apache-2.0 permits commercial use and
> sublicensing, contradicting the NonCommercial and ShareAlike terms that govern 50.8% of
> the content; and for the 221 rows whose sources state no licence, copyright rests with
> their authors, so an Apache-2.0 grant was never ours to make.

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

228 rows (50.8%) derive from MIT OpenCourseWare, which publishes under
[CC BY-NC-SA 4.0](https://ocw.mit.edu/terms/). The **ShareAlike** term requires that
derivative works be distributed under the same licence, and the **NonCommercial** term
forbids commercial use. Because those items are interleaved with the rest of the
benchmark rather than separable into a distinct file, the licence propagates to the
release as a whole:

> **CFE-Bench is released under CC BY-NC-SA 4.0.**
> <https://creativecommons.org/licenses/by-nc-sa/4.0/>

Attribution for the MIT OCW portion is given per item in `PROVENANCE.csv`
(`source_url`, `license`, `license_terms_url`).

Evaluation code (`generate_responses.py`, `evaluation.py`, `upload_huggingface.py`) is
**not** covered by the dataset licence and is released separately under the repository's
code licence.

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
URL. We make no claim that this is an express grant of permission.

## Takedown

Any rights holder who wishes their material removed may open an issue on
<https://github.com/GCYZSL/CFE_Benchmark>. Removals will be applied in a versioned
re-release, with the withdrawn item ids listed in the changelog.

## Regenerating this audit

```bash
python 0_build_provenance_and_croissant.py
```

Rebuilds `PROVENANCE.csv`, `SOURCES.csv`, `ANNOTATIONS.csv`, `REASONING_FLOW.csv`,
`croissant.json` and `croissant_hf.json` from the released files joined against the
upstream crawl pools. The licence column is driven by the `LICENSE_MAP` table at the top of
that script; extend it as further domains are verified.
