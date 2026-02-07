# FLUX-GEO  
**Multiphase Flow and Transport Modeling for Subsurface Energy and Storage Systems**

---

## Executive Summary

**FLUX-GEO** is a comprehensive, Python-driven computational framework for subsurface flow, transport, and coupled process modeling across energy, environmental, and storage applications. The platform integrates multiple, well-established numerical simulators—including **PFLOTRAN**, **FEHM**, **MODFLOW**, **VS2DI**, and **VS2DTI**—within a unified, transparent, and reproducible workflow.


FLUX-GEO is designed to support the **full modeling lifecycle**, from conceptual model development and scenario design to simulation execution, postprocessing, parameter estimation, uncertainty analysis, and decision-ready reporting. By combining solver-appropriate physics with a consistent Python orchestration layer, the framework preserves the numerical strengths of each engine while eliminating fragmentation in setup, analysis, QA/QC, and documentation.

The platform delivers **traceable simulation packages**, operational scenarios with explicit physical and engineering constraints, and **decision-ready outputs** suitable for technical review, regulatory-style documentation, and stakeholder communication. Emphasis is placed on physical realism, transparent assumptions, reproducibility, and defensible uncertainty framing, enabling robust evaluation of **groundwater flow**, **multiphase and gas–liquid systems**, **reactive transport**, **near-field and variably saturated processes**, **microfluidic and pore-scale behavior**, and **long-term system performance** across a wide range of subsurface applications.

---

## Capabilities

FLUX-GEO provides an integrated, multi-scale modeling capability spanning laboratory, field, and regional domains. Each capability leverages the most appropriate numerical engines while maintaining a consistent workflow for scenario definition, execution control, postprocessing, parameter estimation, QA/QC, and reporting.

---

### Groundwater Flow and Solute Transport

FLUX-GEO supports saturated groundwater flow and solute transport modeling for environmental, energy, and infrastructure applications.

#### What We Can Do
- Regional- and site-scale groundwater flow modeling  
- Hydraulic head and pressure evolution under natural and engineered stresses  
- Conservative and reactive solute transport  
- Recharge, boundary-condition, and property sensitivity analysis  

**Primary engines:**  
- **MODFLOW and MODFLOW-family tools**

**Supporting engines:**  
- **PFLOTRAN** (density-dependent flow and coupled transport)  
- **FEHM** (flow with thermal coupling)

---

### Multiphase Flow (CO₂, H₂, Gas–Water Systems)

FLUX-GEO supports multiphase flow and gas–liquid interaction modeling across reservoir-scale, near-field, and transition-zone regimes.

#### What We Can Do
- Gas injection scenarios with pressure buildup and plume migration  
- Buoyancy-driven flow, containment, and trapping behavior  
- Salinity- and temperature-dependent effects  
- Coupled saturated–unsaturated transitions near wells and boundaries  

**Primary engines:**  
- **PFLOTRAN** — multiphase gas–water flow and compositional effects  
- **FEHM** — multiphase and thermal–hydrologic systems  

**Supporting engines:**  
- **MODFLOW-family (density-aware formulations)**  
- **VS2DI / VS2DTI** for near-field and partially saturated zones  

---

### Wells, Operations, and Engineering Constraints

FLUX-GEO represents coupled wells and operational controls under realistic engineering and regulatory constraints.

#### What We Can Do
- Injection and production scheduling (CO₂, H₂, brine, water)  
- Pressure, rate, and fracture-gradient constraint enforcement  
- Well interference analysis and operational trade studies  
- Field-level performance metrics and diagnostics  

**Primary engines:**  
- **PFLOTRAN, FEHM**

**Supporting engines:**  
- **MODFLOW well packages**  
- **Python-based operational logic** for scheduling and constraint handling  

---

### Reactive Transport and Geochemical Processes

FLUX-GEO incorporates reactive transport where geochemistry governs system evolution and long-term behavior.

#### What We Can Do
- Coupled flow, transport, and geochemical reaction modeling  
- Mineral dissolution/precipitation and gas partitioning  
- Time-dependent mass balance and reaction-path analysis  
- Permanence, storage, and transformation metrics with explicit assumptions  

**Primary engines:**  
- **PFLOTRAN**

**Supporting workflows:**  
- Python-based reaction bookkeeping, diagnostics, and reporting  

---

### Variably Saturated Flow and Near-Field Processes

FLUX-GEO supports vadose-zone and near-surface modeling where capillary effects and partial saturation dominate.

#### What We Can Do
- Variably saturated flow and transport simulations  
- Infiltration, leakage, and near-field process representation  
- Coupling of vadose-zone and deeper saturated or multiphase systems  

**Primary engines:**  
- **VS2DI, VS2DTI (VS2DRTI)**

---

### Microfluidic and Pore-Scale Simulations

FLUX-GEO supports microfluidic, pore-scale, and laboratory-scale simulations for process understanding, benchmarking, and scale-bridging.

#### What We Can Do
- Flow and transport in microfluidic and lab-on-chip geometries  
- Geometry-controlled experiments and synthetic pore networks  
- Upscaling insights to inform continuum-scale models  

**Primary engines:**  
- **PFLOTRAN** (micro-domain configurations)  
- **FEHM** (small-scale domains)

**Supporting workflows:**  
- Python-based geometry generation, meshing, and analysis  

---

### Parameter Estimation, Inverse Modeling, and Uncertainty Analysis

FLUX-GEO provides parameter estimation and inverse modeling capabilities across all supported simulators.

#### What We Can Do
- Calibration of hydraulic, transport, thermal, and reactive parameters  
- Gradient-free, ensemble-based, and sampling-driven inverse workflows  
- Sensitivity analysis, identifiability assessment, and uncertainty propagation  
- Cross-solver parameter comparison and risk framing  

**Supported engines:**  
- **PFLOTRAN, FEHM, MODFLOW, VS2DI, VS2DTI**

**Integration layer:**  
- Python-based optimization, sampling, and diagnostic tools  

---

### Post-Processing, KPIs, and Reporting

FLUX-GEO converts raw simulator outputs into consistent, decision-ready products.

#### What We Can Do
- Automated plots for pressure, flow, plume extent, and transport metrics  
- Mass balance, storage partitioning, and diagnostic KPIs  
- Cross-solver comparison and standardized reporting  
- Outputs suitable for technical, regulatory, and stakeholder review  

---

### Reproducibility, QA/QC, and Audit Readiness

FLUX-GEO is designed to produce defensible, auditable results.

#### What We Can Do
- Fully reproducible run packages with complete provenance  
- Solver-agnostic QA/QC (mass balance, stability, convergence checks)  
- Versioning, change tracking, and assumptions registers  
- Transparent linkage from inputs to final deliverables  

---

## Why This Matters for Clients

FLUX-GEO reduces technical risk by transforming complex subsurface problems into **transparent, testable, and repeatable modeling workflows**. By supporting **groundwater flow, multiphase systems, reactive transport, parameter estimation, and pore-scale processes within a single coherent platform**, FLUX-GEO enables faster insight, clearer uncertainty communication, and stronger technical justification for decisions related to energy systems, environmental management, and subsurface storage.



---

## Deliverables

FLUX-GEO deliverables are structured to scale with data availability, project maturity, and decision needs. Each deliverable set produces **fully traceable, reproducible modeling artifacts** designed to support technical review, risk assessment, and stakeholder communication.

All deliverables include documented assumptions, solver configurations, QA/QC checks, and version-controlled outputs to ensure defensibility and reproducibility.

---

### Deliverable Set A — Rapid Screening and Feasibility Assessment (2–4 Weeks)

**Objective:** Provide a defensible first-pass evaluation to inform go/no-go decisions and prioritize data collection.

#### Deliverables
- Screening-scale models sized to available information, capturing:
  - Injectivity and pressure response  
  - First-order plume or influence-zone behavior  
  - Dominant flow and transport controls  
- Targeted sensitivity analysis identifying parameters that most strongly influence outcomes (e.g., permeability, relative permeability, salinity, temperature)  
- Clear articulation of assumptions, limitations, and data gaps  
- Concise, decision-focused PDF report summarizing:
  - Modeling approach  
  - Key results and sensitivities  
  - Recommended next steps and risk-reduction priorities  

---

### Deliverable Set B — Site Concept Model and Operational Scenarios (6–12 Weeks)

**Objective:** Develop a technically consistent site-scale model suitable for engineering evaluation and scenario comparison.

#### Deliverables
- Site-scale conceptual and numerical model including:
  - Domain definition, stratigraphy, and heterogeneity representation  
  - Initial and boundary conditions consistent with site data  
- One or more well configurations and operational schedules with explicit constraint checks (pressure, rate, fracture limits)  
- Scenario comparisons evaluating alternative operational strategies  
- Decision-ready outputs including:
  - Pressure envelopes and spatial diagnostics  
  - Plume evolution and containment indicators  
  - Flow and transport metrics relevant to operations  
- Fully reproducible model package with:
  - Input files and run instructions  
  - Standardized plots and tables  
  - QA/QC summaries and run logs  

---

### Deliverable Set C — Reactive Transport, Mineralization, and Long-Term Performance (6–12 Weeks)

**Objective:** Quantify geochemical processes and long-term system behavior where permanence and transformation are critical.

#### Deliverables
- Chemistry configuration including:
  - Relevant aqueous species, minerals, and reaction pathways  
  - Reaction rate formulations and database selection  
- Coupled flow–transport–reaction simulations  
- Time-resolved partitioning of gas and solutes among:
  - Mobile/free-phase  
  - Dissolved  
  - Mineralized or immobilized fractions  
- Permanence and transformation KPIs suitable for:
  - Technical narratives  
  - Risk and uncertainty discussions  
- Explicit documentation of geochemical assumptions, uncertainties, and modeling limits  

---

### Deliverable Set D — MRV-Ready, Audit-Grade Modeling Package (Ongoing)

**Objective:** Provide a defensible, updateable modeling framework suitable for monitoring, reporting, and verification (MRV) contexts.

#### Deliverables
- Standardized QA/QC checklist applied to each model update  
- Versioned scenario library enabling consistent comparison over time  
- Traceable run logs linking inputs, solver settings, and outputs  
- Monitoring and data-value assessment identifying:
  - Measurements that most constrain pressure, plume, and transport behavior  
  - Data priorities for reducing uncertainty  
- Consistent reporting format suitable for internal governance, external review, or regulatory-style documentation  

---

## Why This Is Valuable

FLUX-GEO transforms complex subsurface problems into **transparent, testable, and repeatable modeling workflows**. By integrating **PFLOTRAN, FEHM, MODFLOW, VS2DI, and VS2DTI** within a single, coherent framework, FLUX-GEO:

- Reduces technical and decision risk  
- Improves consistency across modeling approaches and scales  
- Enables rigorous sensitivity, calibration, and uncertainty analysis  
- Produces audit-ready artifacts that withstand technical scrutiny  

The result is **faster insight, clearer uncertainty communication, and stronger technical justification** for decisions related to subsurface energy systems, environmental management, and storage applications.

---

## License

*License to be defined.*

---

## Citation

If you use **FLUX-GEO** in research, proposals, or technical studies, please cite appropriately. Citation details for FLUX-GEO will be provided in a future release.

Users are responsible for citing the underlying numerical engines (**PFLOTRAN, FEHM, MODFLOW, VS2DI, VS2DTI**) according to their respective citation guidelines and licensing requirements.
