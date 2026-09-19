# Product Requirements

<!-- ============================================================
     HOW TO WORK ON THIS PAGE
     (HTML comments do not appear on the published page.
     No need to delete them when you are done.)

     OWNERSHIP
       Zice     — §1 Objective & Stakeholders, §3.6 Safety,
                  §4 table format + traceability IDs,
                  site build / PDF export / Canvas submission
       Duotao   — §2 Use Cases, §3.3 Interactivity & UX, §3.4 Customization
       Gabriel  — §3.1 Hardware, §3.2 Software, §3.5 Manufacturing
       Everyone — §5 Open Questions; review §4 together

     THREE HARD RULES
       1. Every requirement must trace back to one item from the
          User Needs assignment (fill the Source column).
       2. Every requirement must have a verifiable specification in §4.
          No spec = the requirement is not finished.
       3. Keep table columns few and cell text short. Put long
          explanations in body text. Wide tables break across pages
          in the PDF export — this is one of the listed common mistakes.
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

**Contrast axis:** Two different stakeholders — a therapist and a patient. We chose these two because they use the device in different ways. The therapist sets the resistance level and the target number of repetitions. Patients follow the designated training plan and must not choose resistance levels that exceed the limits set by the therapist.

### 2.1 Use Case 1 — Therapist sets a progression at a clinic follow-up

| Field | Content |
|---|---|
| Actor | Therapist |
| Venue / Context | Clinic treatment room |
| Precondition | The patient's profile has been established; the device has been turned on and calibrated |
| Trigger | The patient arrives for treatment at the appointed time |
| Success criteria | The resistance level and the target number of repetitions are saved to the correct patient profile |

**Main flow**

1. The therapist turns on the device and selects the patient's profile.
2. The patient undergoes a brief grip strength test.
3. The device displays the patient's grip strength in real time.
4. The therapist sets the resistance level and the target number of repetitions.
5. The patient completes a set of supervised training using the new settings.
6. The therapist confirms and saves the training plan.

**What could go wrong**

<!-- Failure mode + how the product should respond. Items written here
     usually become §3.6 safety requirements. -->

- If the patient feels pain, the therapist stops the training and the device removes the resistance.
- If the wrong patient profile is selected, the device asks the therapist to confirm the patient's information before saving.
- If the grip strength reading is abnormal, the device issues a warning and requires recalibration.

### 2.2 Use Case 2 — Patient completes a prescribed session at home

| Field | Content |
|---|---|
| Actor | Patient |
| Venue / Context | A patient's home, where no therapist is present |
| Precondition | The patient profile and training plan have been loaded |
| Trigger | The patient begins the scheduled training |
| Success criteria | When the patient completes the target number of repetitions, the device saves the training results |

**Main flow**

1. The patient turns on the device and selects their own profile.
2. The device loads the training plan set by the therapist.
3. The device displays the resistance level and the target number of repetitions.
4. The patient begins training, and the device displays the grip force and records the number of repetitions.
5. After the target is reached, the device notifies the patient.
6. The device saves the results of this training session.

**What could go wrong**

- If the patient feels pain, the patient stops the training and the device removes the resistance.
- If the patient attempts to exceed the resistance limit, the device prevents the change.
- If power is lost during training, the device releases the resistance and preserves the repetitions completed so far.

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
| HW-01 | The grip span shall be adjustable to accommodate adult hand sizes across the 5th to 95th percentile range | UN 4.7, UN 4.8 | Must |
| HW-02 | The device shall be usable with either hand, with the display readable in both orientations | UN 4.5, UN 4.6 | Must |
| HW-03 | The device shall be carried in one hand and used without permanent installation | UN 7.1, UN 7.2 | Must |
| HW-04 | Hand-contact surfaces shall provide a secure, non-slip grip during repeated exercise and withstand routine cleaning without visible damage | UN 1.7, UN 6.5 | Must |
| HW-05 | Moving components, including the motor and lead-screw mechanisms, shall be enclosed to prevent the user's fingers from contacting pinch, crushing or entanglement hazards during normal operation | UN 1.15, UN 1.2 | Must |

### 3.2 Software / Functionality

| ID | Requirement | Source | Priority |
|---|---|---|---|
| SW-01 | The firmware shall use measured grip force to automatically control the resistance mechanism toward the prescribed resistance setting | UN 2.4, UN 2.11 | Must |
| SW-02 | The firmware shall enforce the clinician-authorized maximum resistance and reject attempts to select a resistance above that limit | UN 2.13, UN 2.12 | Must |
| SW-03 | The firmware shall store completed-session data including repetition count, peak grip force, and session identifier in non-volatile memory | UN 3.5, UN 3.8, UN 3.13 | Must |
| SW-04 | The firmware shall automatically detect and count completed grip repetitions without requiring manual entry | UN 3.5, UN 3.11, UN 3.15 | Must |
| SW-05 | Stored training records shall be exportable for clinician review without requiring custom software | UN 3.18, UN 3.6 | Should |
| SW-06 | The device shall measure the applied grip force across its full operating range with an error small enough for results to be comparable with clinical assessment equipment | UN 3.1, UN 3.2, UN 3.4 | Must |

<!-- SW-06 covers the core sensing function (load cell + analog front end).
     It was added because UN 3.1 and UN 3.2 are among the highest-rated
     needs in the report and were previously only covered indirectly by the
     manufacturing calibration requirement MF-03, which specifies a process
     rather than an accuracy. If the team prefers, SW-06 can move to §3.1
     as a hardware requirement — but it must exist somewhere. -->

### 3.3 Interactivity & User Experience

| ID | Requirement | Source | Priority |
|---|---|---|---|
| UX-01 | A patient shall be able to start a prescribed training session in no more than three operations | UN 4.1 | Must |
| UX-02 | The device shall display the patient's grip force in real time during a training session | UN 3.4, UN 4.6 | Must |
| UX-03 | The device shall display the resistance level, the completed repetition count and the target repetition count during a training session | UN 4.6, UN 3.5 | Must |
| UX-04 | The device shall be operable by patients with limited grip strength or limited hand flexibility | UN 4.11, UN 1.1 | Must |
| UX-05 | The device should notify the patient when the target repetition count is reached | UN 3.5, UN 4.3 | Should |

### 3.4 Customization

<!-- What is configurable, who is allowed to configure it, the range and
     granularity of each setting, and whether settings must persist. -->

| ID | Requirement | Source | Priority |
|---|---|---|---|
| CU-01 | A therapist shall be able to set the resistance level and the target repetition count for each patient | UN 2.12 | Must |
| CU-02 | A patient shall be able to select only the resistance levels authorized by the therapist | UN 2.13 | Must |
| CU-03 | The device should adjust the resistance according to the patient's measured performance | UN 2.11 | Should |
| CU-04 | The grip span of the device shall be adjustable to the size of the patient's hand | UN 4.8 | Must |
| CU-05 | A therapist should be able to select progressive training settings appropriate to the patient's stage of rehabilitation | UN 2.14, UN 2.15 | Should |

### 3.5 Manufacturing

<!-- Volume assumptions, number of assembly steps, need for custom
     fixtures, testability, component sourcing risk (single source or
     long lead time), whether calibration requires manual labor. -->

| ID | Requirement | Source | Priority |
|---|---|---|---|
| MF-01 | The electronic subsystems shall be designed so that critical functions can be tested independently during assembly and troubleshooting | UN 6.8, UN 6.9 | Must |
| MF-02 | Critical sensing and motor-control signals shall be accessible for testing and troubleshooting during assembly | UN 3.12, UN 6.9 | Must |
| MF-03 | The grip-force measurement system shall support calibration using known reference loads without requiring specialized calibration equipment | UN 3.1, UN 3.3 | Must |
| MF-04 | Critical electronic and mechanical components shall be commercially available and have documented replacement options where available | UN 6.14, UN 6.15 | Should |
| MF-05 | The device should be designed to a component cost, at a stated production quantity, that supports affordability for individual patient ownership | UN 7.3 | Should |

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
     no single table runs long enough to break across pages in the PDF.

     WHEN §3 CHANGES, CHANGE §4 IN THE SAME EDIT. The two sections drifted
     apart once already and the mismatch is the first thing a reviewer
     checking traceability will find. -->

Each requirement above is specified below with a measurable criterion and the method by which it will be verified: **inspection**, **analysis**, **test**, or **demonstration**.

### 4.1 Hardware / Product Design

| ID | Specification | Verification | Procedure |
|---|---|---|---|
| HW-01 | Grip span adjustable over 35–87 mm, ±1 mm at any setting, covering the 5th to 95th percentile adult hand breadth | Test | Measure span with calipers at minimum, middle and maximum settings and compare against the anthropometric range cited in the design brief |
| HW-02 | Display information shall be readable and all controls accessible during both left-handed and right-handed use | Demonstration | Have users operate the device with each hand and verify that all displayed information can be read and all controls can be accessed |
| HW-03 | Total mass ≤ 0.75 kg including power source; no fixed mounting required | Test | Weigh the complete unit on a scale accurate to ±5 g; operate on an unsecured table |
| HW-04 | Hand displacement ≤ 5 mm during 20 consecutive repetitions at the maximum prescribed resistance; no visible cracking, peeling or permanent deformation after 100 cleaning cycles with 70 % isopropyl alcohol | Test | Mark the initial hand position and measure displacement after 20 repetitions, then perform 100 cleaning cycles with 70 % IPA and visually inspect the hand-contact surfaces |
| HW-05 | No user-accessible contact with the motor, lead screw, gears or other hazardous moving components during normal operation | Inspection / Test | Operate the device through its full range of motion and inspect all accessible openings to verify that fingers cannot contact hazardous moving components |

<!-- HW-01: cite the anthropometric data source for the 5th–95th percentile
     range (a published hand-dimension table) in the design brief, so the
     35–87 mm figures have a documented basis. -->

### 4.2 Software / Functionality

| ID | Specification | Verification | Procedure |
|---|---|---|---|
| SW-01 | Control update rate ≥ 50 Hz, steady-state resistance within 10 % of the prescribed setpoint, settling time ≤ 2.0 s | Test | Command resistance settings across the operating range, log measured force and motor response, and calculate update rate, steady-state error and settling time |
| SW-02 | Resistance commands above the clinician-authorized maximum shall be rejected in 20 of 20 test attempts | Demonstration | Set a clinician maximum and attempt 20 resistance commands above the limit; verify that none are accepted |
| SW-03 | Stored session data shall retain repetition count, peak grip force and session identifier with zero data loss after 20 power cycles | Test | Record test sessions, cycle device power 20 times, and compare all stored records with the original data |
| SW-04 | Automatic repetition-count accuracy ≥ 95 % over 100 manually verified repetitions, with no more than 5 missed or false counts | Test | Perform 100 manually counted grip repetitions and compare the manual count with the firmware-recorded count |
| SW-05 | At least 30 days of stored sessions exportable within 60 s as a plain-text or CSV file readable on a host PC without custom software | Demonstration | Export from a device holding 30 days of session records and open the file on a host PC using standard software |
| SW-06 | Grip force measured over 0–40 kgf with an error ≤ 5 % of reading when compared against a reference dynamometer at a minimum of 5 points across the range | Test | Apply 5 known loads spanning the range using the reference dynamometer identified in Q-03 and compute the error at each point |

### 4.3 Interactivity & User Experience

| ID | Specification | Verification | Procedure |
|---|---|---|---|
| UX-01 | Session starts within 3 user actions from power-on | Demonstration | Count actions from power-on to the first logged repetition |
| UX-02 | Displayed grip force updates at ≥ 5 Hz with display latency ≤ 200 ms and a displayed resolution of 0.1 kgf | Test | Apply a known step load and measure the update rate and the delay between the applied step and the displayed value |
| UX-03 | Resistance level, completed repetitions and target repetitions all visible simultaneously; character height ≥ 4 mm; text contrast ratio ≥ 4.5:1 | Inspection | Confirm all three values are on screen during a session; measure character height and compute contrast from measured luminance |
| UX-04 | Every control actuates with ≤ 5 N applied force and ≤ 10 mm travel | Test | Force gauge on each control; measure travel with calipers |
| UX-05 | End-of-target notification issued within 500 ms of the final repetition, audible at ≥ 65 dBA measured 0.5 m from the device | Test | Sound level meter at 0.5 m; compare notification timing against the logged repetition timestamp |

### 4.4 Customization

| ID | Specification | Verification | Procedure |
|---|---|---|---|
| CU-01 | Resistance settable 2.0–30.0 kgf in 0.5 kgf steps and target repetitions settable 1–99, stored against the selected patient profile and retained across a power cycle | Demonstration | Set both parameters to their minimum, a middle value and their maximum on two different profiles; power-cycle and confirm each value is restored to the correct profile |
| CU-02 | Patient-selectable resistance bounded by the clinician-authorized maximum, with out-of-range selections rejected in 20 of 20 attempts | Demonstration | Attempt 20 out-of-range selections from the patient interface and confirm none are accepted |
| CU-03 | When the measured peak force over a completed set differs from the prescribed setpoint by more than 10 %, the device applies the clinician-defined progression step at the next session and never exceeds the authorized maximum | Test | Run scripted sessions with applied forces above and below the setpoint; log the resistance applied in the following session and confirm the authorized maximum is never exceeded |
| CU-04 | Grip span setting stored per patient profile and restored within 2.0 s of profile selection | Demonstration | Switch between two profiles with different grip span settings and time the response |
| CU-05 | Progression step settable 0–5.0 kgf and session frequency settable 1–10 per day per profile; the stored plan is retained for ≥ 30 days with power removed | Test | Store a progression plan, remove power for 30 days, then re-read and compare against the stored values |

<!-- Two requirements from the earlier draft lost their §3 row when §3.4 was
     rewritten: prescription persistence, and a minimum number of user
     profiles. Persistence has been folded into the CU-01 and CU-05
     specifications above. If the team wants a stated profile capacity
     (the clinic-sharing case in §1.2), it needs its own §3.4 row — it is
     not covered anywhere at present. -->

### 4.5 Manufacturing

| ID | Specification | Verification | Procedure |
|---|---|---|---|
| MF-01 | Each critical electronic subsystem shall support independent functional verification before final assembly | Test | Power and test the sensing, control and motor-drive functions individually before final assembly and verify correct operation of each subsystem |
| MF-02 | Test access shall be provided for the load-cell signal path and motor-control signals | Inspection | Inspect the assembled electronics and verify that the load-cell signal path and motor-control signals can be measured without disassembling or damaging the circuit |
| MF-03 | Force calibration shall use at least 3 known reference loads distributed across the intended measurement range; verification error shall be ≤ 5 % of full scale | Test | Calibrate the load-cell system using at least 3 known reference loads, then apply an additional reference load not used for calibration and compare the measured force with the known force |
| MF-04 | Critical components shall be identified in the BOM with manufacturer part numbers and at least one documented replacement option for components that are not uniquely required by the design | Analysis | Review the final BOM and verify that critical components are identified and compatible replacement options are documented where available |
| MF-05 | Prototype BOM cost ≤ $150 per unit excluding development tools and reusable laboratory equipment; projected BOM cost at a quantity of 100 ≤ $100, consistent with a retail price at or below the $129 benchmark device | Analysis | Cost the complete BOM at single-unit supplier pricing and again at quantity-100 pricing, and compare the projected retail price against the benchmarked products |

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
| Q-02 | Is the lead screw back-drivable at maximum spring preload? If not, a mechanical release must be designed in. | Gabriel | Before the enclosure brief is sent out | SF-02, HW-05, external design brief |
| Q-03 | Which reference dynamometer will serve as the accuracy standard, and is one available on campus? | Duotao | Before the calibration procedure is written | SW-06, MF-03, UN 3.2 traceability |
| Q-04 | Does the clinician configure the device on-device, or through a host PC over the serial link? | Team | Before the software architecture is frozen | CU-01, SW-05, software board scope |
| Q-05 | Is the home unit battery powered or mains powered? | Gabriel | Before power board layout | HW-03 mass target, power board design |

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

Generative AI tools, including Claude, were used by Zice Sun to interpret the assignment requirements, establish the page structure and traceability scheme, draft candidate requirement and specification wording, and review the completed draft for traceability and consistency errors. All target values, verification methods and open questions were reviewed by the team and adjusted against the actual design before submission.

Full query text (translated from Chinese where applicable):

1. I am starting the EGR 304 team assignment. Lay out all the requirements, how to approach it, and the division of work. If useful, produce a skeleton file that my teammates and I can fill in directly. [assignment link; team repository link]
2. The skeleton should be in English.
3. Based on our previous assignment, fill in 1-2 sample entries for each section as reference.
4. Add the per-section instruction comments back into the filled English version.
5. Also spell out what the abbreviations UN, UX, CU and the rest stand for.
6. Final check. [uploaded the team's completed draft]
7. Rewrite §4.4 to match the new §3.4, apply the rest of the suggested corrections, and output the file.
