# Author your first Skill, Customer Education work sample

A single-page, self-paced lesson teaching first-time skill authoring in ChatGPT. Built as a work sample for the OpenAI Customer Education, Learning Experience & Curriculum Lead role.

**One file. No dependencies. Open in any modern browser.**

---

## What to look at

[**lesson-author-your-first-skill.html**](./lesson-author-your-first-skill.html) is the lesson. Download, double-click, it runs.

It's a 45-minute hands-on lesson with 14 checkpoints, role-and-skill-type personalization (33 starter combinations), four learning objectives, an embedded simulation, a drag-and-drop placement exercise, a failure-mode diagnostic, a 4-question knowledge check, and a badge.

There's also a **LXD VIEW** toggle in the top-right of the page. Flip it on to see the design rationale layer: per-component callouts citing the learning-science principle behind each decision, MCQ-by-MCQ 19-IWF audit results, and the back-of-house cuts the design went through to land where it did. It's co-shipped specifically so a reviewer can audit my thinking without leaving the page.

---

## If you have 5 minutes

Open the lesson. Skim the hero, then jump to Step 01 (the workshop) and pick a role + type. Watch the personalization land. That's the core engagement loop in 90 seconds.

## If you have 15 minutes

Complete the lesson end-to-end. Workshop → lab handoff → "How skills work" → diagnostic → knowledge check → badge. The interactivity is the point; reading without doing misses the design.

## If you have 30 minutes

Do all of the above, then flip LXD VIEW on and re-scroll the page. Each callout names the pedagogy decision behind the component above it. Master design note is at the top under the hero LO box; per-component callouts attach to the components themselves.

---

## What this is meant to demonstrate

**AI-native production, not AI-discussed production.** The lesson's five MCQs were audited by `mcq-quality-coach`, a skill I built and then used on this lesson's own content. The MCQ design rationale documents this iteration: validator-flagged items, manual-audited items, distractors dropped or rewritten, with per-item analysis. It's exactly what the job description means by "use AI to accelerate course development and maintenance." The auditing skill is itself an artifact of the curriculum-production workflow this role builds.

**Hands-on by architecture, not assertion.** The page sequence (build first → explain after) was a deliberate pivot from concept-first based on drop-off data. The lab puts the learner in `chatgpt.com/skills` by minute 4. There is no passive video learning required; the orientation video at the top is brief and the rest of the page is interactive.

**Scaled personalization, not generic content.** The workshop reads the learner's role and skill type to choose 1 of 33 starter scenarios, then carries that customization through to the failure-mode diagnostic in section 1.4 (11 role-specific variants for process-type skills, plus a universal fallback). Surface varies; underlying KCs stay constant. Customizing the lesson to a new audience is a config swap, not a rewrite.

**Assessment design audited against research-supported rubrics.** Each MCQ went through `scripts/validate.py` for the 12 deterministic Haladyna-Downing item-writing flaw criteria, plus a semantic pass against the remaining 7. Four-option items were reduced to three (Rodriguez 2005). Per-item findings and revisions are documented in the LXD layer for transparency.

**Modular learning architecture.** The lesson uses an explicit backwards-design contract: four learning objectives → KC types → assessment-LO mapping → time-on-task per LO. The same scaffold can be filled in for any feature OpenAI ships. It's a template for the operating model the JD describes, not a one-off prototype.

---

## What this sample doesn't show

**Cohort-level analytics infrastructure.** Within-lesson signals (14 checkpoints, completion badge) are prototyped. Engagement-at-scale and behavior-change tracking would live in the surrounding LMS / analytics layer, which is out of scope for a single static deliverable.

**Program-level architecture.** This is Module 1, Lesson 1 of an implied 3-module pathway (M1: authoring → M2: integration → M3: evaluation). The sample shows one lesson at production polish; the program-level decisions (sequencing, credentialing, certification criteria) would be the next layer.

**Customer success motion integration.** In a production deployment, this lesson would hook into the CSM-led onboarding flow as an assignable asset during the customer's activation phase. The deliverable is designed for that drop-in deployment but doesn't show the integration itself.

---

## Design notes for the reviewer

The lesson went through three rounds of polish using Claude as a thinking and editing partner: structural review, redundancy passes, persona-based audits (novice enterprise user, learning-experience-designer, OpenAI Skills expert). The iteration is part of the artifact; the LXD layer documents the most significant design pivots (concept-first → build-first; pre-workshop prose cuts; assessment count reconciliation; LO 3 coverage rebalancing).

I'm transparent about AI use in production because the role is. The work demonstrated here is the kind of human-AI collaboration the JD asks for: AI for acceleration and QA, humans for taste and judgment about what to teach and how to sequence it.

---

## Built with

HTML, vanilla CSS, vanilla JS. No build step, no framework, no analytics SDK. One file, ~750 KB, ~9,800 lines. Loads instantly. Works offline after download. Mobile-responsive.

This is also a design choice: a self-paced learning asset that the customer can deploy anywhere, that doesn't depend on a vendor LMS, and that an enterprise customer can drop into their own learning platform without procurement friction.

---

## Contact

Submitting as part of the Customer Education, Learning Experience & Curriculum Lead application at OpenAI ([job posting](https://jobs.ashbyhq.com/openai/c4726cfd-59c2-4977-80c3-e2204ce27b8e)).
