# Product Requirements

<!-- ============================================================
     HOW TO WORK ON THIS PAGE
     (HTML comments do not appear on the published page.
     No need to delete them when you are done.)

     OWNERSHIP
       Zice      — §1 Objective & Stakeholders, §3.6 Safety,
                   §4 table format + traceability IDs,
                   site build / PDF export / Canvas submission
       Duotao  — §2 Use Cases, §3.3 Interactivity & UX, §3.4 Customization
       Gabriel  — §3.1 Hardware, §3.2 Software, §3.5 Manufacturing
       Everyone  — §5 Open Questions; review §4 together

     THREE HARD RULES
       1. Every requirement must trace back to one item from the
          User Needs assignment (fill the Source column).
       2. Every requirement must have a verifiable specification in §4.
          No spec = the requirement is not finished.
       3. Keep table columns few and cell text short. Put long
          explanations in body text. Wide tables break across pages
          in the PDF export — this is one of the listed common mistakes.

     BEFORE EXTERNAL DESIGN REVIEW — CONFIRM THESE NUMBERS
       Every target value in §4 is a proposed engineering target. Each one
       must be checked against the actual mechanism (spring rate, lead-screw
       pitch, motor torque, load-cell range) and adjusted if infeasible.
       A target the built prototype cannot meet is worse than a
       conservative one.

     PRE-SUBMISSION CHECKLIST
       [ ] §1 objective written, stakeholder table complete
       [ ] §2 at least two Use Cases, both using the same contrast axis
       [ ] §3 all six aspects have >= 3 requirements, roughly balanced
       [ ] §4 every row has target + unit + tolerance + method + procedure
       [ ] §4 contains no adjective-only criteria
           (comfortable / lightweight / sturdy / fast)
       [ ] §5 Open Questions is not empty
       [ ] Browser print preview checked — no table cut across pages
       [ ] AI Use Disclosure updated with all queries used
     ============================================================ -->

## 1. Project Objective and Stakeholders

### 1.1 Project Objective

<!-- 2-4 sentences. Answer: for whom, what problem it solves, what the
     product is, and what success looks like. Do not describe the
     implementation here — objective only. -->

The objective of this project is a prescription-based automatic resistance grip trainer for hand rehabilitation. The device measures the force a patient actually applies through a load cell and a custom analog front end, and automatically sets its own mechanical resistance to a level prescribed by a clinician. Success means a clinician can define a progression plan once and have it carried out correctly across both clinic and home sessions, without manual reconfiguration of the device and without losing the record of what the patient actually did.

### 1.2 Stakeholders

<!-- Beyond the direct user, think about who else imposes design
     constraints: whoever pays, prescribes, maintains, approves,
     or disposes of the product.
     If §2 uses the "two stakeholders" axis, pick two rows from here. -->

| Stakeholder | Role | What they need from the product | How they interact with it |
|---|---|---|---|
| Physical / occupational therapist | Primary user | Prescribe resistance and progression; verify what the patient actually performed | Sets prescription, reviews session records, supervises clinic sessions |
| Patient in rehabilitation | Secondary user | Perform prescribed exercise correctly and without pain, between clinic visits | Runs daily sessions unsupervised at home |
| Family caregiver | Support user | Help set up and position the device for a patient with limited hand function | Assists with power-on, grip span, profile selection |
| Clinic administrator | Purchaser | Justify unit cost; share one device across multiple patients safely | Approves purchase, manages cleaning and profile assignment |
| External industrial designer | Contracted supplier | A complete set of dimensional, ergonomic and material constraints to design against | Receives the §3.1 requirements as a design brief |

---

## 2. Use Cases

<!-- At least two. Pick ONE contrast axis and keep it consistent:
       (a) two different venues
       (b) two different interaction examples
       (c) two different stakeholders
     State which one you chose in the line below. -->

**Contrast axis:** two different stakeholders — a therapist in a clinic and a patient at home. This pair was chosen because the team charter names clinicians as primary users and home-exercising patients as secondary users, and because the two groups impose opposing requirements on the same interface: the therapist needs configuration authority, and the patient must be prevented from exercising it.

### 2.1 Use Case 1 — Therapist sets a progression at a clinic follow-up

| Field | Content |
|---|---|
| Actor | Therapist |
| Venue / Context | Clinic Treatment room |
| Precondition | The patient's file has been established, the equipment has been turned on and calibrated |
| Trigger | The patient came for treatment at the appointed time  |
| Success criteria | The resistance level and the number of target repetitions are saved to the correct patient profile |

**Main flow**

1.The therapist turns on the device and selects the patient's profile. 
2.The patient undergoes a brief grip strength test. 
3.The device displays the patient's grip strength in real time. 
4.The therapist sets the resistance level and the target number of repetitions. 
5.The patient completed a set of supervised training using the new Settings. 
6.The therapist confirms and saves the training plan.

**What could go wrong**

<!-- Failure mode + how the product should respond. Items written here
     usually become §3.6 safety requirements. -->

- If the patient feels pain, the therapist stops the training and the equipment removes the resistance. 
- If the wrong patient file is selected, the device will ask the therapist to confirm the patient's information before saving it. 
- If the grip strength reading is abnormal, the device will issue a warning and require recalibration.

### 2.2 Use Case 2 — Patient completes a prescribed session at home

| Field | Content |
|---|---|
| Actor | Patient |
| Venue / Context | A patient's home where no therapist is present |
| Precondition | The patient files and training plans have been loaded |
| Trigger | The patient began the scheduled training |
| Success criteria | When the patient completes the target number of repetitions, the device saves the training results  |

**Main flow**

1. The patient turns on the device and selects their own file. 
2. The device loads the training plan set by the therapist. 
3. The device displays the resistance level and the number of target repetitions. 
4. The patient begin training, and the device displays the grip strength and records the number of repetitions. 
5. After achieving the goal, the device reminds the patient. 
6. The device saves the results of this training.
**What could go wrong**

- If the patient feels pain, the patient stops the training and the equipment removes the resistance. 
- If the patient attempts to exceed the resistance limit, the device prevents this change. 
- If the power is cut off during the training process, the equipment releases the resistance and saves the number of repetitions that have been completed

<!-- Optional, recommended: add a mermaid flowchart — already enabled
     on this site. Example syntax:

```mermaid
flowchart LR
    A[Step] -> B{Decision}
    B ->|Yes| C[Outcome]
    B ->|No| D[Outcome]
-->

---

## 3. Requirements by Design Aspect

<!-- All six aspects are required. At least 3 requirements each, roughly
     balanced in count across aspects.
     Source column: the User Needs item this came from. This column is the
     traceability the assignment asks for — the QFD / decision matrix tools
     it points to exist to support it.
     Priority: Must / Should / Could.
     State WHAT is needed here. "How much counts as met" belongs in §4. -->

Requirements are traced to the categorised needs in the team's User Needs and Benchmarking report. **`UN c.n` denotes category `c`, need `n`** in that report — for example, `UN 2.4` is "The device provides resistance that matches the indicated setting."

The identifiers used throughout this page are as follows.

| Prefix | Stands for | Where it is defined |
|---|---|---|
| `UN c.n` | **U**ser **N**eed, category `c`, item `n` | User Needs and Benchmarking report, section 5 |
| `HW` | **H**ard**w**are / Product Design requirement | §3.1, specified in §4.1 |
| `SW` | **S**oft**w**are / Functionality requirement | §3.2, specified in §4.2 |
| `UX` | User e**X**perience and Interactivity requirement | §3.3, specified in §4.3 |
| `CU` | **Cu**stomization requirement | §3.4, specified in §4.4 |
| `MF` | **M**anu**f**acturing requirement | §3.5, specified in §4.5 |
| `SF` | **S**a**f**ety requirement | §3.6, specified in §4.6 |
| `Q` | Open **Q**uestion | §5 |

### 3.1 Hardware / Product Design

<!-- Note: the product (industrial) design will be outsourced to an
     external designer. So this section states the CONSTRAINTS GIVEN TO
     THAT DESIGNER, not your own styling decisions — dimensional envelope,
     hand contact surfaces, mounting hole locations, material limits,
     volume taken by the PCBs, thermal and routing clearance,
     ingress protection. -->

The enclosure and external form of the product will be designed by an external industrial designer. This section therefore states the constraints that design must satisfy; it does not specify styling.

| ID | Requirement | Source | Priority |
|---|---|---|---|
| HW-01 | The grip span shall be adjustable to accommodate different adult hand sizes | UN 4.7, UN 4.8 | Must |
| HW-02 | The device shall be usable with either hand, with the display readable in both orientations | UN 4.5, UN 4.6 | Must |
| HW-03 | The device shall be carried in one hand and used without permanent installation | UN 7.1, UN 7.2 | Must |
| HW-04 | Hand-contact surfaces shall provide a secure, non-slip grip during repeated exercise and withstand routine cleaning without visible damage | UN 1.7, UN 6.5 | Must |
| HW-05 | Moving components, including the motor and lead-screw mechanisms, will be enclosed to prevent the user's fingers from contacting pinch, crushing or entanglement hazards during normal operation | UN 1.15, UN 1.2 | Must |

### 3.2 Software / Functionality

| ID | Requirement | Source | Priority |
|---|---|---|---|
| SW-01 | The device shall close a control loop from measured grip force to motor-driven resistance, holding the prescribed setpoint | UN 2.4, UN 2.11 | Must |
| SW-02 | The device shall enforce the clinician-authorised maximum resistance and reject any request above it | UN 2.13, UN 2.12 | Must |
| SW-03 | The device shall store every repetition with timestamp, peak force and session identifier in non-volatile memory without overwriting earlier records | UN 3.5, UN 3.8, UN 3.13 | Must |
| SW-04 | The device shall detect completed repetitions automatically, without manual entry | UN 3.5, UN 3.11, UN 3.15 | Must |
| SW-05 | Stored records shall remain retrievable after power loss and shall be exportable for clinician review | UN 3.18, UN 6.12 | Should |

### 3.3 Interactivity & User Experience

| ID | Requirement | Source | Priority |
|---|---|---|---|
| UX-01 | A patient shall be able to start their prescribed session in a small fixed number of actions | UN 4.1, UN 3.11 | Must |
| UX-02 | Repetition and end-of-set feedback shall be perceivable without looking at the device | UN 5.15, UN 5.16 | Must |
| UX-03 | The display shall show current resistance, repetitions completed and target throughout a session | UN 4.6, UN 3.16 | Must |
| UX-04 | All controls shall be operable by a user with limited grip strength and limited dexterity | UN 4.11, UN 1.1 | Must |
| UX-05 | A first-time user shall complete a session using on-device prompts alone, with no prior training | UN 4.2, UN 4.3 | Should |

### 3.4 Customization

<!-- What is configurable, who is allowed to configure it, the range and
     granularity of each setting, and whether settings must persist. -->

| ID | Requirement | Source | Priority |
|---|---|---|---|
| CU-01 | A clinician shall be able to set the prescribed resistance, target repetitions, sessions per day and progression step | UN 2.12, UN 2.15 | Must |
| CU-02 | A stored prescription shall survive power loss and firmware update without alteration | UN 6.12, UN 6.11 | Must |
| CU-03 | The grip span setting shall be stored per user and restored on profile selection | UN 4.8, UN 4.14 | Should |
| CU-04 | A patient shall be able to select only among resistance levels the clinician has authorised | UN 2.13, UN 2.1 | Must |
| CU-05 | The device shall hold multiple independent user profiles so one unit can serve several patients | UN 3.8, UN 7.3 | Should |

### 3.5 Manufacturing

<!-- Volume assumptions, number of assembly steps, need for custom
     fixtures, testability, component sourcing risk (single source or
     long lead time), whether calibration requires manual labor. -->

| ID | Requirement | Source | Priority |
|---|---|---|---|
| MF-01 | The electronics shall be partitioned into three boards that can each be powered and tested independently | UN 6.1, UN 6.9 | Must |
| MF-02 | Each analog stage and each motor-driver input shall be accessible at a test point for production test | UN 3.12, UN 6.9 | Must |
| MF-03 | Force calibration shall be performed at end of line with known masses and no custom fixture | UN 3.1, UN 3.3 | Must |
| MF-04 | Every critical component shall have an identified second source or documented alternate | UN 6.14, UN 6.15 | Should |
| MF-05 | The bill of materials shall stay low enough for the unit to be affordable to an individual patient | UN 7.3 | Should |

### 3.6 Safety

<!-- The assignment encourages citing safety regulations you find. For each
     citation, give the standard number and its scope, and say which part of
     this product it applies to.
     Every "What could go wrong" item in §2 should have a matching
     requirement here.

     The regulatory pathway is NOT yet settled — see Q-01 in §5.
     Do not state an FDA device class on this page until it is verified. -->

| ID | Requirement | Source / Standard | Priority |
|---|---|---|---|
| SF-01 | Applied resistance shall never exceed the authorised maximum, and an overforce condition shall be released automatically | UN 1.6, UN 2.13 | Must |
| SF-02 | The patient shall be able to release the resistance by hand, without tools and without power | UN 1.2, UN 1.1 | Must |
| SF-03 | A mechanical failure shall not release stored spring energy or fragments toward the user | UN 1.2, UN 1.15 | Must |
| SF-04 | Skin-contact materials shall be biologically evaluated and shall withstand clinical cleaning between patients | UN 1.9, UN 6.5; ISO 10993-1 | Must |
| SF-05 | Hazards shall be identified and mitigated under a documented risk management process | ISO 14971; IEC 60601-1; IEC 62366-1 | Must |

---

## 4. Requirement Criteria Specifications

<!-- One row per requirement in §3, matched by Req ID.

     The Specification column must be: metric + target value + unit +
     tolerance. Adjectives are never acceptable. If you cannot write a
     number, the requirement is not yet thought through.

     Verification — pick one:
       Inspection     confirmable by looking (label, material,
                      dimension, connector type)
       Analysis       calculated (power budget, error stack-up, loading)
       Test           measured with instruments (accuracy, bandwidth,
                      response time, endurance)
       Demonstration  show the function running (self-test, alarm
                      trigger, power-loss behavior)

     Procedure: one sentence — what equipment, how many points measured,
     and the pass/fail condition. If you cannot write a procedure, the
     verification method is probably the wrong choice.

     This section is split into six small tables, one per aspect, so that
     no single table runs long enough to break across pages in the PDF. -->

Each requirement above is specified below with a measurable criterion and the method by which it will be verified: **inspection**, **analysis**, **test**, or **demonstration**.

### 4.1 Hardware / Product Design

| ID | Specification | Verification | Procedure |
|---|---|---|---|
| HW-01 | Grip span adjustable over 35–87 mm, ±1 mm at any setting | Test | Measure span with calipers at minimum, middle and maximum settings |
| HW-02 | Display information shall be readable and all controls accessible during both left-handed and right-handed use | Demonstration | Have users operate the device with each hand and verify that all the displayed information can be read and all the controls can be accessed |
| HW-03 | Total mass ≤ 0.75 kg including power source; no fixed mounting required | Test | Weigh the complete unit on a scale accurate to ±5 g; operate on an unsecured table |
| HW-04 | Hand displacement ≤ 5mm during 20 consecutive repetitions at the maximum prescribed resistance, no visible cracking, peeling, or permanent deformation after 100 cleaning cycles with 70% isopropyl alcohol | Test | Mark the initial hand position and measure displacement after 20 repetitions, then perform 100 cleaning cycles with 70% IPA and visually inspect the hand-contact surfaces |
| HW-05 | No user-accessible contact with the motor, lead screw, gears, or other hazardous moving components during normal operation | Inspection / Test | Operate the device through its full range of motion and inspect all accessible openings to verify that fingers cannot contact hazardous moving components |

### 4.2 Software / Functionality

| ID | Specification | Verification | Procedure |
|---|---|---|---|
| SW-01 | Control loop executes at ≥ 50 Hz; steady-state resistance within 5 % of setpoint; settling within 2.0 s of a commanded change | Test | Command step changes across the full range; log setpoint and measured force |
| SW-02 | Requests above the authorised maximum rejected in 20 of 20 trials | Demonstration | Attempt to set resistance above the authorised level from the patient interface |
| SW-03 | ≥ 500 sessions retained; zero records lost across 20 power-cycle events | Test | Fill storage, power-cycle, export and compare record counts |
| SW-04 | Automatic repetition count agrees with manual count to ≥ 98 % over 200 repetitions, with no double counts | Test | Two observers count manually while the device logs |
| SW-05 | 30 days of records exportable in a documented text format within 60 s | Demonstration | Export from a populated device and open the file on a host PC |

### 4.3 Interactivity & User Experience

| ID | Specification | Verification | Procedure |
|---|---|---|---|
| UX-01 | Session starts within 3 user actions from power-on | Demonstration | Count actions from power-on to first logged repetition |
| UX-02 | Repetition confirmation within 300 ms of detection, at ≥ 65 dBA measured 0.5 m from the device | Test | Sound level meter at 0.5 m; timing captured on a logic analyser |
| UX-03 | Character height ≥ 4 mm; text contrast ratio ≥ 4.5:1 | Inspection | Measure characters and compute contrast from measured luminance |
| UX-04 | Every control actuates with ≤ 5 N applied force and ≤ 10 mm travel | Test | Force gauge on each control; measure travel with calipers |
| UX-05 | 3 of 3 untrained users complete a full session with no verbal assistance | Demonstration | Observed trial with participants who have not used the device before |

### 4.4 Customization

| ID | Specification | Verification | Procedure |
|---|---|---|---|
| CU-01 | Resistance settable 2.0–30.0 kgf in 0.5 kgf steps; target repetitions 1–99; sessions per day 1–10; progression step 0–5.0 kgf | Demonstration | Set each parameter to its minimum, a middle value and its maximum |
| CU-02 | Prescription retained ≥ 30 days with power removed, and unchanged after a firmware update | Test | Store prescription, remove power 30 days, re-read; repeat across an update |
| CU-03 | Grip span setting restored within 2.0 s of profile selection | Demonstration | Switch between two profiles with different spans and time the response |
| CU-04 | Patient-selectable range bounded by the authorised maximum in 20 of 20 attempts | Demonstration | Attempt out-of-range selection from the patient interface |
| CU-05 | ≥ 8 independent user profiles, each with its own prescription and records | Inspection | Create 8 profiles and confirm records do not cross between them |

### 4.5 Manufacturing

| ID | Specification | Verification | Procedure |
|---|---|---|---|
| MF-01 | Three boards with keyed inter-board connectors; each board passes a standalone power-on test | Test | Power each board alone and confirm its documented pass criteria |
| MF-02 | Test point present at bridge output, instrumentation amplifier output, filter output and each motor-driver input | Inspection | Review PCB layout against the test point list |
| MF-03 | End-of-line calibration completed in ≤ 5 min per unit using three known masses; residual error ≤ 2 % of full scale | Test | Time the procedure and verify against a fourth mass not used in calibration |
| MF-04 | 100 % of components designated critical have a second source or documented alternate | Analysis | BOM review against distributor availability |
| MF-05 | Bill of materials ≤ $120 per unit at a quantity of 100 | Analysis | Costed BOM at quantity-100 pricing |

### 4.6 Safety

| ID | Specification | Verification | Procedure |
|---|---|---|---|
| SF-01 | Measured force never exceeds the authorised maximum by more than 10 %; on exceedance, resistance reduced to minimum within 500 ms | Test | Drive the mechanism past the limit deliberately and log the response time |
| SF-02 | Manual release operable one-handed with ≤ 10 N in ≤ 2.0 s, with power removed | Demonstration | Remove power at maximum resistance and release using the other hand only |
| SF-03 | After 30 000 cycles at maximum resistance, the spring remains captive and no fragment escapes the enclosure | Test | Cycle test on a fixture, then inspect and disassemble |
| SF-04 | Skin-contact materials evaluated for cytotoxicity, irritation and sensitisation per ISO 10993-1; no cracking or discolouration after 100 cleaning cycles | Analysis, Inspection | Material data review against ISO 10993-1; visual inspection after cleaning cycles |
| SF-05 | Risk file documents every identified hazard with a mitigation and a residual risk rating, reviewed and signed by the team | Inspection | Review the risk file against the ISO 14971 clause structure |

---

## 5. Open Questions

<!-- Writing this section honestly earns credit — it shows the team knows
     what it does not yet know. For each item: what is blocked, who will
     find the answer, and when the answer is needed. -->

| ID | Question | Owner | Needed by | Blocking |
|---|---|---|---|---|
| Q-01 | Which FDA classification applies to a prescription powered hand exerciser, and does 21 CFR 890.5380 cover this device? | Zice | Before external design review | SF-05, labelling, any regulatory claim on this page |
| Q-02 | Is the lead screw back-drivable at maximum spring preload? If not, a mechanical release must be designed in. | Member B | Before the enclosure brief is sent out | SF-02, HW-05, external design brief |
| Q-03 | Which reference dynamometer will serve as the accuracy standard, and is one available on campus? | Member A | Before the calibration procedure is written | MF-03, SW-01, UN 3.2 traceability |
| Q-04 | Does the clinician configure the device on-device, or through a host PC over the serial link? | Team | Before the software architecture is frozen | CU-01, SW-05, software board scope |
| Q-05 | Is the home unit battery powered or mains powered? | Member B | Before power board layout | HW-03 mass target, power board design |

---

## Appendix — Requirement Derivation

<!-- Optional but recommended: a decision matrix or QFD table supporting the
     Source column in §3. The assignment specifically calls attention to
     these two tools — having one beats having none.
     Large tables can live in docs/Appendix/ and be linked from here so
     this page stays a reasonable length. -->

The seven need categories in the User Needs and Benchmarking report were rated for importance by all three team members. Those mean ratings are used as weights when requirements compete for the same resource — enclosure volume, board area, unit cost, or development time.

| Need category | Mean importance | Design aspects it drives |
|---|---|---|
| Resistance and Progression | 4.33 | Software, Customization, Safety |
| Usability, Fit, and Accessibility | 4.14 | Hardware, Interactivity & UX |
| Reliability and Support | 4.09 | Manufacturing, Safety |
| Safety and Comfort | 4.07 | Safety, Hardware |
| Therapeutic Capability | 4.00 | Software, Customization |
| Portability and Access | 3.83 | Hardware, Manufacturing |
| Measurement and Data | 3.74 | Software, Manufacturing |

---

## AI Use Disclosure

Generative AI tools, including Claude, were used by Zice Sun to interpret the assignment requirements, establish the page structure and traceability scheme, and draft candidate requirement and specification wording. All target values, verification methods and open questions were reviewed by the team and adjusted against the actual design before submission.

Full query text (translated from Chinese where applicable):

1. I am starting the EGR 304 team assignment. Lay out all the requirements, how to approach it, and the division of work. If useful, produce a skeleton file that my teammates and I can fill in directly. [assignment link; team repository link]
2. The skeleton should be in English.
3. Based on our previous assignment, fill in 1-2 entries for each section for reference.
4. Add the per-section instruction comments back into the filled English version.
5. Also spell out what the abbreviations UN, UX, CU and the rest stand for.

<!-- Add any further queries here before submitting. -->
