## Peter Jemley

Informaticist and former intelligence analyst. Reading law at Vanderbilt.
New York · Arabic, French, German

I build systems that turn heterogeneous, partly adversarial, often unreliable evidence into something people can act on — and that decline to state a confidence they have not earned.

---

### Work

**[Bridget: Bridge Alerts](https://apps.apple.com/app/id6781426694)** · iOS, App Store
Infers drawbridge state from congestion telemetry. Confidence tiers are validated against a public ground-truth feed; locations with no such feed are labelled *unvalidated* rather than shown with an inferred probability. Federal navigation regulation (33 CFR §117) encoded as deterministic constraint. Swift, MapKit, SwiftData. 251 tests across 28 suites.

**[mcp-server-kleidiai](https://github.com/PeterJemley/mcp-server-kleidiai)** · Python, TypeScript
An MCP server giving agents provenance-verified access to a technical corpus on Arm CPU optimisation. Every indexed document carries source URL, pinned commit, timestamp, SHA-256 and licence; a file without a manifest entry fails the test suite. Retrieval measured against a 51-question held-out set: **41/51 (80%)**, report committed in-repo, all ten remaining failures categorised by mechanism and held as expected-failure tests. The score history keeps its regressions. Two of my own design hypotheses are on the record as refuted by measurement. Widening the answer key requires a curator's note in a dedicated commit. Includes a committed, reproducible kernel port — f32 matmul to KleidiAI int4, 2.4×–13.5× measured on Apple Silicon.

[`docs/evidence-discipline.md`](https://github.com/PeterJemley/mcp-server-kleidiai/blob/main/docs/evidence-discipline.md) maps each principle to the place the repository enforces it.

**[Continuous-Depth Transformers with Learned Control Dynamics](https://arxiv.org/abs/2601.10007)** · arXiv:2601.10007 [cs.LG], January 2026
Sole author. A hybrid transformer replacing discrete middle layers with a neural ODE block, giving inference-time control over generation via a learned steering signal. Contributes the Solver Invariance Test — a falsification diagnostic built to detect a specific failure of the architecture it evaluates.

**[Notes and shorter pieces](https://gist.github.com/PeterJemley)**

---

### Writing

**[Health Informatics at the Center of Patient Blood Management](https://gist.github.com/PeterJemley/a3928c36672bcb20a910f667fcc4f712)**
Systematic literature review from my master's work. 977 PubMed records screened to 52 articles and 7 reference works under Cochrane Handbook guidelines. Examines computerised decision support, predictive modelling, and guideline development in transfusion practice, and argues for integrating oxygen-transport data with haemoglobin thresholds in the decision.

**[Clinical Documentation Standards for Digitally-Created Pathology Reports](https://gist.github.com/PeterJemley/7804f96435b6df5e909c7e2b25b65352)**
Documentation standards — CDA, FHIR, HL7, PDF/A-3 — read against GDPR and German medical professional-code requirements. The argument is that semantic consistency can serve automated analysis and human readability at the same time, and that legal constraints are better treated as design parameters than as a compliance layer bolted on afterwards.

**[A Fundamental Identity for K-Means Clustering](https://gist.github.com/PeterJemley/086879d3a12ee39ff33bf301b17b1d49)**
A derivation. *An Introduction to Statistical Learning* states the identity between the pairwise-distance and cluster-mean formulations of within-cluster variation and asks for a proof; it supplies no method. Worked through in full, with the reasoning at each stage made explicit and an R check of the distance computation.

---

### Experience

**Independent — applied research and software** · Feb 2025 – present · New York
Bridget and mcp-server-kleidiai, above.

**Independent researcher** · Dec 2022 – present
Doctoral research proposal on intelligence-informed programme design in contested environments: collection planning, controlled evaluation, adversarial pre-mortem, boundary-setting. Comparative research on nineteenth-century industrial chemistry and contemporary AI.

**Public health informatics fellow, project lead** · May 2022 – Nov 2022 · Stanford School of Medicine / Solano County Public Health
Retrieval framework across CDC ESSENCE, CalREDIE and CAIR-2 — laboratory results, immunisation records, syndromic surveillance received continuously from every major health system and laboratory in the county. ETL and validation for California's Public Health Data Ecosystem, 35+ sources of social and environmental determinants joined to health outcomes at census-tract level. Introduced knowledge-ontology methods to a programme that had not used them. Worked under negotiated data use and business associate agreements.

**Independent educator** · Jan 2009 – Jan 2022 · Washington, Vermont, New Hampshire
Designed and taught a curriculum grounded in Popperian critical rationalism, treating instruction as continuous error correction. Completed the M.S. concurrently.

**Intelligence analyst and linguist** · Feb 2007 – Dec 2008 · National Security Agency and the Pentagon
Arabic and French linguist and analyst, Middle East counterterrorism, producing assessments from noisy and partly deceptive sources under statutory collection and retention limits that were audited and enforced. At the Office of Military Commissions, synthesised evidentiary material supporting military attorneys preparing capital cases, within classification, privilege and discovery constraints.

---

### Education

**Vanderbilt University Law School** — Master of Legal Studies, in progress
**Northeastern University** — M.S. Informatics (health informatics and mathematics), summa cum laude, 2019–2020
**University of Washington** — B.A. History, magna cum laude, Honors
**Defense Language Institute** — A.A. Modern Arabic, summa cum laude, Honors

---

Former TS/SCI (NSA). HIPAA trained, GDPR certified.
peter.w.jemley@vanderbilt.edu
