---
layout: page
title: Clinical Hallucination Detection
description: Ontology-based detection of hallucinated claims in clinical LLM outputs, with coverage gating
importance: 2
category: research
related_publications: false
---

**Lab:** Data Science Lab, Montclair State University · **PI:** Dr. Hao Liu · **Status:** Under review at ICLR 2027

#### The problem

Large language models used in clinical settings can make clinical statements that are fluent but unsupported. These hallucinated claims are hard to spot by reading the output alone, and a single unsupported claim in a clinical summary can mislead a care decision.

#### The approach

This project checks the individual claims in a clinical LLM output against a structured clinical ontology. The check is **coverage-gated**: a claim is only judged by the ontology when the ontology actually contains the knowledge needed to verify it. This avoids treating a gap in the ontology as evidence that a claim is false.

#### My contributions

- **Contamination experiment.** Ran a held-out contamination test that deleted the ontology facts behind half of the benchmark claims and re-scored the system. This separates genuine reasoning gains from the method simply retrieving the answer key.
- **Label review.** Served as one of two annotators on a 110-claim clinical label review, reaching a Cohen's kappa of 0.966, and identified 6.4% of labels as context-dependent.
