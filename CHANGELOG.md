# Changelog

All notable changes to this skill are recorded here. Versions follow [Semantic Versioning](https://semver.org) and match `metadata.version` in `skills/directing-creative-work/SKILL.md`.

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
