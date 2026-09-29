# Scaleout presentation style guide

**Version:** 0.1 — starting point for review  
**Use:** Attach this guide, the approved slide copy, and a reference deck when asking an AI tool to create a Scaleout presentation.  
**Visual reference:** `scaleout-edge-sovereign-fct-content-updated.pptx` (15-slide FCT briefing, 28 September 2026). The palette, Inter typography, header treatment, and diagram style below are drawn from that deck.

## 1. Overall character

Clear, technical, and restrained. The deck should feel suitable for a defence programme review: precise language, legible architecture, and enough detail to circulate without a presenter. Prefer whitespace, rules, and simple rectangular panels to decoration. Use diagrams to explain placement, flows, boundaries, and decisions.

Use a **16:9 widescreen** canvas. Keep a consistent header: Scaleout identity at top left, a short uppercase category eyebrow at top right, and a thin dark divider beneath. Start the main title below the divider, aligned with the content margin. Keep all text within the slide boundary; shorten a title before reducing it to an unreadable size.

## 2. Colour system

| Role | Colour | Hex | Use |
| --- | --- | --- | --- |
| Background | White | `#FFFFFF` | Default slide background |
| Main text / dark panels | Near black | `#111215` | Titles, body copy, dark headers, primary rules |
| Platform / structure | Deep blue | `#004B87` | Architecture tiers, links, section labels, information accents |
| Operational emphasis | Orange | `#FF4600` | Small rules, key warnings, decision gates, selected highlights |
| Secondary text | Slate grey | `#5A5F68` | Subtitles, qualifiers, captions |
| Panel fill | Pale grey | `#F4F5F7` | Light content areas and diagrams |
| Dividers / borders | Cool grey | `#D1D5DB` | Fine lines and quiet panel outlines |

Keep most of each slide white. Use blue and orange to direct attention, with one clear accent priority per slide. Use orange for short, bold labels or graphic accents; use near black for paragraphs. Avoid gradients, shadows, saturated background blocks, or extra accent colours unless a particular presentation has an approved reason.

## 3. Typography

Use **Inter** throughout. Use Inter ExtraBold or Bold for strong titles, Inter Semibold or Bold for labels, and Inter Regular for body text. If Inter is unavailable, use a close sans-serif fallback and keep the same hierarchy.

For a standard 13.33 × 7.5 in widescreen slide, start with these sizes and adjust proportionally if the tool uses a different physical canvas:

| Element | Starting size | Treatment |
| --- | --- | --- |
| Cover title | 34–42 pt | Bold; one or two lines |
| Slide title | 26–30 pt | Bold; ideally one line, at most two |
| Eyebrow / header | 11–12 pt | Uppercase, short |
| Body text | 14–16 pt | Regular; generous line spacing |
| Panel heading | 16–19 pt | Semibold or Bold |
| Technical label / caption | 11–13 pt | Use sparingly; never make main content this small |

Use **Title Case** for main slide titles and **ALL CAPS** for short eyebrows and diagram tier labels, matching the reference deck. Keep wording short enough to fit naturally. Do not use all caps for paragraphs.

## 4. Slide anatomy and layouts

Use a common header and margins across the deck. The reference layout places identity near the upper left, eyebrow at the upper right, a thin rule across the page, then a left-aligned title and content below. Preserve this rhythm even when the body layout changes.

Choose the layout that fits the slide's job:

- **Statement:** one clear point, short explanation, and ample whitespace.
- **Two-column explanation:** problem and implication; software and customer responsibilities; current and proposed state.
- **Three-part system:** field site, aggregation, control plane; or application, model operations, deployment scope.
- **Process:** three to five numbered stages, with a distinct evaluation or approval gate.
- **Architecture:** editable boxes, labelled arrows, and visible security or data boundaries.
- **Comparison:** a compact table or three-state view when the same criteria are compared across options.

Use rectangular panels with pale grey fills and thin borders. Dark header strips are useful for tier names or numbered sections. Vary the layouts across consecutive slides; avoid turning the whole presentation into a grid of identical cards. Aim for one main visual idea per slide.

For a send-ahead deck, moderate text is acceptable. As a starting range, keep most slides to roughly **50–100 words of on-slide copy**. A technical appendix may be denser if it remains readable at normal presentation size. Split a slide when the argument needs more room; do not shrink all body text to make it fit.

## 5. Diagrams and imagery

Make architecture and process diagrams **editable slide objects**. Label the nodes and the payload on each arrow: for example, “approved model and instructions” toward field sites, and “model updates and configured metrics” toward aggregation. Show what stays local and draw customer-controlled or security boundaries where the distinction matters.

Use blue for system structure and flow; use orange for an operational constraint, boundary crossing, or approval point. Use straight lines and simple arrows. Keep arrows consistent in direction and meaning. A diagram should be understandable without its accompanying paragraph.

Use product screenshots or approved photographs only when they provide evidence or necessary context. Prefer a clean explanatory diagram to generic military imagery. Use approved Scaleout logo assets; do not generate substitute logos or customer/partner marks.

## 6. Content and claim rules

Write for an operational sponsor first and a technical evaluator second. Begin with the mission or programme question, then explain the software. Define terms such as *model operations*, *federated learning*, and *control plane* in plain language when first used. Use familiar defence terms where accurate: **field site, mission task, deployed model, approved baseline, operational continuity, evidence, boundary, and authority to approve**.

Keep these distinctions visible:

- **Mission application:** the capability the buyer is trying to improve.
- **Model operations:** the Scaleout Edge software that runs and coordinates the model lifecycle.
- **Deployment scope:** the selected sites, devices, interfaces, data flows, and customer-controlled infrastructure.

Separate **available**, **being evaluated**, and **planned** functions. Do not imply that federated learning guarantees privacy, that every function works offline, or that a candidate model is deployed automatically. Preserve qualifications about device support, component maturity, model approval, security controls, and integration effort from the approved copy. Do not invent performance figures, customer examples, certifications, or roadmap commitments.

## 7. Paste-ready instruction for an AI presentation tool

> Create the slides from the accompanying approved copy. Follow the attached Scaleout reference deck and this style guide. Use a 16:9 canvas, Inter, a white background, near-black text (`#111215`), deep-blue structural accents (`#004B87`), restrained orange emphasis (`#FF4600`), pale-grey panels (`#F4F5F7`), and cool-grey dividers (`#D1D5DB`). Keep the Scaleout identity at top left, a short uppercase eyebrow at top right, and a thin divider below the header. Use varied, simple layouts and editable diagrams. Preserve all factual qualifications in the copy. Shorten or split content only when necessary for readability; do not add facts, logos, claims, or decorative imagery. Ensure every title and text box fits within the slide.

## Decisions to revisit in version 0.2

1. Confirm the approved logo/wordmark file and the exact header lock-up.
2. Decide whether orange remains the primary operational accent across all Scaleout decks or whether another approved palette is needed for specific audiences.
3. Add three approved reference slides: cover, explanatory content, and architecture.
4. Agree minimum font sizes after testing one deck in Google Slides and PowerPoint.
