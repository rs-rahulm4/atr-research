# Five-minute demo

| Time | Show and say |
|---|---|
| 0:00–0:45 | Open the G1 brief. Ask whether a single retrieved abstract improves exact PubMedQA label agreement for a fixed FLAN-T5-small checkpoint. |
| 0:45–1:45 | Show a preloaded smoke notebook and run or show the six non-test question triples. Open the PASS output for ranking, parsing, pairing and truncation. |
| 1:45–2:45 | Open the real results table. Show 34.6%, 52.8%, and 53.4%, and explain the paired +18.2-point gain and the 11.4–24.8 interval. |
| 2:45–3:45 | Show PMID 7860319. TF–IDF found its reference source, but both context arms predicted no against gold yes. Explain the distinction between successful source lookup and correct label prediction. |
| 3:45–5:00 | Show the fixed 1,000-document pool and the unknown training overlap. Explain that all arms missed the maybe class and fell below the 55.2% always-yes rule. Point to the archive and show how to regenerate the figure without rerunning the model. |

## Submission checklist against assignment §8

| Item | Evidence | Status |
|---|---|---|
| A · Research paper | Compiled PDF, six manuscript pages plus references, along with LaTeX, BibTeX and figure | Ready |
| B · GitHub repository | One notebook, README, versioned analysis dependencies and frozen settings | Bundle ready. Push to GitHub and submit URL. Clean-Colab inference is [TEST REQUIRED]. |
| C · Experimental evidence | Original prediction ZIP, comparison/stratum tables, manifest and seeds, paper figure, smoke screenshots | Ready. Full console transcript unavailable. |
| D · Research provenance | G1 brief, G2 smoke report, decisions and AI audit with three real debugging examples | Ready |
| E · Demonstration | Timed walkthrough and smoke/analysis entry points | Rehearse and confirm a live component reruns. |
| Course submission details | Folder naming includes enrollment number or approved group ID | Fill in identifier and check the submission location and deadline in Google Classroom. |
