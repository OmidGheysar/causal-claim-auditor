# Limitations

This is a prototype. Known ways it can go wrong:

- **Search coverage.** The tool only sees what web search returns. Paywalled papers, older literature, and non-English studies may be missed. It often works from abstracts or summaries, not full texts.
- **Extraction errors.** The model can misread a study's design (for example, labelling a cross-sectional study as a cohort) or misstate its main finding.
- **Reasoning errors.** The model can miss a well-known confounder, or name one that does not apply.
- **Calibration.** Scores have not yet been validated against expert judgement on a reference set of claims.
- **Claim phrasing.** Vague or compound claims ("X is bad for you") are hard to audit. Specific exposure → outcome claims work best.
- **Diagrams.** The DAG is a simplified sketch of the main causal structure, not a full model.
- **Shared networks.** The 3-audit limit is per IP address, so visitors on the same office or campus network share it.
- **Not advice.** Results are not medical, legal, or professional advice.

Found a case where it is wrong? Please open an issue with the claim and what you expected.
