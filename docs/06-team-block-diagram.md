---
title: Block Diagram, Process Diagram, and Message Structure
---

# Block Diagram, Process Diagram, and Message Structure

<!-- ============================================================
     HOW TO WORK ON THIS PAGE
     (HTML comments do not appear on the published page or in the PDF.
     No need to delete them when you are done.)

     DUE: Team: Block Diagram — Canvas, Fri 10/2 (confirm the time on
     Canvas). Submit BOTH: (1) the working URL of this page and (2) a PDF
     exported from the LIVE page.
     Points: 50 initial (completeness) + 150 External Design Review
     (quality, 10/26–10/30) + 50 final report = 250.

     WHAT THE ASSIGNMENT GRADES (Design Checklist on the course site)
       - Page is easy to find (linked from the landing page)      -> index.md
       - Each teammate's role is clear, sensors/actuators marked  -> §2, §4
       - Each subsystem: sufficient complexity, unique, has at
         least one sensor OR actuator                             -> §2, §6.2
       - Each microcontroller well-marked; every IC has
         Manufacturer + Part # (unknown = yellow highlight)       -> §4 figure
       - Wires use directional arrows + labels; lines tidy        -> §4 figure
       - >= 1 ribbon connector per teammate; class standard used
         (pins 1–5 digital, 6–7 analog, 8 GND)                    -> §5
       - Every used ribbon pin is mapped to a SPECIFIC MCU pin,
         never straight to a sensor/actuator                      -> §5
       - Individual block diagrams (due 10/5) match this one       -> §7
       - Spelling correct; image legible on the website           -> all

     OWNERSHIP
       Zice    — §1, §3, §5 Zice-side columns, §6, §7, AI disclosure;
                 master draw.io file (layout, connectors, cable arrows,
                 force board), PNG export, landing-page link, build,
                 PDF export, Canvas submission
       Gabriel — Motor board: his group in the draw.io file, his row in
                 Table 1, the Gabriel column of Table 3, spelling pass
                 on the finished diagram
       Duotao  — UI board: his group in the draw.io file, his row in
                 Table 1, the Duotao column of Table 2, Design Checklist
                 review of the live page before PDF export
       Everyone — the Step 1 meeting (topology + pin map decisions);
                 review §6 answers before export

     HARD RULES
       1. Ribbon pins connect to the teammate's MICROCONTROLLER pins only.
          A sensor or actuator never sits directly on a ribbon pin.
       2. Pin 8 = GND on every connector. Do NOT pass +5 V or 9 V through
          the ribbon — every board has its own barrel jack + 5 V regulator.
       3. Do not use RF0/RF1 (USB CDC serial = UART1, keep for debugging),
          RF3 (on-board LED0) or RB4 (on-board SW0) for team signals.
       4. UART TX/RX pins are chosen with PPS. Pick them in MCC Pin Grid
          View (it only offers legal pins) and copy the result here.
       5. The diagram is embedded as a PNG in this repo, and the .drawio
          source is committed next to it. Never link to a live Google
          Drive / draw.io file as the content of this page.
       6. Keep tables narrow (<= 6 short columns) for the PDF export.
     ============================================================ -->

## 1. Overview

<!-- OWNER: Zice. 3–5 sentences. What this page is, what the three
     boards are, and how to read the rest of the page. Report tone. -->

This page defines how the three subsystem boards of Team 103's prescription-based grip trainer connect and communicate. Each team member designs one board around a Microchip PIC18F57Q43 Curiosity Nano, and the boards are joined by 8-wire ribbon cables that follow the class connector standard. [FILL: one or two more sentences summarizing the arrangement and pointing the reader to Figure 1 and Tables 2–3.]

## 2. Subsystem Roles

<!-- OWNER: each person fills their own row; Zice checks consistency.
     Every IC needs Manufacturer + Part #. If a part is not chosen yet,
     write "TBD" here AND leave it highlighted yellow in the diagram.
     Sensor/actuator column must name the item that satisfies the course
     requirement (Course Sequence Requirements page):
       Zice    — load cell + amplifier + active filter = acceptable
                 analog sensor ("Load-cells & wheatstone bridges").
       Gabriel — DC gear motor on an H-bridge driver IC = acceptable
                 actuator (bidirectional, driver IC).
       Duotao  — speaker driven by DAC/PWM through a filter + amplifier
                 stage = acceptable actuator. Display and buttons are
                 extra user interface, they do NOT count on their own. -->

**Table 1. Subsystem boards and their owners.**

| Board | Owner | Main function | Sensor / actuator | Key ICs (Manufacturer, Part #) |
|---|---|---|---|---|
| Force board (center) | Zice Sun | Measures grip force, runs the session logic, relays messages between the other two boards | Sensor: load cell, [FILL: Manufacturer, Part #] | Texas Instruments INA125P; [FILL: op-amp for active low-pass filter] |
| Motor board | Gabriel Toneser Facchin | [FILL] | [FILL] | [FILL] |
| UI board | Duotao Gao | [FILL] | [FILL] | [FILL] |

## 3. Connection Arrangement

<!-- OWNER: Zice. Explain the topology chosen at the Step 1 meeting and
     WHY. Points worth making (pick, do not list them all):
       - Daisy chain UI board <-> Force board <-> Motor board.
       - Force is the one quantity both other boards need, so the board
         that measures it sits in the middle; the two end boards never
         need to talk directly.
       - Every board-to-board link carries the same pattern of signals
         (UART on 1–2, a dedicated safety line on 3), so the center
         board's firmware for the two links is nearly identical.
       - Each link uses only 3–4 of the 7 signal pins, leaving spares
         for changes before the External Design Review. -->

The boards are connected in a daisy chain, with the force board in the middle: the UI board connects to connector J1 of the force board, and the motor board connects to connector J2. [FILL: 2–3 sentences on why the team chose this arrangement.]

## 4. Team Block Diagram

<!-- OWNER: Zice merges; each member draws the inside of their own board.
     FILES (exact names, no spaces):
       docs/image/team-block-diagram.png     <- PNG export, transparent
       docs/image/team-block-diagram.drawio  <- draw.io source
     The PNG currently in the repo is a PLACEHOLDER. Overwrite it with
     your export using the same file name and this section updates
     itself. The .drawio link below shows a build warning until that
     file is committed — that is expected.
     draw.io export: File > Export as > PNG..., tick "Transparent
     Background", Zoom 200%, Border Width 10. Check the image is still
     readable on the live page AND in the exported PDF. -->

![Team 103 block diagram: the UI board, force board and motor board, each built around a PIC18F57Q43 Curiosity Nano, linked in a daisy chain by two 8-pin ribbon cables with every ribbon pin mapped to a microcontroller pin](image/team-block-diagram.png)
**Figure 1. Team 103 block diagram.** [FILL: one sentence on how to read it, e.g. what the yellow highlights mean.]

The editable source of Figure 1 is available as a [draw.io file](image/team-block-diagram.drawio).

## 5. Ribbon Cable Pin Assignments

<!-- OWNER: Zice fills the Signal / Direction / Zice-pin columns;
     Duotao fills his pin column in Table 2, Gabriel in Table 3.
     The Type column is the class standard — do not change it.
     Direction is written as source -> destination.
     MCU pin = the exact Curiosity Nano pin (e.g. "RA2 (DAC1)"), as set
     in MCC. Unused pins: Signal "Not connected", Direction "—", pin "—".
     The pin plan agreed at the Step 1 meeting goes here; the proposed
     plan is in the task guide PDF (section 3). -->

**Table 2. Connector J1: force board (Zice) to UI board (Duotao).**

| Pin | Type | Signal | Direction | Zice MCU pin | Duotao MCU pin |
|---|---|---|---|---|---|
| 1 | Digital | UART data, force board to UI board | Zice -> Duotao | [FILL: U?TX pin] | [FILL: U?RX pin] |
| 2 | Digital | [FILL] | [FILL] | [FILL] | [FILL] |
| 3 | Digital | [FILL] | [FILL] | [FILL] | [FILL] |
| 4 | Digital | [FILL] | [FILL] | [FILL] | [FILL] |
| 5 | Digital | [FILL] | [FILL] | [FILL] | [FILL] |
| 6 | Analog | [FILL] | [FILL] | [FILL] | [FILL] |
| 7 | Analog | [FILL] | [FILL] | [FILL] | [FILL] |
| 8 | Ground | Common ground | — | GND | GND |

**Table 3. Connector J2: force board (Zice) to motor board (Gabriel).**

| Pin | Type | Signal | Direction | Zice MCU pin | Gabriel MCU pin |
|---|---|---|---|---|---|
| 1 | Digital | [FILL] | [FILL] | [FILL] | [FILL] |
| 2 | Digital | [FILL] | [FILL] | [FILL] | [FILL] |
| 3 | Digital | [FILL] | [FILL] | [FILL] | [FILL] |
| 4 | Digital | [FILL] | [FILL] | [FILL] | [FILL] |
| 5 | Digital | [FILL] | [FILL] | [FILL] | [FILL] |
| 6 | Analog | [FILL] | [FILL] | [FILL] | [FILL] |
| 7 | Analog | [FILL] | [FILL] | [FILL] | [FILL] |
| 8 | Ground | Common ground | — | GND | GND |

## 6. Design Decisions

<!-- OWNER: Zice writes from the Step 1 meeting notes; Gabriel and
     Duotao review. One short paragraph per question. These are the three
     questions the assignment tells the team to answer before drawing.
     Write what the TEAM decided and why, not a generic answer. -->

### 6.1 Minimizing interconnections

<!-- Question: "You only have 8-pin connectors. How do you divide
     functionality across the team in a way that minimizes
     interconnections between teammates?" -->

[FILL: one paragraph.] For example: all data passes over a single UART pair on each link, so adding a new message later changes firmware, not wiring.

### 6.2 Meeting the minimum requirements

<!-- Question: "Does your system layout ensure each teammate meets
     minimum project requirements?" Name each person's qualifying
     sensor/actuator and why it qualifies; say the three are different
     chips, functions and design processes, and that the team as a
     whole mixes sensing and actuation. -->

[FILL: one paragraph.]

### 6.3 Risk if a teammate is lost

<!-- Question: "What are the risks to your system if you lose a
     teammate? How can you de-risk your system design by grouping and/or
     distributing similar functions between teammates?"
     Cover all three cases, including the honest one: the center board
     is the single point of failure. Say what the team does about it. -->

[FILL: one paragraph.]

## 7. Next Steps

<!-- OWNER: Zice. 2–4 bullet points. -->

- Each member's individual block diagram (due 10/5) will use exactly the connector pins and microcontroller pins listed in Tables 2 and 3.
- [FILL]

<!-- RESERVED — later assignments add to this page (the page title
     already names them). Leave hidden until then:
## Process Diagram
## Message Structure
-->

---

## AI Use Disclosure

<!-- REQUIRED for EGR 304: full query disclosure on every submission.
     Add Gabriel's and Duotao's use (or a statement that they used none)
     and any further queries before export. -->

Generative AI (Claude) was used by Zice Sun to read and summarize the assignment requirements, propose a division of work and a draft connector pin plan for team discussion, and generate this page's blank structure with one example entry per section. The board roles, connection arrangement, pin assignments, block diagram and written answers were decided and produced by the team.

Full query text:

1. I need to do the EGR 304 team assignment: assign tasks to the three team members, and produce the detailed steps and an overview as PDFs, in a Chinese and an English version. If needed, create a skeleton file like before. [team repository link; assignment link]

2. (Answer to "Which board does each member own?") Give me the most complex board, the one that ties all the boards together, and give Gabriel the simplest one.

3. (Answer to "How are the three boards connected?") Force board in the center, daisy chain.

[FILL: Gabriel's and Duotao's AI use, or a statement that they used none.]
