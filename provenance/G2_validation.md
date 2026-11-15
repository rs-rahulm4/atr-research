# G2 baseline validation

Source: Colab smoke screenshots alongside this document. Six fixed non-test PMIDs, three matched arms, 18 predictions.

| Condition | Correct / 6 | Accuracy | Macro-F1 | Invalid |
|---|---:|---:|---:|---:|
| Closed-book | 1 | 16.7% | 0.095 | 0 |
| TF–IDF top-1 | 5 | 83.3% | 0.556 | 0 |
| Reference | 5 | 83.3% | 0.556 | 0 |

**VERIFIED.** The ranking fixture covered an exact match, smallest-PMID tie resolution, and an all-zero query. The long-input fixture retained the prompt prefix and reached the 512-token cap. Label parsing and shuffled-PMID scoring passed. All 18 rows paired, repeated inference agreed, and forced source-hit and zero-score inputs produced matching labels as expected. TF–IDF retrieved the paired source for five of six smoke questions. No smoke query yielded an all-zero score. The export/scoring cell displayed the PMID join PASS.

**NEEDS CORRECTION, resolved in the actual run.** The original notebook used a private configuration attribute and an unavailable tokenizer helper. The user ran the repaired notebook through smoke and full comparison. The tokenizer fixture shows the EOS helper. Both compatibility changes are recorded in the AI audit.

**UNCERTAIN.** Exact final loading-cell text and full console transcript were unavailable. These results are from six non-test questions and serve as engineering validation. The reconstructed submission notebook has not been rerun end to end.
