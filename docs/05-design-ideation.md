---
title: Ideation and Concept Generation
---

# Ideation and Concept Generation

<!-- ============================================================
     HOW TO WORK ON THIS PAGE
     (HTML comments do not appear on the published page or in the PDF.
     No need to delete them when you are done.)

     WHAT THE ASSIGNMENT GRADES (from the checklist on the course site)
       - Page is easy to find (linked from the landing page) and well formatted
       - Goal of the product and the audience are clearly stated     -> §1
       - ~100 brainstormed features, each tied to a need/requirement -> §2, §3
       - Snapshots of the brainstorm at DIFFERENT stages             -> §4.4
       - Features sorted/grouped AND ranked                          -> §4
       - Three high-quality, distinct concepts as drawing / mockup /
         storyboard / video, with the selected features annotated
         with labels AND arrows                                      -> §5
       - A 1-page description of the ideation process                -> §6
       Points: 50 initial (completeness) + 150 external design review
       (quality) + 50 final report = 250. Only the first 50 are
       completeness; the other 200 are judged on quality.

     OWNERSHIP (mirrors who owned which aspects in Product Requirements)
       Zice    — §1 Goal & Audience, §2 Prioritization, §3.1 feature table,
                 §5.1 Concept A, §6 one-page discussion (draft),
                 AI disclosure, site build / landing-page link /
                 PDF export / Canvas submission
       Gabriel — §3.2 feature table, §4.2 Ranking (scoring sheet),
                 §5.2 Concept B
       Duotao  — §3.3 feature table, §4.1 Grouping, §4.4 Snapshots
                 (session scribe), §5.3 Concept C
       Everyone — the live brainstorm session, §4.3 new features,
                 §5.4 concept comparison, review §6 before export

     ORDER OF WORK (the assignment says "capture and save" three times —
     do not skip the snapshots, they cannot be recreated afterwards)
       1. Each owner pre-seeds ~15 features in their §3 table ALONE,
          before the meeting. Individual-first brainstorming produces
          more distinct ideas than starting in a group.
       2. Team session: pool everything on one board (Miro / FigJam /
          Google Slides). Add, build on each other's ideas, no criticism.
          Fill each §3 table up to its target.   -> SNAPSHOT 1 (raw)
       3. Sort into themed groups, rank inside each group, write down any
          new combined features.                  -> SNAPSHOT 2 (grouped)
       4. Pull features into three concept bins. Unused features stay
          on a "parking lot" area, never deleted. -> SNAPSHOT 3 (binned)
       5. Each owner produces their concept figure (§5).
       6. Zice drafts §6, team reviews, then build -> check -> PDF.

     THREE HARD RULES
       1. Every feature row has a Req ID from the Product Requirements page
          (HW/SW/UX/CU/MF/SF). No Req ID = the idea is not tied to a need,
          and the assignment is explicitly about "solutions that are needed".
       2. Nothing on this page may be just a link to a living document
          (Google Docs/Sheets, Miro, draw.io). Export PNG/SVG into
          docs/image/ideation/ and embed it. File names: no spaces.
       3. Keep tables to 4-5 short columns and split long lists into
          several small tables — wide or long tables break badly in the
          PDF export (same rule as the Requirements page).

     FEATURE ID SCHEME (used everywhere on this page)
       F-001 ... F-100   features from the brainstorm (§3)
       F-N01 ... F-Nxx   new features created during discussion (§4.3)
       G1 ... Gn         feature groups (§4.1)
       Concept A / B / C (§5)
     ============================================================ -->

## 1. Product Goal and Audience

<!-- OWNER: Zice
     WHAT: 3-5 sentences. The checklist explicitly grades "clearly identify
     the goal" and "clearly identify your audience" — do not assume the
     reader has read the earlier pages.
     HOW: restate the product in one sentence (reuse the wording of
     §1.1 Project Objective on the Requirements page so the pages agree),
     name the primary and secondary users from the stakeholder table,
     then one sentence on what this page does.

     EXAMPLE 1 (goal sentence):
       "Team 103 is developing a prescription-based automatic resistance
        grip trainer that measures the force a patient applies and sets
        its own resistance to a level prescribed by a clinician."
     EXAMPLE 2 (audience + page purpose):
       "The primary users are physical and occupational therapists; the
        secondary users are patients exercising at home between clinic
        visits. This page records how the team generated about 100
        candidate features for that device and recombined them into
        three distinct product concepts." -->

## 2. Prioritization of Needs and Requirements

<!-- OWNER: Zice
     WHAT: The assignment's "Update" asks you to explain HOW you chose
     which needs/requirements to brainstorm on, and whether you used the
     user-needs weighting from the earlier assignment. This section answers
     that directly.

     HOW (the method this skeleton is built on — change it if the team
     decides differently, but then update the table):
       - Start from the 32 requirements on the Product Requirements page.
       - Each requirement inherits the mean importance of the need category
         of its Source (UN c.n -> category c, Table 2 of the User Needs
         page). If a requirement cites needs from two categories, use the
         higher category mean.
       - Drop requirements that are process or documentation obligations
         rather than design choices (e.g. SF-05 risk file, MF-04 BOM
         alternates) — there is nothing to "brainstorm 5 features" for.
       - Merge requirements whose solutions would overlap (e.g. SW-02 and
         CU-02 both limit resistance to the authorized maximum).
       - Keep the top 20 -> 20 prompts x 5 features = 100 features, which
         meets the ~100 target exactly.
     Write 1 short paragraph explaining this in your own words, then the
     table. Say explicitly: "Yes, we used the category weights from the
     User Needs assignment", and say what else influenced the choice.

     EXAMPLE sentence 1:
       "Rather than brainstorming on all 32 requirements equally, we
        weighted each requirement by the mean importance of the need
        category it traces to."
     EXAMPLE sentence 2:
       "Requirements that describe a process rather than a feature, such
        as maintaining a risk file, were set aside because they do not
        have alternative physical or software solutions."

     The table below is the PROPOSED allocation and is also the division
     of work for §3. Adjust at the team meeting; if you change a row,
     change the matching §3 table in the same edit. -->

**Table 1. Requirements selected as brainstorm prompts, in priority order.**

| # | Req ID | Prompt (short) | Weight | Owner |
|---|---|---|---|---|
| 1 | SW-01 | Resistance follows the prescription automatically | 4.33 | Gabriel |
| 2 | SF-01 | Resistance never exceeds the authorized maximum | 4.33 | Zice |
| 3 | CU-01 | Therapist sets resistance and repetition target | 4.33 | Duotao |
| 4 | CU-03 | Resistance adapts to measured performance | 4.33 | Duotao |
| 5 | HW-01 | Grip span fits 5th–95th percentile hands | 4.14 | Gabriel |
| 6 | UX-01 | Session starts in ≤ 3 operations | 4.14 | Duotao |
| 7 | UX-03 | Resistance and repetition progress are visible | 4.14 | Duotao |
| 8 | UX-04 | Operable with weak or stiff hands | 4.14 | Duotao |
| 9 | UX-05 | Patient is notified when the target is reached | 4.14 | Duotao |
| 10 | SF-04 | Skin-contact surfaces are safe and cleanable | 4.09 | Zice |
| 11 | SF-02 | Resistance can be released by hand without power | 4.07 | Zice |
| 12 | HW-05 | Moving parts cannot pinch the user | 4.07 | Gabriel |
| 13 | HW-03 | Carried in one hand, no installation | 3.83 | Gabriel |
| 14 | MF-05 | Unit cost supports individual ownership | 3.83 | Gabriel |
| 15 | SW-06 | Grip force is measured accurately | 3.74 | Zice |
| 16 | SW-04 | Repetitions are counted automatically | 3.74 | Zice |
| 17 | MF-03 | Force sensing calibrates with known loads | 3.74 | Zice |
| 18 | MF-02 | Sensing and motor signals can be probed | 3.74 | Zice |
| 19 | SW-03 | Session data survives power loss | 3.74 | Gabriel |
| 20 | SW-05 | Records export without custom software | 3.74 | Gabriel |

<!-- Workload check: Zice 7 prompts (35 features), Gabriel 7 (35),
     Duotao 6 (30) = 100. Duotao has one fewer prompt because Duotao also
     scribes the live session and captures the snapshots (§4.4).
     Note that the Measurement & Data prompts rank lowest by category mean
     even though SW-06 contains some of the highest-rated individual needs —
     the User Needs page (§4.1 there) already explains why. Worth one
     sentence here so a reviewer does not think sensing was deprioritized. -->

## 3. Initial Capture of Design Features

<!-- WHAT: Step 2 of the assignment. For each prompt in Table 1, five
     different features that could satisfy it. Goal: SMALL ideas that can
     later be mixed into different full solutions.

     HOW:
       - Five features per prompt must be genuinely DIFFERENT approaches
         (different physics, different interaction, different part of the
         system), not five sizes of the same thing. "Load cell 10 kg /
         20 kg / 50 kg" is one idea, not three.
       - Brainstorm rules from the assignment: no criticism, wide variety,
         build on each other's ideas, unrealistic ideas are welcome. Aim
         for at least one "wild" idea per prompt — those often become the
         seed of a distinct concept in §5.
       - Feature = a noun phrase (what it is). Detail = one sentence (how
         it would satisfy the prompt). Keep both short.
       - Number features continuously F-001 to F-100 across all three
         tables so that §4 and §5 can refer to them by ID.
       - Fill this table AS CAPTURED during the session. Do not reorder or
         prune here — sorting happens in §4.

     Two example rows per table are filled in below as a model of the
     expected level of detail. Keep them only if the team agrees they
     belong in the brainstorm. -->

### 3.1 Sensing, Measurement and Safety (Zice)

<!-- OWNER: Zice. Prompts: SF-01, SF-04, SF-02, SW-06, SW-04, MF-03, MF-02
     -> 7 prompts x 5 = 35 rows, F-001 to F-035.
     If the table gets long, split it into one small table per prompt. -->

| ID | Req ID | Feature | Detail |
|---|---|---|---|
| F-001 | SW-06 | Bar load cell + instrumentation amplifier | A strain-gauge bridge in the handle is amplified by an INA125 and filtered before the ADC, giving a continuous force reading |
| F-002 | SW-06 | Force-sensitive resistor pads | Thin FSR pads under each finger report force per finger instead of one total, at lower cost and lower accuracy |
| F-003 | | | |

### 3.2 Actuation, Mechanics and Data (Gabriel)

<!-- OWNER: Gabriel. Prompts: SW-01, HW-01, HW-05, HW-03, MF-05, SW-03,
     SW-05 -> 7 prompts x 5 = 35 rows, F-036 to F-070. -->

| ID | Req ID | Feature | Detail |
|---|---|---|---|
| F-036 | SW-01 | Motor-driven spring preload | A gear motor turns a lead screw that compresses the return spring, so resistance changes with spring preload |
| F-037 | SW-01 | Magnetorheological brake | A fluid brake whose resistance changes with coil current, giving smooth resistance with no moving preload mechanism |
| F-038 | | | |

### 3.3 Interaction, Feedback and Prescription (Duotao)

<!-- OWNER: Duotao. Prompts: CU-01, CU-03, UX-01, UX-03, UX-04, UX-05
     -> 6 prompts x 5 = 30 rows, F-071 to F-100. -->

| ID | Req ID | Feature | Detail |
|---|---|---|---|
| F-071 | UX-01 | Single start button | One large button resumes the last prescribed session, so a home patient starts in one press |
| F-072 | UX-01 | Patient ID card tap | Tapping an NFC card loads that patient's profile and prescription with no menu navigation |
| F-073 | | | |

## 4. Sorting, Ranking and Refinement

<!-- WHAT: Step 3 of the assignment. Three things must be visible to the
     grader: the features are GROUPED, the features are RANKED (top ones
     clearly indicated in each group), and NEW features came out of the
     discussion. Plus snapshots proving the stages happened.

     Before the tables, write 2-3 sentences: what grouping axis the team
     chose and why (theme / function / user need / subsystem). -->

### 4.1 Feature Groups

<!-- OWNER: Duotao
     HOW:
       - Group by FUNCTION, not by who wrote the feature. If the groups
         end up identical to §3.1/3.2/3.3, the grouping step added nothing
         and a reviewer will notice. Features from different owners should
         mix inside a group.
       - 6-10 groups is a workable number for ~100 features.
       - Mark the top-ranked feature(s) of each group in bold in the last
         column (results come from §4.2).

     Group names below are examples only. -->

**Table 2. Feature groups and the top-ranked features in each.**

| Group | Theme | Feature IDs | Top feature(s) |
|---|---|---|---|
| G1 | Force sensing front end | F-001, F-002, … | **F-001** |
| G2 | Resistance mechanism | F-036, F-037, … | **F-036** |
| G3 | | | |

### 4.2 Ranking Method and Results

<!-- OWNER: Gabriel
     HOW: The assignment only says "rank and indicate the top ideas", so
     the method is the team's choice — but it must be stated and applied
     consistently. A simple, defensible method:
       Score = W x (Fit + Feasibility + Cost), each criterion 1-5
         W           = requirement weight from Table 1
         Fit         = how well the feature satisfies its prompt
         Feasibility = can our team build it this semester with the
                       course toolchain (KiCad, PIC, one PCB each)?
         Cost        = 5 = cheap, 1 = expensive
       Each member scores independently, use the mean (same approach as
       the User Needs rating, which keeps the pages consistent).
     Alternative: dot voting (each member gets N votes). Faster, but
     weaker to defend at the external review.

     Do NOT put all 100 scores in the main body. Show the method, then only
     the top features per group here; put the full sheet as an image or
     table in docs/Appendix/ and embed it there (not a link to a Sheet). -->

**Table 3. Highest-scoring features (full scoring sheet in the Appendix).**

| Rank | ID | Feature | Score |
|---|---|---|---|
| 1 | F-036 | Motor-driven spring preload | — |
| 2 | F-001 | Bar load cell + instrumentation amplifier | — |
| 3 | | | |

### 4.3 New Features from Discussion

<!-- OWNER: Everyone; Zice records.
     WHAT: The assignment explicitly asks you to "generate new features from
     the ideas that came out of your discussion". These are usually
     COMBINATIONS of existing features — cite the IDs they came from.
     Aim for 5-10.

     EXAMPLES (the combination logic is the point, not the exact wording): -->

| ID | New feature | Built from | Why it is better |
|---|---|---|---|
| F-N01 | One force signal, three jobs | F-001 + a rep-count idea + an overforce idea | The same load-cell reading drives the display, the repetition counter and the overforce cutoff, so no extra sensor is needed |
| F-N02 | Card-locked prescription | F-072 + a resistance-limit idea | The patient's card carries the authorized maximum, so a home patient cannot select a level the therapist did not allow |
| F-N03 | | | |

### 4.4 Brainstorm Snapshots

<!-- OWNER: Duotao (session scribe)
     WHAT: The checklist grades "snapshots of the brainstorm from different
     stages of organization". Three images minimum, taken at the three
     "capture and save" points in the assignment. They must show the
     board genuinely changing between stages.
     HOW: export each stage from the board tool as PNG at readable
     resolution; save to docs/image/ideation/ with no spaces in the name;
     embed with a numbered caption. If text is too small to read in the
     PDF, add a cropped close-up rather than shrinking further.

     Format to follow (these two lines are the pattern; uncomment and
     replace the file names once the images exist):

     ![Raw brainstorm board with all features before sorting](image/ideation/stage1-raw.png)
     **Figure 1. Stage 1 — all features as first captured, before sorting.**

     ![Features arranged into thematic groups with top features highlighted](image/ideation/stage2-grouped.png)
     **Figure 2. Stage 2 — features sorted into groups and ranked.**
-->

## 5. Product Concepts

<!-- WHAT: Step 4. Three concepts, each a DIFFERENT recombination of the
     features — "alternative visions" for the client. Each concept needs:
       (a) a name and a one-sentence pitch
       (b) the features it uses, by ID, with the requirement each satisfies
       (c) ONE visually engaging representation
       (d) 1 paragraph: what it does and how its features satisfy the
           needs and requirements from earlier assignments

     ALLOWED REPRESENTATIONS (pick one per concept; the three concepts may
     use different formats):
       - Photo of a physical mockup (cardboard / 3D print), annotated in a
         vector tool with text boxes + arrows
       - Computer-generated VECTOR sketch or CAD render, annotated with
         text boxes + arrows. CAD must NOT be just a dimensioned drawing.
       - Vector storyboard / comic with at least one human character
       - Narrated stop-motion video < 5 min, or a mock advertisement
     NOT ALLOWED: hand-drawn sketches. Anything else needs instructor
     approval first.
     Every feature listed in (b) must be visibly labeled with an arrow in
     (c) — the checklist grades exactly this.

     MAKING THE THREE DISTINCT: give each concept a different "center of
     gravity" (e.g. clinic accuracy / home simplicity / motivation and
     adaptivity). A feature may appear in more than one concept, but if
     two concepts share most of their features, merge them and make a
     new third one.

     Suggested tools: Inkscape, Figma, Affinity Designer, PowerPoint
     shapes exported as SVG, Onshape/Fusion render + vector labels. -->

### 5.1 Concept A — {name} (Zice)

<!-- OWNER: Zice
     EXAMPLE direction: "Clinic Precision" — accuracy-first unit that
     doubles as a dynamometer. Replace name and pitch with the team's. -->

**Pitch:** {one sentence}

| ID | Feature | Satisfies |
|---|---|---|
| F-001 | Bar load cell + instrumentation amplifier | SW-06, SW-04 |
| F-036 | Motor-driven spring preload | SW-01, CU-01 |
| | | |

<!-- ![Concept A annotated sketch](image/ideation/concept-a.svg)
     **Figure 4. Concept A — {name}, with each selected feature labeled.** -->

{1 paragraph: what the concept does and how its features satisfy the needs and requirements.}

### 5.2 Concept B — {name} (Gabriel)

<!-- OWNER: Gabriel
     EXAMPLE direction: "Home Companion" — lightest, simplest unit for
     unsupervised home use. -->

**Pitch:** {one sentence}

| ID | Feature | Satisfies |
|---|---|---|
| F-071 | Single start button | UX-01 |
| F-037 | Magnetorheological brake | SW-01, SF-02 |
| | | |

<!-- ![Concept B annotated sketch](image/ideation/concept-b.svg)
     **Figure 5. Concept B — {name}, with each selected feature labeled.** -->

{1 paragraph.}

### 5.3 Concept C — {name} (Duotao)

<!-- OWNER: Duotao
     EXAMPLE direction: "Adaptive Coach" — motivation and automatic
     progression; a storyboard with a patient character suits this one. -->

**Pitch:** {one sentence}

| ID | Feature | Satisfies |
|---|---|---|
| F-072 | Patient ID card tap | UX-01, CU-01 |
| F-N02 | Card-locked prescription | CU-01, SF-01 |
| | | |

<!-- ![Concept C storyboard](image/ideation/concept-c.svg)
     **Figure 6. Concept C — {name}, storyboard of a home session.** -->

{1 paragraph.}

### 5.4 Concept Comparison

<!-- OWNER: Everyone (fill after all three concepts exist)
     WHAT: Not strictly required, but it is the fastest way to show the
     reviewer the three concepts really are "alternative visions", and the
     team will need this comparison for the next assignment anyway.
     HOW: 5-7 rows, each a top-weighted need category or key requirement.
     Short words only (Strong / Partial / Weak, or a 1-5 score). -->

| Criterion | Concept A | Concept B | Concept C |
|---|---|---|---|
| Resistance accuracy (SW-01) | Strong | Partial | Partial |
| Home usability (UX-01) | Partial | Strong | Strong |
| | | | |

<!-- The ratings in the two rows above are placeholders that illustrate the
     format; set them once the concepts are finalized. -->

## 6. Ideation Process

<!-- OWNER: Zice drafts, Gabriel and Duotao review.
     WHAT: Step 5 — ONE page (single-spaced 12 pt ≈ 500-600 words). Must
     answer every question below; a reviewer will check them one by one:
       [ ] How the brainstorm session was run (format, length, rules)
       [ ] Who participated
       [ ] How and when you met (in person / Zoom / async)
       [ ] How ideas were collected — which tools, WHO recorded them
       [ ] Which earlier assignments the requirements came from
           (User Needs & Benchmarking, Product Requirements)
       [ ] What other resources were used to generate ideas (the linked
           brainstorming articles, benchmark products, patents, ...)
       [ ] How features were grouped
       [ ] How rankings were applied to the top ideas
     HOW: prose paragraphs, no bullet lists; write only what actually
     happened, with specific numbers (minutes, feature counts before and
     after, number of groups). Take notes DURING the session so this can
     be written accurately.

     EXAMPLE sentence 1 (process):
       "Each member first generated roughly fifteen features alone for the
        prompts assigned in Table 1, after which the team met for a
        {length} session on {tool} to pool and extend them."
     EXAMPLE sentence 2 (grouping/ranking):
       "Features were regrouped by function rather than by author, which
        produced {n} groups; within each group every member scored the
        features on fit, feasibility and cost, and the mean score weighted
        by requirement importance determined the ranking." -->

{Approximately one page.}

---

## AI Use Disclosure

<!-- REQUIRED for EGR 304: full query disclosure on every submission.
     Update the description and the query list before export if more
     queries are made on this page (by anyone on the team). -->

Generative AI tools, including Claude, were used by Zice Sun to interpret the assignment requirements, propose the page structure, the prioritization method and the division of work, and provide example entries illustrating the expected format. {Describe any further use.} All brainstormed features, rankings, concept designs and the process description reflect the team's own session and were reviewed by the team before submission.

Full query text (translated from Chinese where applicable):

1. EGR 304 team assignment: build a complete skeleton file, write clearly in English comments what each section should do and how to do it, fill 2 examples in each section, and divide the work among Zice Sun (me), Duotao Gao and Gabriel. [team repository link; assignment link]
