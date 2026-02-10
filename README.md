# Architectural Research Reading Log

This repository documents peer-reviewed research and position papers in computational architecture, digital fabrication, and architectural robotics, with a focus on work relevant to ITKE, IAAC, ETH Zürich, and related labs.

---

## [2022] Jenny et al.  
**Robotic On-Site Adaptive Thin-Layer Printing: Challenges and Workflow for Design and Fabrication of Bespoke Cementitious Plasterwork at Full Architectural Scale**

**Context**  
Conventional plastering is a highly skilled manual craft, typically limited to planar surfaces. Existing digital fabrication workflows struggle with unpredictable material behavior and unstructured construction sites, especially at full architectural scale.

**Core Contribution**  
Introduces *Interactive Robotic Plastering (IRoP)*, a human-in-the-loop, on-site fabrication workflow that enables designers to shape bespoke plaster geometries interactively during robotic execution.

**Computational / Technical Strategy**  
Human gestures are captured via motion tracking and mapped in real time to robotic parameters using AR interfaces. A controller-based interaction system and digital twin alignment allow designers to preview and influence spray outcomes during fabrication. A data-driven prediction model estimates thickness based on distance and velocity.

**Material / Fabrication**  
A lime-cement plaster (Weber IP 18 Turbo) is sprayed in millimeter-thin vertical layers using a UR10 robotic arm mounted on a semi-mobile vertical axis tower. Thickness and geometry are controlled through end-effector distance, angle, and velocity without formwork.

**Why It Matters**  
Demonstrates that complex, craft-based materials can be digitally fabricated on-site through adaptive workflows that integrate human judgment. Shifts robotic construction from pre-scripted automation toward responsive, situated making.

**Limitations**  
Segmented fabrication leads to visible joints when the robot is relocated. Depth sensing lacks sufficient resolution for fine texture analysis. System mobility remains limited and requires manual repositioning.

**Key Takeaway**  
Robotic plaster spraying can support expressive, site-specific architecture when combined with real-time sensing, human interaction, and predictive computation.

**Tags**  
`Robotic Fabrication` `On-Site Construction` `Human-in-the-Loop` `3D Concrete Printing` `Augmented Reality` `Cementitious Materials`

---

## [2022] Daniela Mitterberger  
**Augmented Human, Extended Machine** — *XRDS / ACM*  
DOI: 10.1145/3558196

**Context**  
Robotic fabrication in architecture struggles in unstructured environments, where rigid, GUI-driven workflows suppress embodied knowledge and reduce human agency during construction.

**Core Contribution**  
Proposes extended reality (XR) as a framework for reciprocal human–machine augmentation, enabling embodied, real-time collaboration between designers, builders, and robotic systems.

**Computational / Technical Strategy**  
Introduces a bidirectional feedback loop where human motion and interaction directly influence robotic trajectories through an interactive computational “design-synthesizer.”

**Material / Fabrication**  
Demonstrated through on-site robotic plaster spraying (IRoP) using motion capture and projection-based AR, translating craft gestures into robotic fabrication parameters.

**Why It Matters**  
Reframes human involvement as a strength rather than a limitation, enabling adaptive, site-responsive robotic workflows that merge design and making.

**Limitations**  
XR systems are hardware-intensive, require task-specific interface design, and remain difficult to scale beyond experimental contexts.

**Key Takeaway**  
XR enables a “workmanship of synthesis,” balancing machine precision with human judgment through embodied interaction.

**Tags**  
`XR` `Human-in-the-Loop` `Robotic Fabrication` `Digital Embodiment` `AR Interfaces` `AEC Robotics`

---

## [2024] Alexi et al.  
**Cooperative Augmented Assembly (CAA): Augmented Reality for On-Site Cooperative Robotic Fabrication** — *Construction Robotics*

**Context**  
Fully autonomous construction systems struggle with uncertainty, tolerance variation, and situational complexity on real building sites.

**Core Contribution**  
Introduces *Cooperative Augmented Assembly (CAA)*, a framework where humans and robots collaboratively assemble architectural structures rather than relying on full automation.

**Computational / Technical Strategy**  
Augmented Reality functions as a shared interface, visualizing assembly sequences, tolerances, and robotic actions for both humans and machines in real time.

**Material / Fabrication**  
Robots assist with precision, reach, and strength, while humans handle alignment, judgment, and situational decision-making during on-site assembly.

**Why It Matters**  
Shows that cooperative human–robot systems are more robust than fully autonomous approaches in unpredictable construction environments.

**Limitations**  
Relies on accurate AR registration and coordinated workflows; productivity gains depend heavily on user training and interface quality.

**Key Takeaway**  
Human–robot cooperation offers a scalable and resilient model for architectural robotics that integrates, rather than replaces, human expertise.

**Tags**  
`Architectural Robotics` `Human–Robot Collaboration` `Augmented Reality` `On-Site Fabrication` `Computational Design`

---

## [2023]  
**Outcomes vs Rails: The Race to a $10B Construction Robotics Giant**

**Context**  
Construction robotics has repeatedly failed to scale due to unstructured sites, weak autonomy, and poor economics. Recent advances in AI, sensing, and compute have revived the sector.

**Core Thesis**  
While task-specific “outcome” robots win early adoption, durable $10B-scale value is more likely to emerge from infrastructure (“rails”) platforms that provide autonomy, orchestration, and data layers.

**Computational / Technical Strategy**  
Rails platforms focus on mapping, simulation, orchestration, and data aggregation across robotic systems, while outcome providers optimize vertically integrated task execution.

**Why It Matters**  
Frames construction robotics as a platform-vs-vertical dynamic similar to cloud computing, clarifying where long-term defensibility and scale may emerge.

**Limitations**  
Infrastructure platforms face slow adoption, data ownership constraints, and a catch-22 between scale and demonstrated value. Outcome providers scale faster but face operational and TAM limits.

**Key Takeaway**  
Vertical robots drive early traction, but infrastructure platforms are better positioned for compounding value—though hybrid strategies will likely dominate.

**Tags**  
`Construction Robotics` `Platforms vs Verticals` `Autonomy Infrastructure` `AEC Technology` `Robotics Strategy`

---

## Degrees of Life
**Degrees of Life** is an experimental architectural environment that explores how human attention can influence living systems embedded within space.
Rather than treating architecture as a static object or a controllable machine, the project frames it as a **co-evolving system** involving humans, computation, and biological matter.

### Core Idea
The research proposes that **human perception itself**—specifically visual attention—can function as an architectural input.
Instead of explicit commands or interfaces, the project uses gaze to create indirect, non-deterministic interactions with living organisms.

### Human Attention as Input
Visitors wear an eye-tracking device that measures where they look, for how long, and with what intensity (including unconscious signals such as pupil dilation).
Gaze is interpreted as sustained attention rather than intentional control, allowing the system to respond to what draws human focus over time.

### Living Environments
The installation consists of three enclosed environments hosting different bacteria: *Escherichia coli*, *Sucrofermentas*, and cyanobacteria.
Each environment responds to gaze-driven machine actions that alter conditions such as chemical composition, nutrient distribution, or light exposure.

### Feedback Loops
Human attention triggers subtle environmental changes, while biological processes respond slowly and autonomously.
The resulting system forms a feedback loop in which humans influence conditions, bacteria transform the environment, and those transformations in turn shape human perception.

### Broader Implications
Degrees of Life challenges control-oriented models of interactive architecture by emphasizing **influence over command**.
It suggests future architectural systems that respond to presence, attention, and long-term behavioral patterns rather than explicit user input.

### Significance
The project expands architectural computation beyond optimization and automation toward **co-authorship with living systems**.
It positions architecture as an ongoing process that unfolds across biological, computational, and human timescales rather than a finished artifact.

### Keywords
Living Architecture · Human Attention · Bio-computation · Responsive Environments · Co-evolving Systems

---
