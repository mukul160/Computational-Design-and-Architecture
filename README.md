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

