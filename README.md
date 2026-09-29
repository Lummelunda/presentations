# Presentation system

This folder holds the reusable instructions for turning Scaleout source material into presentations. The **copy workflow** governs the story and wording; the **style guide** governs the visual treatment. Keep them separate so a change to a deck's content does not silently change the presentation style.

## Files

| File | Role |
| --- | --- |
| [Slide-copy workflow prompt](scaleout-slide-copy-workflow-prompt.md) | Reusable prompts for reviewing source material, agreeing an outline, writing slide-by-slide copy, and preparing a clean handoff to a slide-generation tool. |
| [Presentation style guide](scaleout-presentation-style-guide-v0.1.md) | Starting rules for colour, Inter typography, headers, layouts, diagrams, and claim presentation. Based on the newer deck style. |
| [Platform copy example](examples/scaleout-edge-platform-deck-copy-v1.md) | Worked example of an 11-slide Scaleout Edge platform copy master. It includes on-slide copy plus internal purpose and layout notes. |

## Workflow

1. **Gather sources and fill in the brief.** Attach the relevant strategy, product, and technical material. State the audience, presentation purpose, buyer decision, approximate length, and any claim or disclosure constraints.
2. **Agree the outline.** Use **Prompt A** in the slide-copy workflow. Review the proposed story, slide purposes, evidence gaps, and what belongs in an appendix before requesting full copy.
3. **Write and review the copy master.** Use **Prompt B** with the approved outline. Review the slide text and the internal purpose, layout, and source notes. Check maturity, privacy, security, integration, and customer-responsibility claims with the relevant owners.
4. **Prepare the slide-generation input.** Use **Prompt C** to remove internal notes and produce only eyebrows, titles, on-slide text, and layout instructions. Give that output and the style guide to the presentation tool. Attach an approved reference deck when possible.
5. **Inspect the finished deck.** Check text fit, diagram meaning, factual qualifications, logo use, and whether the deck reads without a presenter. Revise the copy or guide if the generated slides expose a recurring problem.

## How the example fits

The platform copy in `examples/` is a **working copy master**, illustrating the output of the outline-and-copy stages. Its **Purpose**, **Layout idea**, and **Source and claim notes** sections guide review; they are not text to place on slides. A slide-generation tool should receive a clean export made with Prompt C.

## Versioning

The style guide is deliberately marked **v0.1**. Update it when a visual rule has been tested and approved for reuse. Keep presentation-specific content, evidence, and layouts in the individual copy master rather than turning one deck's choices into a rule for every deck.
