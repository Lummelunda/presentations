# Scaleout Edge — platform presentation copy

**Status:** Working copy for Product and Engineering review before external use  
**Audience:** Defence operational sponsors, programme teams, and technical evaluators who may have limited AI expertise  
**Purpose:** Explain the operational problem, the software layer Scaleout supplies, and how a buyer could evaluate it. This is a general platform presentation, not an account-specific deployment proposal.

**Writing principle:** Start with the fielded capability and the buyer's decisions. Explain technical terms at the point where they become useful. “Tactical computer vision” names an example application area; it is not used here as a product name.

---

## Slide 1 — Cover

**Eyebrow:** PLATFORM OVERVIEW  
**Title:** Scaleout Edge: Model Operations for Fielded AI

**On-slide copy**

Keep AI models effective across distributed sites and devices. Scaleout Edge helps teams run, improve, evaluate, and manage model versions where operational data is generated, with fleet coordination in customer-controlled infrastructure.

**Purpose:** Give a non-specialist an immediate answer to what Scaleout does. “Model operations” is paired with a plain-language explanation rather than left as an unexplained category label.

**Layout idea:** Restrained cover. Large title and one two-line proposition. A simple field-site-to-control-plane motif may sit below the text; avoid a detailed architecture diagram on the cover.

## Slide 2 — The operational problem

**Eyebrow:** OPERATIONAL CHALLENGE  
**Title:** Field Conditions Change After a Model Is Deployed

**On-slide copy**

A model that performed well in testing may encounter different sensors, locations, seasons, object appearances, or tactics in use. Its performance must be checked against the task it is meant to support and improved when the evidence warrants it.

The relevant examples are often generated across sites and devices. Moving every raw feed to one centre may be impractical because of bandwidth, interrupted links, security rules, or data ownership. A separate model at every site is also hard to oversee: teams need to know which version is running, what changed, and whether a replacement is better.

**Purpose:** Establish the buyer's maintenance problem without claiming that every model always degrades or assuming a particular defence organisation's current architecture.

**Layout idea:** Two-column problem view: **conditions change in the field** and **centralising the response is difficult**. End with a short line across the bottom: “A fielded model needs a controlled way to improve.”

## Slide 3 — The requirement

**Eyebrow:** MODEL LIFECYCLE  
**Title:** A Fielded Model Needs a Maintenance Cycle

**On-slide copy**

Operating AI involves more than installing a model once. Teams need a repeatable cycle:

1. Observe how the current model performs on the mission task.
2. Select and review useful new examples.
3. Train or adapt a candidate model.
4. Compare it with the approved baseline.
5. Approve, distribute, and record the new version—or retain the baseline.

The cycle must work across the places where data is generated, while leaving the customer in control of evaluation criteria and operational approval.

**Purpose:** Define “model operations” in buyer language before introducing Scaleout's architecture. Make human evaluation and approval visible in the lifecycle.

**Layout idea:** A five-step loop, with **approval** as a distinct gate before distribution. Keep each step editable and pair it with one short verb; place the explanatory paragraph beneath the loop.

## Slide 4 — The platform

**Eyebrow:** WHAT SCALEOUT SUPPLIES  
**Title:** Scaleout Edge Coordinates the Model Lifecycle Across Sites

**On-slide copy**

Scaleout Edge is a reusable software platform for distributed model operations. Supported edge clients work with local data; the core coordinates training across participating nodes, maintains model versions, and provides APIs and configured fleet telemetry. Teams can bring a model developed in an existing ML environment and extend its lifecycle to field sites and devices.

Scaleout supplies the model operations layer. The customer and its partners define the mission task, provide or approve the sensor and compute environment, validate models for use, and retain responsibility for operational command and control.

**Purpose:** State the offer and its boundaries. A defence buyer should understand what they would acquire without mistaking Scaleout for a sensor, C2, or autonomy system supplier.

**Layout idea:** One horizontal layer diagram: **mission application and C2** above, **Scaleout Edge model operations** in the centre, **customer or partner infrastructure and sensors** below. Add a compact responsibility note beside it.

## Slide 5 — The operating loop

**Eyebrow:** HOW IT WORKS  
**Title:** From Field Evidence to an Approved Model Update

**On-slide copy**

**At the site:** An application identifies useful new examples. Reviewers can label or assess selected data locally, and a supported node trains or adapts a candidate using that site's data.

**Across sites:** When several sites participate, Scaleout's federated learning workflow distributes a common starting model, collects model updates from available nodes, and aggregates them into a candidate shared model. Raw training datasets are not routinely moved to a central location in this workflow.

**Before use:** The candidate is compared with the agreed baseline and recorded as a model version. The customer decides whether it meets the task criteria, who may approve it, where it should run, and when the previous version should be restored.

**Purpose:** Make the platform's central mechanism concrete while separating model creation from operational promotion. This should be the slide a buyer remembers.

**Layout idea:** Three connected stages—**site**, **fleet**, **approval**—with arrows labelled by what moves. Show raw data staying at the site and model updates moving toward aggregation. Make the approval gate visually unmistakable.

## Slide 6 — Architecture

**Eyebrow:** EDGE-TO-CLOUD ARCHITECTURE  
**Title:** Local Execution, Fleet Aggregation, Customer-Controlled Coordination

**On-slide copy**

**Edge clients** run with the data at sites or on supported devices. They can execute configured training or inference tasks and initiate outbound connections.

**Combiners** manage groups of participating clients and aggregate their model updates into partial models.

**The control plane** coordinates training, combines partial models, maintains model versions and session information, and exposes an API, user interface, and configured telemetry. It can be placed in the customer's chosen data centre, sovereign cloud, or isolated environment, subject to the target deployment design.

Approved models and instructions move toward the edge; model updates and configured metrics move back. Data permissions and network crossings are agreed for each deployment.

**Purpose:** Give architects a credible first map while keeping the main story legible to non-specialists. Distinguish logical tiers from the physical placement that must be designed with the customer.

**Layout idea:** Three large tiers left to right: **field sites / edge clients**, **Combiners**, **control plane**. Use two clearly labelled directional arrows. Draw the customer-controlled boundary around the chosen server-side environment rather than implying one universal placement.

## Slide 7 — Limited connectivity

**Eyebrow:** OPERATIONAL CONTINUITY  
**Title:** Local Work Can Continue When Links Are Limited

**On-slide copy**

**Connected:** Participating sites receive configured tasks and models, return model updates and telemetry, and contribute to fleet learning.

**Intermittent:** Supported local inference and site workflows continue. Synchronisation and training participation depend on the available link and the deployment configuration.

**Disconnected:** An installed model can continue to run locally while its device has the required power and compute. Cross-site aggregation and central visibility wait for communication to return. Local selection, review, or training may continue where the application and site configuration support them.

An evaluation should interrupt the link deliberately and check what keeps working, what is held locally, and how the system reconciles after reconnection.

**Purpose:** Explain the defence-relevant value of local operation without suggesting that every fleet function remains available offline.

**Layout idea:** A three-state comparison—**connected**, **intermittent**, **disconnected**—with the same three rows in each state: local operation, fleet coordination, and visibility. Put the proposed link-interruption test in a small bottom band.

## Slide 8 — Governance

**Eyebrow:** CONTROL AND ASSURANCE  
**Title:** Every Model Change Needs Evidence and Authority

**On-slide copy**

A candidate model is not an automatic operational replacement. Programme teams need to know which version ran where, what training session produced a candidate, which participants contributed, and how it performed against agreed test data. They also need a named authority to approve deployment and a way to return to the previous approved version when required.

Scaleout Edge provides model versioning, session records, and telemetry that support this review. Evaluation workflows, access controls, evidence exports, and release procedures should be checked against the specific software version and the customer's assurance requirements. Model updates and metrics may themselves be sensitive even when raw training data remains local.

**Purpose:** Show that the value is governed improvement, not uncontrolled adaptation. Introduce assurance and security as concrete buyer tasks without claiming automatic accreditation or guaranteed privacy.

**Layout idea:** A candidate-to-approved gate. Put **evidence**, **decision authority**, and **release / restore** as three checks around the gate. Keep release-dependent controls in a small, plainly worded note.

## Slide 9 — Integration and responsibility

**Eyebrow:** FIT WITH EXISTING SYSTEMS  
**Title:** Extend Existing Models and Mission Systems to the Edge

**On-slide copy**

Scaleout Edge can connect to existing model-development tools through SDKs and APIs. A deployment can use customer models or agreed reference starting points, with workloads packaged for supported nodes. The selected mission application determines which sensor feeds, edge hardware, user interfaces, and operational outputs need integration.

Scaleout manages the model lifecycle layer. The customer and integration partners control the mission requirements, source data, operational displays and C2 environment, security boundary, and approval of models for use. Interfaces to any named system must be tested in the target configuration; integration is part of the scope, not assumed to be automatic.

**Purpose:** Address the build-versus-buy and integration questions faced by programme teams and primes. Reinforce Scaleout's role as a supplier within an existing system.

**Layout idea:** Two-column responsibility map, **Scaleout software** and **customer / partner systems**, joined by a narrow **agreed interfaces** column. Use a few concrete examples rather than a long list of logos or standards.

## Slide 10 — Application example

**Eyebrow:** MISSION APPLICATION EXAMPLE  
**Title:** Tactical Computer Vision: Keeping Detection Models Current

**On-slide copy**

Consider a counter-UAS or ISR task using an agreed video feed. A field site runs a selected detection model, retains relevant imagery locally, and lets reviewers select and label examples from changed operating conditions. A Vision Ground Node can support local inference, training, and comparison of a candidate against the current model. Where several sites participate, their model updates can contribute to a shared candidate for further evaluation.

An Edge AI Companion may extend inference onto a supported drone, vehicle, or embedded device when the mission needs onboard processing. Its hardware fit and integration require separate validation. The customer chooses the task, performance measures, operational display, and authority for model use.

**Purpose:** Make the horizontal platform tangible in the defence application area that currently has the clearest product path, without presenting it as the whole platform or using an internal product name.

**Layout idea:** A single annotated operating scene: **sensor feed → Ground Node workflow → approved model → operational system**. Show optional onboard inference as a branch, not a required component.

## Slide 11 — Evaluation path

**Eyebrow:** PATH TO EVALUATION  
**Title:** Prove the Model Lifecycle Against One Mission Task

**On-slide copy**

Begin with one task, one baseline model, and a deployment boundary the customer can approve. Agree the sensor feed, sites and hardware, data permissions, integration points, success measures, and people authorised to review model outputs.

Test the full cycle: run the baseline, collect selected field examples, produce a candidate, compare it with the baseline, inspect the model record, and exercise the release decision. Interrupt the link to check local continuity and recovery. Add a second site only if cross-site learning is needed to answer the capability question.

The decision is whether the task improves enough, under acceptable integration and security conditions, to justify a larger trial or production design. The scope, maturity, support terms, and remaining engineering work should be explicit before that decision.

**Purpose:** End with a concrete next buyer decision rather than a generic request for a meeting. Keep the evaluation bounded and honest about component maturity.

**Layout idea:** Four-step evaluation path: **define baseline → test local cycle → test architecture → decide**. Place the decision criteria directly below the steps.

---

## Source and claim notes for the copy review

- **Positioning and audience:** `Marketing Strategy 2026.md`, especially sections 3–6; `GTM Strategy.docx.md`, especially the ready-customer profile.
- **Platform/application distinction and ownership:** `Product Strategy.docx.md`, sections 1–3 and 7.
- **Architecture and mechanics:** `Scaleout Edge Technical Brief.md`; verify release-specific details against current product documentation before publication.
- **Maturity:** `Scaleout Edge Platform - Product Roadmap.docx.md` and `Tactical CV Network - Product Roadmap.docx.md`. The core, vision workflows, Companion, governance functions, and security controls do not all have the same maturity.
- **Claim discipline:** The newer Marketing Strategy governs external wording where an older technical overview makes broader claims. In particular, federated learning does not guarantee privacy; model updates and telemetry require their own boundary assessment. Avoid unqualified claims of automatic accreditation, guaranteed offline synchronisation, or universally supported device integration.
