---
name: fpsot-accessibility
description: Accessibility rules for FPSOT products. Use when building or reviewing a web page, a component, a theme, a mobile app screen, a generated PDF, a chart or diagram, a video, an accessibility test, an accessibility statement or a call for tenders.
---

# FPSOT accessibility

Summary of the FPSOT accessibility specification. It adds no rules of its own.
The spec text in `spec/` wins on any difference. Each line cites its requirement ID and keeps its strength: must, should or may.

## Baseline

- Products must meet every level A and AA criterion of WCAG 2.2, and its five conformance requirements (ACC-001).
- The baseline must cover every web page, document and mobile app, including staff and admin screens (ACC-002).
- Products must also meet the AAA criteria 2.3.2, 2.4.13, 2.5.6 and 3.1.4 (ACC-003).
- Québec deployments should offer Québec Sign Language for key prerecorded audio. Others may offer it or ASL (ACC-004).
- Products must not target an older WCAG version. They may meet a later W3C Recommendation too (ACC-005).
- Own content must not be exempt. Third-party content must be listed as a gap and offered in an accessible form on request (ACC-006).

## Values (style and diagrams point here)

- Text contrast must be 4.5:1, or 3:1 for text of 24 CSS px, or 18.66 CSS px bold. It must hold in every theme, mode and state (ACC-010).
- Visible parts of controls, states, icons and chart lines must have 3:1 against adjacent colors (ACC-011).
- Color must not be the only cue. Charts and diagrams must label series or use patterns (ACC-012).
- Focus indicators must meet 2.4.13: a 2 CSS px thick line around the component and a 3:1 change. The browser outline must not be removed without such a replacement (ACC-013).
- Added content must not cover the focused component completely, and should not cover it in part (ACC-014).
- Targets must be 24 × 24 CSS px or meet a 2.5.8 exception. Touch screens and mobile apps should use 44 × 44 (ACC-015).
- Content must not flash more than three times a second, with no threshold (ACC-016).
- Motion over five seconds must have a pause control. With reduced motion on, non-essential motion must stop (ACC-017).
- Meaningful images, icons, charts and diagrams must have a text alternative. Charts and diagrams must also have a longer description, such as a data table. Decorative images must have an empty one (ACC-018).
- Content must work at 200% text, 320 CSS px width and WCAG text spacing. Images of text must not be used, except logos (ACC-019).

## Web pages and apps

- Everything must work by keyboard, with no trap and a logical focus order. Single-key shortcuts must be possible to turn off or remap (ACC-020).
- Controls must use native HTML elements, and WAI-ARIA 1.2 only where none exists. Each must expose name, role and value (ACC-021).
- Pages must have a title, landmarks, headings in order and a skip link (ACC-022).
- Fields must have visible, tied labels and state the format and whether required. Errors must name the field and problem. Forms should show an error summary (ACC-023).
- Sign-in must not rely on a memory test or puzzle alone, and must allow paste and password managers. It should offer a method without memory. Processes must not ask twice for the same data (ACC-024).
- Status messages must reach assistive technologies without moving focus. Time limits must be adjustable, with a warning and 20 seconds to extend (ACC-025).
- Help must stay in the same place, and repeated navigation must keep its order (ACC-026).
- Mobile apps must meet the baseline as WCAG2ICT applies it, clause 11 of EN 301 549 V4.1.1, the platform accessibility services, the system text size and both orientations (ACC-027).
- Drag and complex gestures must have a single-tap way. Motion input must have a control and must be possible to turn off (ACC-028).

## Documents and media

- Documents must meet the baseline as WCAG2ICT applies it, and clause 10 of EN 301 549 V4.1.1 (ACC-030).
- Generated PDF must be tagged from structured source, in the formats of DOC-042. Tagging a finished file must not be the only method. Scan-only documents must not be published (ACC-031).
- Documents must have a title, language, ordered headings, a meaningful reading order, table headers and text alternatives. Documents over 20 pages should have bookmarks (ACC-032).
- Services should publish content as web pages. They must not require a fillable PDF when a web form can do the task (ACC-033).
- Prerecorded video must have captions and, where needed, audio description. Audio must have a transcript. Live video must have captions. Captions must follow the language of the sound, and should exist in each official language of the video (ACC-034).
- Media players must work by keyboard and assistive technology, with caption and description controls. Sound must not autoplay over three seconds without a stop control (ACC-035).

## Testing

- CI must run automated accessibility checks on every change, and a new failure must block the merge. Checks should use ACT Rules engines (ACC-040).
- Conformance must not be claimed from automated results alone (ACC-041).
- Every ACC-001 and ACC-003 criterion must be checked by hand before each release that changes the UI, on a WCAG-EM 2.0 sample (ACC-042).
- Manual checks must include keyboard only, a screen reader per desktop and mobile platform, 200% text and 400% zoom, in English and French. Voice control and magnification should also be tested (ACC-043).
- Usability tests should include people with disabilities before each major release (ACC-044).
- Each test must produce a test record: product, version, date, standards, sample, result per criterion, tools and assistive technologies with versions, tester roles (ACC-045).
- Test records must be kept four years in a text format under version control, and statements and reports must cite them (ACC-046).
- Each failure must become an issue. Blocking failures must be fixed before release, and others must appear in the statement with a date (ACC-047).

## Statements and procurement

- Each deployment must publish a statement in English and French, linked from every page, the app home or settings, and each download page (ACC-050).
- The statement must give the standards and level, status, dates, gaps with workarounds and dates, assistive technologies with versions, icon meanings, two contact methods and an offer of help (ACC-051).
- Full conformance must not be claimed with a known failure. A conformance claim must hold the parts of WCAG 2.2 section 5.3.1 (ACC-052).
- Statements must be updated every 12 months and after each release that changes a gap (ACC-053).
- Each FPSOT product release must ship a conformance report against ACC-001, ACC-003 and EN 301 549 V4.1.1 (ACC-054).
- Buyers must require EN 301 549 V4.1.1 and ACC-001 to ACC-003, plus any edition a law names, such as CAN/ASC - EN 301 549:2024 (ACC-055).
- Calls for tenders must ask for a conformance report with a gap analysis, based on an ACC-045 test record. Bare claims must not be accepted (ACC-056).
- Buyers should test the leading bid before award, and should weight accessibility in scoring (ACC-057).
- Contracts must require fixes within an agreed time and a new report each major release (ACC-058).
- Projects must check each outside library, widget or theme against the baseline before adopting it, and must record and fix or report each gap (ACC-059).
