# AI assistance audit

Prompt entries are short paraphrases of actual user requests. Tool was ChatGPT/Codex throughout, with Python for artifact creation and analysis, web search for primary-source metadata, and LaTeX for the paper. Colab execution was performed by the user.

| Interaction | Prompt and AI suggestion | User decision | Verification and outcome |
|---|---|---|---|
| 1 · Brief and literature | Read review and assignment, verify original papers and nearby comparisons. Suggested a matched three-arm design and limited the novelty claim. | User proceeded with the approved comparison. | Original sources were checked. The G1 brief distinguishes the retrieval-only pilot from generated-label outcomes. |
| 2 · Protocol | Freeze the official split, separate non-test smoke IDs, define ranking, parsing, and outcomes. | User requested six smoke IDs and an optional fixed non-test prompt-check subset. | The IDs and source hashes were checked and recorded before final outcomes. |
| 3 · Notebook and G2 | Make a single Colab notebook, default to smoke, and pause for actual output. | User uploaded the notebook to Colab and supplied errors and successful outputs. | Local checks verified split, index and scorer. Colab screenshots establish actual smoke inference and validation. |
| 4 · Debug and run | Diagnose narrowly, fix compatibility and run every test PMID. | User applied notebook edits, ran Sections 8–9, and uploaded the actual ZIP. | The full export contains 1,500 unique predictions, official test IDs, and the recorded CPU configuration. |
| 5 · Analysis | Score saved predictions, plot results, and choose examples by a transparent rule. | User requested analysis from supplied outputs. | Tables and bootstrap interval were independently recomputed. Example PMIDs were selected by lowest numeric ID within each category. |
| 6 · Manuscript | Draft and review a 6–10 page evidence-grounded paper. | User requested ACM style when no instructor template was provided. | Compiled six manuscript pages plus references. Applied traceability and scope revisions. Remaining gaps were marked [TO VERIFY]. |
| 7 · Submission | Keep one notebook, provenance, evidence and paper sources. | User requested a minimal GitHub package. | Code cells compiled locally. Archive-analysis cells reproduced four tables and exported the figure. Clean-Colab rerun and remote upload remain open. |

## Three genuine correction examples

1. **Checkpoint metadata.** The model loaded but the private `_commit_hash` assertion errored. AI suggested checking the revision-specific Hub snapshot while retaining the pinned model and tokenizer arguments. The user continued to successful inference. The exact final load cell was not shared. The archive manifest records the revision.
2. **Tokenizer compatibility.** Colab's tokenizer lacked the assembly helper. AI suggested reserving one encoder token and appending T5 EOS explicitly, including corresponding fixture updates. The user applied the helper. The smoke screenshots show the new fixture and validation PASS outputs.
3. **Smoke-mode skip.** Section 8 skipped official inference when `RUN_MODE` was still smoke. AI suggested changing and executing the Section 1 setting before Sections 8–9. The user supplied the completed ZIP. The 1,500 saved rows verify the final run occurred after the skip.

No failed attempt above generated a competing completed test result. The run archive documents the executed comparison. Primary literature sources are cited in the paper bibliography.
