# Changelog

All notable changes to this skill are recorded here. Versions follow [Semantic Versioning](https://semver.org) and match `metadata.version` in `skills/directing-creative-work/SKILL.md`.

## [0.6.0] - 2026-11-20

- Shortened the notes that follow a piece to at most three brief items: the obvious version passed over, two other directions and essential checks. A fuller rationale is available on request.
- Replaced the worked example of an anchor with one from a different domain, and added the best-known fact about a location to the second-order defaults. A place's general reputation is no longer suggested as a source of anchors.
- The piece now includes every fact the user supplied for it, and public copy grounds claims about how the business works in the brief.
- Functional copy now keeps an unconfirmed state, such as whether a failed transfer moved money, as a placeholder inside the customer copy rather than as a caveat in the notes.
- Added an evaluation for an open homepage brief and tightened the assertions on note length and unconfirmed payment status.

## [0.5.0] - 2026-11-18

- Made the requested deliverable, language, count and edit scope take precedence over the default creative review. Short functional copy now carries only essential editorial checks.
- Distinguished invented story details and proposed scenes from real-world claims. Missing transaction status and recovery actions require confirmation before publication.
- Replaced the fixed sketch quota with exploration proportionate to the brief. The transplant test now asks whether changing a detail would change a creative choice.
- Added regression cases for fiction, exact JSON, critique and narrow revisions. Updated the original evaluations to assess the delivered work and expanded the multilingual activation queries.
- Corrected the repository validator's handling of malformed evaluation data.

## [0.4.0] - 2026-11-18

First public release.

### Added

- The `directing-creative-work` skill: it names the average version of a piece and the first clever twist on it, sketches at least ten directions and keeps three, applies a transplant test, breaks one convention with a stated reason, and delivers the finished piece with a Direction block, three next rounds and a "To check" line.
- Rules that keep hard constraints intact and never invent facts: anything the brief did not give appears as a bracketed placeholder.
- Layouts for names and taglines (a recommendation plus four to six alternatives) and for requests with several options.
- `references/average-defaults.md`: average defaults by medium, second-order defaults, moves worth trying and places to look for an anchor.
- Replies in the user's language, with the English heading template translated.
- Six evals and twelve trigger queries in English, Italian, Spanish, German and French.
