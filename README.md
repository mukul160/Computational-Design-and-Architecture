# Architectural Research Reading Log

This repository documents peer-reviewed research papers in
computational architecture, digital fabrication, and architectural robotics,
with a focus on work relevant to ITKE, IAAC, ETH Zürich, and related labs.

## Papers

### [2022] Jenny et al. — Robotic on-site adaptive thin-layer printing: Challenges and workflow for design and fabrication of bespoke cementitious plasterwork at full architectural scale 
- Context: 
  - The paper explores Robotic Plaster Spraying (RPS), a novel method for applying bespoke, cementitious plasterwork in a 1:1 scale construction setting.
  - Conventional manual plastering is a highly skilled craft often limited to flat surfaces; this research seeks to use digital fabrication to unlock the three-dimensional, ornamental potential of the material.
  - It addresses the need for on-site, adaptive fabrication that can respond to unpredictable material behavior and existing building structures.

- Contribution:
  - Demonstrates a human-in-the-loop workflow called Interactive Robotic Plastering (IRoP), which allows users to design interactively on-site while fabrication is ongoing.
  - Introduces a non-horizontal, thin-layer printing technique where layers are applied vertically, unlike most traditional 3D concrete printing processes.
  - Provides a method for predicting complex-to-simulate material behavior using data collected from physical results.

 
- Computational strategy:
  - Utilizes a controller-based interaction tracking system (HTC VIVE) and an augmented reality interface to map human gestures to robotic parameters.
  - Employs a 3-point localization method using a total station to orient the robot within a digital twin of the building.
  - Features a data-driven prediction model (initially linear) to visualize the 3D spray outcome before execution, helping designers understand how distance and velocity affect thickness.

- Material / fabrication:
    - Material: A dry-mix, base coat lime-cement plaster (Weber IP 18 Turbo) mixed in 25–30 kg batches.
    - Hardware: A UR10 collaborative robotic arm mounted on a semi-mobile 2-DoF vertical axis tower, equipped with a pneumatic spray gun, a pinch valve for flow control, and a depth camera.
    - Process: Multiple millimeter-thin layers are sprayed to build up 2D and 3D formations without formwork, controlled by parameters like end-effector distance ($E_d$), angle, and velocity ($V$).
  
- Why it matters:
  - It shifts digital fabrication from pre-determined "black box" processes to adaptive, on-site creation that can integrate the "tacit knowledge" of human designers.
  - The technique allows for complex architectural articulations and ornamental qualities that functionalize the material (e.g., for light diffusion or acoustics) directly on existing structures.
  - It reduces waste by eliminating the need for support structures or formwork.

- Limitations:
    - Segmentation: Relocating the robot creates "cold joints" or visible interruptions between sprayed segments, requiring complex branching strategies to hide.
    - Sensing Resolution: The current depth camera (Intel RealSense D455) provides a rough estimate of thickness but lacks the resolution to capture fine surface textures or accurately assess prediction accuracy.
    - Mobility: The current system is semi-mobile and requires manual relocation; a fully mobile, synchronized platform is needed for truly continuous printing.
 
- Takeaway:
  - Robotic Plaster Spraying proves that complex, unpredictable materials can be used for bespoke architectural design through a combination of real-time sensing, human interaction, and predictive modeling.

- Tags:
  - Tags: - #RoboticFabrication #3DConcretePrinting #InteractiveDesign #AugmentedReality #OnSiteConstruction #ComputationalDesign #CementitiousMaterials

---
### Augmented Human, Extended Machine  
**Daniela Mitterberger (2022)** — *XRDS / ACM*  
DOI: 10.1145/3558196

**Context**  
Robotic fabrication in AEC struggles in unstructured environments. Existing GUI-based, linear workflows marginalize human involvement and suppress embodied, tacit knowledge during fabrication.

**Contribution**  
Proposes extended reality (XR) as a framework for reciprocal human–machine augmentation, enabling embodied, real-time human–robot collaboration in architectural fabrication.

**Computation Strategy**  
Real-time, bidirectional feedback loops translate human motion and interaction into robotic trajectories via an interactive computational model (“design-synthesizer”).

**Material / Fabrication**  
On-site robotic plaster spraying (IRoP) using projection-based AR and motion capture, integrating craft-based hand movements directly into robotic fabrication.

**Why it Matters**  
Reframes human-in-the-loop fabrication as a strength rather than a limitation, enabling adaptive, site-specific, and collaborative robotic construction workflows.

**Limitations**  
Hardware-intensive XR setups; task- and user-specific interface design; limited scalability beyond experimental contexts.

**Key Takeaway**  
XR enables a “workmanship of synthesis,” balancing machine precision with human judgment by overlapping design and fabrication through embodied interaction.

**Tags**  
`XR` `Human-in-the-loop` `Robotic Fabrication` `Digital Embodiment` `AR Interfaces` `AEC Robotics`

---

# Outcomes vs Rails: The Race to a $10B Construction Robotics Giant

## Context
The paper analyzes why construction robotics is finally becoming viable after decades of failure, and frames the market around two dominant strategies: **outcome-driven vertical robots** that execute specific construction tasks, and **infrastructure (“rails”) platforms** that provide the autonomy, orchestration, and data layers enabling robotic systems at scale.

## Core Thesis
Construction robotics will produce decacorns, but **durable $10B-scale value is more likely to emerge from infrastructure (rails) platforms than from task-specific outcome providers**, despite outcomes winning early adoption.

## Section-by-Section One-Line Summaries

### The Case for Construction Robotics
- Construction faces a structural crisis driven by labor shortages, rising costs, and decades of stagnant productivity.
- Early construction robots failed due to fragility, cost, and inability to handle unstructured sites.
- Advances in AI, sensing, simulation, and compute have finally made on-site robotic deployment feasible.
- Investment momentum has returned strongly, with construction robotics becoming a breakout ConTech category.
- Robotics startups cluster into two camps: foundational infrastructure builders and task-specific vertical operators.

### Outcomes vs Rails Framing
- “Rails” provide the connective infrastructure that enables robotic systems to function together.
- “Outcomes” use those rails to directly perform construction work like bricklaying or rebar tying.
- The key question is which model can generate a defensible, long-term construction robotics decacorn.

### Outcomes: Vertical, Task-Focused Robotics
- Outcome-driven startups target well-defined labor bottlenecks with robots optimized for one task.
- Vertical robots are easy for contractors to evaluate because ROI maps directly to time, cost, and labor savings.
- Selling completed work often fits better into construction procurement than selling technology.
- Narrow scope allows vertical robots to achieve production-grade reliability faster than general platforms.
- Precision and tolerance guarantees transform robotics performance into contractual risk reduction.
- Outcome models tolerate imperfect autonomy by backstopping failures operationally.
- Vertical focus accelerates adoption but inherently limits total addressable market.
- Scaling outcome providers is operationally intensive and resembles field services more than SaaS.
- Defensibility comes from execution and experience rather than deep platform lock-in.
- Vertical-first companies eventually face growth ceilings unless they expand scope or evolve into platforms.

### Rails: Infrastructure and Platform Robotics
- Rails providers supply autonomy, mapping, orchestration, simulation, and data layers rather than finished work.
- Infrastructure platforms parallel cloud computing’s role in enabling downstream applications.
- Shared infrastructure benefits from compounding data, cross-use-case learning, and ecosystem adoption.
- Platform scale creates network effects that are difficult for vertical competitors to replicate.
- Infrastructure-first models favor high-margin software over hardware deployment.
- Hardware differentiation is diminishing, shifting competitive advantage to software orchestration.
- Rails platforms can monetize via subscriptions, APIs, and OEM integrations.

### Challenges of Infrastructure Platforms
- Platforms are harder to build and sell because they must solve broad problems upfront.
- Construction autonomy still struggles with reliability, explainability, and certification.
- Infrastructure startups face a catch-22: needing scale to prove value but value to reach scale.
- Outcome providers capture richer failure data due to operational ownership.
- Rails players benefit from OEM and rental distribution but face complex stakeholder politics.
- Infrastructure risks commoditization if abstraction layers become interchangeable.
- Deep integration into mandatory systems (BIM, compliance, payments) can create defensibility.
- Data ownership constraints limit AI flywheels compared to consumer or automotive robotics.
- Mega-valuations increase risk if platform adoption does not compound fast enough.

### Convergence and Hybrid Strategies
- Outcomes and rails are not mutually exclusive and will increasingly converge.
- Outcome-led companies can more easily grow upward into platforms than vice versa.
- Vertical deployments provide access to real-world edge cases that platforms struggle to obtain

---
