## Peter Jemley

Informaticist and former intelligence analyst. Graduate student at Vanderbilt University Law School.
New York · Arabic, French, German

I build systems that take in evidence which is uneven in quality, partly shaped by someone who wants to mislead, and often incomplete, and turn it into something an organisation can act on. Each of them refuses to state a confidence it has not earned, which in practice means that where a number has not been checked against anything, the system says so instead of showing the number.

---

### Work

**[Bridget: Bridge Alerts](https://apps.apple.com/app/id6781426694)** · iOS, App Store
Estimates whether a drawbridge is open by watching traffic congestion around it. Where a public data feed exists to check those estimates against what actually happened, the application shows a confidence level derived from that comparison. Where no such feed exists, it labels the location *unvalidated* and shows no probability at all, because to a user an unchecked number and a checked one look identical. Federal drawbridge regulation — 33 CFR §117, which sets when bridges may and may not open — is written in as a fixed rule rather than something the system tries to infer. Swift, MapKit, SwiftData. 251 tests across 28 suites.

**[mcp-server-kleidiai](https://github.com/PeterJemley/mcp-server-kleidiai)** · Python, TypeScript
A server built on the Model Context Protocol, a standard that lets AI assistants call external tools. It gives those assistants searchable access to a curated collection of technical documents on Arm CPU optimisation. Every document in the collection carries its source address, the exact version it was taken from, a timestamp, a cryptographic fingerprint that changes if the file changes, and its licence. A file missing any of these fails the automated checks and cannot enter the collection.

Accuracy is measured against 51 test questions with known correct answers: **41 correct**, in a report committed to the repository. Each of the ten remaining failures is categorised by cause and held as a test marked *expected to fail*, which breaks the build if it starts passing — so an improvement cannot slip by unnoticed. The score history keeps its declines: an earlier expansion of the collection dropped the score from 22 out of 30 to 18 out of 30, and that decline is still in the report. Two design ideas of my own are recorded there as refuted by measurement. Widening the list of answers counted as correct requires a written note from the curator in a commit of its own, because quietly loosening the standard is the easiest way to make a system appear better than it is. Also included: a port of a matrix-multiplication routine to Arm's KleidiAI library at reduced numerical precision, measured at 2.4× to 13.5× faster on Apple Silicon, with the benchmark committed so it can be re-run.

[`docs/evidence-discipline.md`](https://github.com/PeterJemley/mcp-server-kleidiai/blob/main/docs/evidence-discipline.md) sets out each of these principles next to the place in the repository that enforces it.

**[Clinical-Information-Retrieval](https://github.com/PeterJemley/Clinical-Information-Retrieval)** · Python
A retrieval framework for a situation where matching the subject matter is required but does not by itself make a document the right one to read. It scores medical documents on how recent they are, judged against how quickly work in that field stops being cited; on the strength of the study design behind them, drawn from published rankings of study types; and on how well they apply to the patient in question and how far they support a decision. Every design assumption is labelled by how much support it has: derived from theory, chosen on judgement and to be tested for sensitivity, or conjecture put forward to be tested and reported either way.

The success criterion was registered before any test was run: the system had to beat a standard word-matching retrieval method by at least 5% on NDCG@10, a common measure of how well a ranked list of results matches human judgements of relevance. **The test ran on 23 August 2026 and the system failed it.** It scored 0.071 against the baseline's 0.310 on NFCorpus, a public medical retrieval benchmark, across 323 questions, and the ranges of statistical uncertainty around the two figures do not overlap.

Committed alongside the result: the component-by-component breakdown, which showed that the meaning-based part of the system was making results worse rather than better; the two criteria the test dataset could not evaluate at all, with the reasons; and a defect the run exposed, namely that the language model named in the configuration file was never loaded by any code in the repository. A companion note sets out what the failure establishes and what it does not.

**[Continuous-Depth Transformers with Learned Control Dynamics](https://arxiv.org/abs/2601.10007)** · arXiv:2601.10007 [cs.LG], January 2026
Sole author. A transformer architecture whose middle layers, ordinarily a fixed stack of discrete steps, are replaced by a continuous process described by a differential equation. This allows the character of the generated text to be steered while it is being produced rather than only at training time. The methodological contribution is a diagnostic I called the Solver Invariance Test, built to detect one specific way the architecture could have been wrong: I constructed the instrument that could have refuted my own result, ran it, and published the number.

**[Notes and shorter pieces](https://gist.github.com/PeterJemley)**

---

### Writing

**[Health Informatics at the Center of Patient Blood Management](https://gist.github.com/PeterJemley/a3928c36672bcb20a910f667fcc4f712)**
A systematic literature review from my master's work, conducted under the Cochrane Handbook guidelines, which are the standard method for synthesising medical evidence. 977 PubMed records were screened down to 52 articles and 7 reference works. The review examines computerised decision support, predictive modelling, and guideline development in transfusion practice, and argues that the decision to transfuse should take account of how much oxygen the blood is actually carrying, alongside the haemoglobin threshold conventionally used on its own.

**[Clinical Documentation Standards for Digitally-Created Pathology Reports](https://gist.github.com/PeterJemley/7804f96435b6df5e909c7e2b25b65352)**
Four standards governing how a clinical document is structured so that software can read it — CDA, FHIR, HL7 and PDF/A-3 — read against the General Data Protection Regulation and the professional codes governing German physicians. Two arguments. First, that a document can be consistent enough for a machine to analyse and still be readable by a person, so the two goals need not be traded against one another. Second, that the legal requirements should be treated as design parameters from the start, because a system built without them and then adjusted to satisfy them satisfies them badly.

**[A Fundamental Identity for K-Means Clustering](https://gist.github.com/PeterJemley/086879d3a12ee39ff33bf301b17b1d49)**
A derivation. *An Introduction to Statistical Learning* states an identity — an equation holding for all values, showing two apparently different formulations to be the same quantity — between the pairwise-distance and cluster-mean expressions of within-cluster variation, and asks the reader for a proof. It supplies no method. Worked through in full, with the reasoning at each stage made explicit and a check of the distance computation written in R.

---

### Experience

**Independent — applied research and software** · Feb 2025 – present · New York
Bridget and mcp-server-kleidiai, above.

**Independent researcher** · Dec 2022 – present
A doctoral research proposal setting out a four-part method for designing programmes in environments where the people being studied have their own reasons to shape what an investigator sees: deciding what to collect before collecting it, evaluating interventions against controls, working out in advance how the programme could fail, and setting limits on what may be collected. Separately, comparative research on the industrialisation of nineteenth-century organic chemistry and the current development of artificial intelligence.

**Public health informatics fellow, project lead** · May 2022 – Nov 2022 · Stanford School of Medicine / Solano County Public Health
Built a unified search framework across three county-wide data streams — laboratory results, immunisation records, and the presenting complaints recorded when patients arrive at an emergency department — received continuously from every major hospital and laboratory in the county. Engineered the pipelines that moved and reshaped the data for California's Public Health Data Ecosystem, joining more than 35 sources of social and environmental information to health outcomes at the level of individual census tracts. Introduced formal ontology methods — explicit, machine-readable definitions of the entities in a domain and the relationships between them — to a programme that had not previously used them, on my own initiative. Worked under negotiated data use and business associate agreements governing what could be collected, linked, and shared.

**Independent educator** · Jan 2009 – Jan 2022 · Washington, Vermont, New Hampshire
Designed and taught a curriculum grounded in Karl Popper's critical rationalism, the position that knowledge advances by finding and correcting errors rather than by accumulating confirmations, and treated instruction accordingly. Completed the M.S. concurrently with the final years of this work.

**Intelligence analyst** · Jan 2008 – Dec 2008 · AllWorld Language Consultants, Inc., assigned to the Office of Military Commissions, the Pentagon
Cleared contract analyst; transferred clearances in person to the Office. Synthesised dense evidentiary material supporting military attorneys preparing capital cases — prosecutions in which the death penalty is available — working at the same time inside classification rules, the protection that keeps a lawyer’s communications with a client confidential, and the obligation to disclose material to the other side. Resigned in December 2008.

**Arabic linguist and analyst** · Jun 2005 – Jan 2010 · United States Army and Army National Guard
Intermittent active duty and National Guard service. Language training at the Defense Language Institute Foreign Language Center, Oct 2005 – Apr 2007. Assigned to the National Security Agency from Aug 2007, Middle East counterterrorism mission, in uniform: producing assessments from source material that was noisy, partly shaped to mislead, and incomplete, under limits on collection and retention set by statute, audited, and enforced.

---

### Education

**Vanderbilt University Law School** — Master of Legal Studies, May 2026 – Dec 2027 expected  
**Fordham University, Center for Jewish Studies** — Werthein Fellow, Fall 2026  
**Fordham University, Graduate School of Arts and Sciences** — M.A. Humanitarian Studies, admitted, deferred to the next academic year  
**Northeastern University** — M.S. Health Informatics, Bouvé College of Health Sciences, *summa cum laude*, 2019–2020  
**University of Washington** — B.A. History, *magna cum laude*, Honors, conferred 17 August 2018  
**Defense Language Institute Foreign Language Center** — A.A. Modern Arabic, *summa cum laude*, Honors, 2005–2007  
**Seattle Central Community College** — A.A., August 2000  
**Lake Washington Institute of Technology** — Diesel and Heavy Equipment Technology, 2004–2005, 65 credits, 4.00, President’s List; left to enter the Army  

---

Former TS/SCI (NSA). HIPAA trained, GDPR certified.
peter.w.jemley@vanderbilt.edu
