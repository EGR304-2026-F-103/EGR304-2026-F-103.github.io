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
     then one sentence on what this page does.-->
Our product is a hand-rehabilitation grip trainer whose resistance is set by a therapist's prescription rather than by the patient. It senses how hard the hand is squeezing and adjusts its mechanism so that each exercise is performed at the intended load. We are designing it for two groups: therapists in physical and occupational therapy, who decide the training plan and check the results, and the patients they treat, who follow that plan at home without supervision. The sections below records how the team moved from those needs to a total of about 100 ideas and then to three alternative product concepts.

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
     User Needs assignment", and say what else influenced the choice.-->
Brainstorming on every requirement with equal effort would mean 100 features over 32 prompts, so the team first decided which requirements deserved the most weights and attention. We reused the importance ratings from our User Needs and Benchmarking work: a requirement took the average rating of the need category listed in its Source column, and a requirement citing two categories took the larger of the two. Two kinds of requirements were then removed from the list. Those that describe paperwork or a process, such as keeping a risk file, offer nothing to brainstorm, and pairs whose solutions would be the same, such as the two resistance-limit requirements, were combined into one prompt. That left the 20 prompts in Table 1, and asking for five features on each gave the target of 100.

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
         prune here — sorting happens in §4. -->
Tables 2 to 4 are the raw output of the brainstorm, recorded in the order the ideas were offered. At this point the team was only collecting: nothing was judged, edited or discarded, and ideas that seemed impractical were written down with the same care as conventional ones, since an unusual idea can become the starting point of a different concept later.

### 3.1 Sensing, Measurement and Safety (Zice)

<!-- OWNER: Zice. Prompts: SF-01, SF-04, SF-02, SW-06, SW-04, MF-03, MF-02
     -> 7 prompts x 5 = 35 rows, F-001 to F-035.
     If the table gets long, split it into one small table per prompt. -->

| ID | Req ID | Feature | Detail |
|---|---|---|---|
| F-001 | SF-02 | Quick-release cam lever | Flipping a lever on the side lets the spring go slack, so the resistance drops right away |
| F-002 | SF-02 | Pull-out safety pin | Pulling a pin out of the handle disconnects the spring, so the handles open freely |
| F-003 | SF-02 | Release button | Pressing a large button separates the motor from the spring, so the handle can be opened by hand |
| F-004 | SF-02 | Return to lowest setting on power loss | If the power goes out, the mechanism moves back to its easiest setting on its own |
| F-005 | SF-02 | Snap-off handle | A firm pull pops the grip handle off the body, freeing the hand immediately |
| F-006 | SF-01 | Mechanical end stop | A physical stop inside the housing keeps the spring from being tightened past the prescribed limit |
| F-007 | SF-01 | Software resistance limit | The controller refuses any setting above the maximum the therapist entered |
| F-008 | SF-01 | Automatic back-off | If the squeeze force goes over the limit, the motor eases the resistance off on its own |
| F-009 | SF-01 | Slip clutch | A clutch slips when the load gets too high, so the extra force never reaches the hand |
| F-010 | SF-01 | Therapist-only unlock | Raising the maximum needs the therapist's code, so the patient can only choose lower settings |
| F-011 | SF-04 | Removable grip sleeves | Soft sleeves slide off the handles so they can be washed or replaced for each patient |
| F-012 | SF-04 | Seamless handle | The handle has no gaps or seams, so it can be wiped clean with disinfectant |
| F-013 | SF-04 | Antimicrobial handle material | The handle is made from a plastic that resists germ growth |
| F-014 | SF-04 | Disposable grip covers | Single-use covers slip over the handles and are thrown away between patients |
| F-015 | SF-04 | UV cleaning case | The storage case shines UV light on the handles while the device is put away |
| F-016 | SW-06 | Force sensor between the handles | A sensor placed where the two handles meet measures the squeeze force directly |
| F-017 | SW-06 | Spring compression reading | The device measures how far the spring is squeezed and turns that distance into a force |
| F-018 | SW-06 | Air-filled squeeze bulb | The patient squeezes a sealed bulb, and the air pressure inside is turned into a force reading |
| F-019 | SW-06 | Motor effort estimate | Force is estimated from how hard the motor has to work to hold the handle in place |
| F-020 | SW-06 | Per-finger pressure pads | Thin pads under each finger report how hard each finger presses, as well as the total |
| F-021 | SW-04 | Force threshold counting | A repetition is counted each time the squeeze force rises above a set level and falls back |
| F-022 | SW-04 | Closed-handle switch | A switch clicks each time the handle is squeezed fully closed |
| F-023 | SW-04 | Motion sensor | A motion sensor in the handle recognizes the squeeze-and-release pattern |
| F-024 | SW-04 | Light-beam sensor | A light beam across the handle gap is broken each time the hand closes |
| F-025 | SW-04 | Phone camera counting | A phone app watches the hand through the camera and counts each squeeze |
| F-026 | MF-03 | Calibration weight hook | A hook lets a standard weight hang from the handle so the reading can be checked |
| F-027 | MF-03 | Guided calibration mode | A menu mode walks the technician through an empty step and a known-weight step |
| F-028 | MF-03 | Reference spring check | A spring of known stiffness is squeezed and the reading is compared with the force it should give |
| F-029 | MF-03 | Calibration dock | A dock presses the handle with a known force and corrects the reading automatically |
| F-030 | MF-03 | Automatic zero at startup | The reading resets to zero each time the device turns on with no one holding it |
| F-031 | MF-02 | Labeled test points | Marked metal pads on the circuit board where a meter probe can be clipped on |
| F-032 | MF-02 | Removable service cover | A panel unscrews to reach the circuit board without taking the whole device apart |
| F-033 | MF-02 | External test connector | One plug on the outside brings out the key signals for testing |
| F-034 | MF-02 | Live readings to a computer | The device sends its readings to a computer over a cable while it runs |
| F-035 | MF-02 | Status lights | Small lights show whether the sensor and motor are working, visible without any tools |

### 3.2 Actuation, Mechanics and Data (Gabriel)

<!-- OWNER: Gabriel. Prompts: SW-01, HW-01, HW-05, HW-03, MF-05, SW-03,
     SW-05 -> 7 prompts x 5 = 35 rows, F-036 to F-070. -->

| ID | Req ID | Feature | Detail |
|---|---|---|---|
| F-036 | SW-01 | Motor-driven spring preload | A gear motor turns a lead screw that compresses the return spring, so resistance changes with spring preload |
| F-037 | SW-01 | Magnetorheological brake | A fluid brake whose resistance changes with coil current, giving smooth resistance with no moving preload mechanism |
| F-038 | SW-01 | Motor-adjusted elastic tension | A motor changes the stretch of an elastic resistance element automatically to match the therapist's prescribed resistance |
| F-039 | SW-01 | Servo-positioned resistance lever | A servo moves the attachment point of the resistance mechanism to automatically increase or decrease mechanical resistance |
| F-040 | SW-01 | Electromagnetic resistance system | An electromagnet changes opposing force electronically so the controller can automatically apply the prescribed resistance level |
| F-041 | HW-01 | Sliding adjustable handle | One grip slides along a guided track so the distance between handles can be adjusted for different hand sizes |
| F-042 | HW-01 | Multi-position locking grip | The handle locks into several predefined positions covering a range of hand sizes |
| F-043 | HW-01 | Threaded grip-span adjustment | A screw mechanism moves the handle inward or outward to provide fine adjustment of grip span |
| F-044 | HW-01 | Interchangeable grip inserts | Different-sized grip inserts change the effective handle size to accommodate different users |
| F-045 | HW-01 | Self-adjusting grip | A spring-loaded sliding grip automatically conforms to the user's hand span within its allowable range |
| F-046 | HW-05 | Enclosed moving mechanism | A protective housing surrounds gears, springs and linkages so fingers cannot reach moving components |
| F-047 | HW-05 | Flexible joint guards | Flexible covers close gaps around moving joints while still allowing the mechanism to move |
| F-048 | HW-05 | Minimum-gap mechanical stops | Mechanical stops prevent moving surfaces from closing far enough to create a finger pinch point |
| F-049 | HW-05 | Internal linkage system | Linkages and pivot points are placed inside the housing rather than near the user's hand |
| F-050 | HW-05 | Pinch-detection cutoff | A sensor detects unexpected resistance near a moving mechanism and immediately stops its motion |
| F-051 | HW-03 | Integrated carrying handle | A handle built into the housing allows the entire device to be carried comfortably with one hand |
| F-052 | HW-03 | Compact tabletop enclosure | All mechanical and electronic components fit inside one compact housing that can be placed directly on a table |
| F-053 | HW-03 | Rechargeable battery power | An internal rechargeable battery allows operation without requiring a permanent power connection |
| F-054 | HW-03 | Foldable grip assembly | The grip mechanism folds into the housing to reduce the device's size during transportation |
| F-055 | HW-03 | Non-slip freestanding base | Rubber feet stabilize the device during use without clamps, screws or permanent installation |
| F-056 | MF-05 | Injection-moldable housing | The enclosure uses simple molded plastic parts suitable for inexpensive high-volume manufacturing |
| F-057 | MF-05 | Standard off-the-shelf motor | A commonly available motor reduces cost compared with a custom actuator |
| F-058 | MF-05 | Single-controller architecture | One microcontroller handles sensing, control and data functions to reduce electronic component count |
| F-059 | MF-05 | Shared mechanical components | Identical fasteners, bearings and other repeated components reduce the number of unique parts required |
| F-060 | MF-05 | Modular optional features | The base device includes essential rehabilitation functions while more expensive capabilities can be added as optional modules |
| F-061 | SW-03 | EEPROM session storage | Session results are saved to nonvolatile EEPROM so they remain available after power is removed |
| F-062 | SW-03 | MicroSD data storage | Each completed session is written to a removable microSD card that retains information without power |
| F-063 | SW-03 | Flash memory autosave | The controller automatically saves session progress to internal flash memory during training |
| F-064 | SW-03 | Backup capacitor save | Stored electrical energy gives the controller enough time to save the active session when power is suddenly lost |
| F-065 | SW-03 | Incremental session logging | Exercise results are saved after each repetition instead of waiting until the entire session is completed |
| F-066 | SW-05 | USB CSV export | Connecting the device by USB provides session records as standard CSV files readable by common spreadsheet programs |
| F-067 | SW-05 | Removable microSD export | Session files are stored on a microSD card that can be inserted directly into a computer |
| F-068 | SW-05 | USB mass-storage mode | The device appears as a standard flash drive when connected to a computer so records can be copied directly |
| F-069 | SW-05 | QR-code session export | The display generates a QR code containing a session summary that can be scanned with a phone |
| F-070 | SW-05 | Bluetooth standard-file transfer | The device transfers standard session files to a phone or computer using Bluetooth without requiring custom desktop software |


### 3.3 Interaction, Feedback and Prescription (Duotao)

<!-- OWNER: Duotao. Prompts: CU-01, CU-03, UX-01, UX-03, UX-04, UX-05
     -> 6 prompts x 5 = 30 rows, F-071 to F-100. -->

| ID | Req ID | Feature | Detail |
|---|---|---|---|
| F-071 | UX-01 | Single start button | Press a large button and you can continue the training as prescribed last time. |
| F-072 | UX-01 | Patient ID card tap | After swiping the NFC card, the device automatically loads the patient's file and training prescription. |
| F-073 | UX-01 | Qr coded patient card | Scan the QR code on the card to load the patient's training plan. |
| F-074 | UX-01 | Paired mobile phone recognition | The device recognizes the paired mobile phone, and the patient can start training with one click.|
| F-075 | UX-01 | Magnetic profile token | Insert the exclusive identification plate, select the patient file, and then press the Start button. |
| F-076 | CU-01 | Password-protected therapist menu | After the therapist enters the password, they set the resistance and target number of repetitions for the designated patient. |
| F-077 | CU-01 | USB prescription editor | The therapist connects the device to the computer to save the resistance and the target number of repetitions. |
| F-078 | CU-01 | Therapist configuration Card | The authenticated NFC card transmits the parameters set by the therapist to the device. |
| F-079 | CU-01 | Detachable setting keyboard | The therapist connects the keyboard to input the parameters. After setting them up, the keyboard is removed. |
| F-080 | CU-01 | A key-controlled knob | The therapist unlocks the knob with a key and then adjusts the resistance and the target number of repetitions.|
| F-081 | CU-03 | Peak grip strength threshold rule | If the measured peak grip strength differs from the set value by more than 10%, the equipment should be adjusted within the range specified by the therapist in the next training session. |
| F-082 | CU-03 | Two-direction progression | When the grip strength is too high or too low, increase or decrease the resistance as prescribed in the next training session. |
| F-083 | CU-03 | Patient-exclusive advanced table | Therapists preset different resistance adjustment magnitudes for different rehabilitation stages. |
| F-084 | CU-03 | Adjust according to the training trend | Refer to the recent training results of the equipment to select a more stable adjustment range for the next training. |
| F-085 | CU-03 | Pre-approved advanced rules | The therapist pre-approves the adjustment rules. When the measured grip strength meets the conditions, the device will automatically execute. |
| F-086 | UX-03 | Three-field OLED dashboard | The screen is divided into three columns, simultaneously displaying resistance, completed times and target times. |
| F-087 | UX-03 | Segmented LCD panel | Three fixed number areas make the three items of data in training always visible. |
| F-088 | UX-03 | Large-print e-paper panel | Display three sets of data in large characters and high contrast, and update the number of times each action is completed |
| F-089 | UX-03 | Three independent digital displays | Three named displays each show a piece of training data. |
| F-090 | UX-03 | Color TFT information screen | The color screen delineates a fixed area and simultaneously displays three types of data. |
| F-091 | UX-04 | Large low-force key | The patient can start or pause the training by pressing the wide button with a very small force. |
| F-092 | UX-04 | Capacitive touch area | It can be operated by simply touching the larger sensing area, without the need to press hard. |
| F-093 | UX-04 | voice activation  | Patients can operate by giving simple commands without pressing buttons. |
| F-094 | UX-04 | Optional foot switch | Patients can start or stop using the foot switch without having to use the hand being trained. |
| F-095 | UX-04 | Palm-operated rocker | The patient pushes the wide control keys with the palm of their hand, without having to use a single finger flexibly. |
| F-096 | UX-05 | piezoelectric buzzer | When the last action is recorded, the buzzer emits a prompt sound. |
| F-097 | UX-05 | Voice completion message  | The built-in speaker tells the patient by voice that the goal has been achieved. |
| F-098 | UX-05 | Exclusive completion prompt tone | The device plays a sound different from other alarms to let the patient know that the training is complete. |
| F-099 | UX-05 | Electromechanical chime | When the target number of times is reached, the small machine's electric bell makes a sound. |
| F-100 | UX-05 | Shell sound-emitting transducer | The transducer drives the equipment housing to emit a completion prompt sound. |

## 4. Sorting, Ranking and Refinement

<!-- WHAT: Step 3 of the assignment. Three things must be visible to the
     grader: the features are GROUPED, the features are RANKED (top ones
     clearly indicated in each group), and NEW features came out of the
     discussion. Plus snapshots proving the stages happened.

     Before the tables, write 2-3 sentences: what grouping axis the team
     chose and why (theme / function / user need / subsystem). -->
Once the board was full, the team rearranged the notes according to the job each feature does in the device. Sorting this way, instead of by author, put competing ideas for the same job next to each other, which made them easier to compare. The team then ranked the features inside each group, and talking through the rankings led to a handful of new features that joined ideas from separate groups.

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

**Pitch:** The "Adaptive Coach" is a home-based hand rehabilitation training device. It conducts training according to the prescription set by the therapist and adjusts subsequent training based on the patient's recent performance.

| ID | Feature | Satisfies |
|---|---|---|
| F-072 | Patient ID card tap | UX-01 |
| F-076 | Password-protected therapist menu | CU-01 |
| F-084 | Adjust according to the training trend | CU-03 |
| F-086 | Three-field OLED dashboard | UX-03 |
| F-091 | Large low-force key | UX-04 |
| F-097 | Voice completion message | UX-05 |
| F-036 | Motor-driven spring preload | SW-01 |
| F-001 | Quick-release cam lever | SF-02 |

<!-- ![Concept C storyboard](image/ideation/concept-c.svg)
     **Figure 6. Concept C — {name}, storyboard of a home session.** -->

The therapist sets the patient's training resistance and target repetitions through a password-protected menu. At home, the patient swips the identity card to load the training plan and then presses the effortless large button to start the training. During training, the OLED screen displays resistance, completed times and target times. When the goal is reached, the device will remind the patient by voice. The equipment refers to the recent training results to determine the resistance setting for subsequent training and makes adjustments through a motor-driven spring mechanism. If the patient needs to release the resistance immediately, they can manually pull the quick release rod.

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

The brainstorm session was run in-person by Zice Sun and Duotao Gao, Gabriel brainstormed by himself at a different time and location. We settled on rules like no judgement. We first jot down our ideas and not rush to consider whether they can be realized. In this way, we can come up with several solutions for the same problem. Starting from the requirements of the previous two assignments, we put forward ideas regarding grip strength mechanisms, strength measurement, and home use, and summarized them into 100 numbered functions. After that, we divided them into ten groups based on their functions to facilitate the comparison of similar solutions, while retaining the original numbers to meet the corresponding requirements.

---

## AI Use Disclosure

<!-- REQUIRED for EGR 304: full query disclosure on every submission.
     Update the description and the query list before export if more
     queries are made on this page (by anyone on the team). -->

Generative AI tools, including Claude, were used by Zice Sun to interpret the assignment requirements, propose the page structure, the prioritization method and the division of work, and provide example entries illustrating the expected format. All brainstormed features, rankings, concept designs and the process description reflect the team's own session and were reviewed by the team before submission.

Full query text:

1. EGR 304 team assignment: build a complete skeleton file, write clearly in English comments what each section should do and how to do it, fill 2 examples in each section, and divide the work among Zice Sun (me), Duotao Gao and Gabriel. [team repository link; assignment link]
