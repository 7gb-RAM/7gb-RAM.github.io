---
layout: page
title: CoChair
description: AI assistant for university faculty workflows. Pilot with the Biology Department at Montclair State University.
img: assets/img/projects/montclair_logo.png
importance: 2
category: engineering
featured: true
related_publications: false
---

**Role:** Technical Administrator · **Collaboration:** Cephgate LLC and the College of Science and Mathematics, Montclair State University · **Dates:** May 2026 – Present

CoChair is an AI assistant embedded in the Gmail sidebar that helps faculty handle student requests such as prerequisite overrides, capacity permits, advising referrals and room changes. For each email it identifies the request, retrieves the institutional policies that apply, recommends a decision and drafts a reply, without the faculty member leaving Gmail. The pilot runs in the Biology Department on synthetic data, with a FERPA-conscious design that keeps real student records out of scope until they are cleared.

My contributions:

- **Policy retrieval.** Improved retrieval over the department's policy corpus in Qdrant: searching the incoming email as a second query, replacing a fixed cosine-similarity cutoff with relative selection, adding applicability and precedence rules, and a recency tie-break for conflicting policies.
- **Reply drafting.** Made the recommendation's action buttons redraft the reply when a faculty member overrides the suggested decision, and kept internal document identifiers out of student-facing replies.
- **Policy management.** Built the settings screen for creating, editing and deleting policy documents, backed by Firestore.

Multi-intent classification reached 85.7% exact-set accuracy and 100% entity accuracy on the labeled seed set with an on-premises Llama 4 Scout model.

**Stack:** Python, FastAPI, Qdrant, Vertex AI (Gemini), vLLM (Llama 4 Scout), Google Apps Script, Firestore, Cloud Run.
