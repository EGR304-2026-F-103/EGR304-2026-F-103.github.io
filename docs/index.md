<div align="center" markdown>

# Home

## Team 103 Embedded Systems Design Project

**Team 103**  
Duotao Gao · Gabriel Toneser Facchin · Zice Sun  

**Prepared:** September 3, 2026  
**Fall 2026**  
Arizona State University  
**EGR 304**  
Instructor: Zane Reynolds  

</div>

## Project Summary

**GripRx** is a prescription-based grip trainer for hand rehabilitation. A therapist sets the resistance and the number of repetitions; the device measures how hard the patient actually squeezes and moves its own resistance mechanism to match the prescription. A load cell measures grip force, a DC gear motor sets the preload of a return spring, and a character LCD, three large buttons and a speaker guide the patient through each set. If the force goes past the therapist's limit, or a cable comes loose, the resistance is released automatically. The electronics are split across three boards, one per team member, each built around a Microchip PIC18F57Q43 Curiosity Nano and linked in a daisy chain by 8-pin ribbon cables: the UI board (Duotao Gao), the force sensing board in the center (Zice Sun), and the motor board (Gabriel Toneser Facchin).

## Team Introduction

Team 103 is three engineering students in EGR 304 at ASU Polytechnic. Each of us designs one board of GripRx and documents it in an individual datasheet (linked in the table below), while this team report holds the work we did together. To follow the design from the beginning, read the pages in order: who we are and how we work, what users need, the requirements we derived from those needs, how we generated and chose a concept, how the three boards connect, and how the software runs across them.

## Report Pages

1. [Team Organization](02-Team-Organization.md): team charter and product mission
2. [User Needs and Benchmarking](03-User-Needs-and%20Benchmarking.md): stakeholders, user needs and competing products
3. [Product Requirements](04-Product-Requirements.md): requirements traced to the user needs
4. [Ideation and Concept Generation](05-design-ideation.md): about 100 features, three concepts and the final design
5. [Block Diagram, Process Diagram, and Message Structure](06-team-block-diagram.md): the three boards and every ribbon-cable pin
6. [Software Proposal](07-Software%20Proposal.md): software sequence, activity diagrams and message structure

## Team Members Datasheet links

| **Team Member**       | **Ind Datasheet Links**   |
| --------------------- | ------------------------- |
| Duotao Gao            | [duotaoga.github](https://duotaogao.github.io/duotaogao_EGR304_Fall-26-.github.io/)|
| Gabriel Toneser Facchin | [GabrielFacchin22.github](https://gabrielfacchin22.github.io/EGR304DataSheetTemplate/) |
| Zice Sun              | [empcity21.github](https://empcity21.github.io/Empcity21_EGR304_F26_Datasheet.github.io/) |
