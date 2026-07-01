# Design notes

This file records deliberate Wayfinder design decisions once visual
customization begins. It intentionally contains no new styling direction yet.

## Current baseline

- The inherited visual behavior is the known-good baseline.
- Structural cleanup must not alter the generated CSS.
- Existing color schemes, feature toggles, and plugin compatibility remain
  available until individually reviewed.

## Decision template

For each future decision, record:

- Date and scope
- Goal
- Chosen approach
- Alternatives considered
- Affected tokens or source modules
- Light, dark, desktop, and mobile verification
- Accessibility considerations

## Open questions

- What should Wayfinder optimize for in the owner's daily workflow?
- Which inherited color schemes and optional features are actually used?
- Which visual concepts should become shared tokens before component work?
- What compatibility baseline should be tested after larger changes?
