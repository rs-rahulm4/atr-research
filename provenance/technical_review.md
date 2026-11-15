# Technical review of the compiled manuscript

| Page and section | Review question | Applied revision or finding |
|---|---|---|
| p. 1, §1 Introduction | Does the pilot establish answer accuracy? | Identified the pilot as retrieval-only, attributed its numbers to the review, marked the unavailable raw evidence, and named the new outcome as generated-label agreement. |
| pp. 1–2, §2 Related Work | Is the contribution overstated? | Added MedRAG and BioHarness as precedents. Scoped the contribution to the paired result for the pinned small checkpoint and fixed lexical policy. |
| p. 2, §3.1 Questions and candidates | Is the test set leaking through the index? | Stated that the paired test abstracts are deliberately available, described the CONTEXTS-only fields and post-inference gold join, and separated fixed-corpus lookup from unknown training overlap. The prior audit matched the question/context hashes and rebuilt the rankings. |
| pp. 2–3, §§3.2–4.1 | Are comparators fair? | Specified identical question, instruction, checkpoint, decoder settings, input cap, and text handling across arms, with context as the intervention. Stated that C uses known source identity. The exported B/C inputs and predictions agree on all 433 source hits. |
| pp. 4–5, §5 Results and Fig. 2 | Are results traceable and accurate? | Checked the three 500-row arm summaries, 200 gains and 109 losses, 95% interval of 11.4–24.8 points, 433 source hits, and denominators in Tables 2–4 against the run export. Figure 2 uses those same prediction rows. Removed implied uncertainty estimates for secondary contrasts. |
| pp. 5–6, §§6–7 Discussion and Limitations | Do results support causal or general claims? | Restricted the intervention claim to paired context substitution in this run. Separated source identity from evidence quality, explicitly reported the majority comparator and missing maybe predictions, and framed proposed error mechanisms as untested explanations. |
| pp. 3, 6, §§4.2 and 9 | Could another reader reproduce it? | Mapped each reported output to an archive member. Included actual package versions, source hashes by manifest reference, and the run ID. Marked the executed notebook with Colab edits and complete console transcript as [TO VERIFY]. |

## Open items

- Export the edited notebook from the successful Colab runtime and retain it with the original evidence archive. Confirm the exact edited checkpoint-loading cell and whether an optional development run occurred. These actions improve provenance and require no changes to the verified scores.
- Training-data overlap and the raw retrieval-only pilot artifacts remain unresolved. Preserve the corresponding limits in any submission draft.
- The author line follows the approved brief. Verify the final author list with the instructor and collaborators before submission.

## Build

The assignment did not supply a separate instructor template in the provided materials. The source uses the ACM single-column manuscript format with conference-specific rights and publication metadata disabled. Upload the source ZIP to Overleaf and select `main.tex`, or build with `latexmk -pdf main.tex` in a TeX Live installation with ACM dependencies.
