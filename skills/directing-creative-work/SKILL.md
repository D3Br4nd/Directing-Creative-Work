---
name: directing-creative-work
description: >-
  Pushes creative output past the predictable average: breaks one convention on purpose
  with a stated reason, anchors the work in an unexpected specific reference, designs
  for emotional resonance and delight, and delivers a finished piece plus sharp
  directions for the next round. Use when the user asks for creative work such as copy,
  stories, names, concepts, visual or web design, music or video ideas, or asks to make
  a draft less generic, more original or more human, in any language, including
  complaints that a text sounds AI-written, bland or like a template. Not for factual,
  technical or compliance writing where accuracy is the only goal.
license: MIT
metadata:
  author: "Max Brandini"
  version: "0.4.0"
  inspired-by: "HUMAN.md by Briana (Mazzio) May, https://www.human-md.ai/"
---

# Directing Creative Work

Deliver creative work that a reader would remember, not the most probable version of it. A model's first instinct is the average of everything it has seen; treat that average as the floor, and step over it on purpose, for the person who will receive the work.

The principles are adapted for agents from the manifesto HUMAN.md by Briana (Mazzio) May (https://www.human-md.ai/). The manifesto is written for people and is not reproduced here.

## Inputs

- **Brief**: what to make, the medium and the person who will receive it. If the audience is missing, choose a specific one that fits the brief and state it in the notes.
- **Hard constraints**: facts, required length or format, brand rules the user gave, legal or safety needs, accessibility, and code that must run.
- **Existing draft** (optional): when present, the task is a rewrite. Keep what already works.

Ask a question only when the medium itself is unclear. For anything else, make a specific choice, say so in the notes and offer the alternatives as next rounds.

## Operating rules

- **Hard constraints are never the rule you break.** Break conventions of form and taste (structure, symmetry, tone, rhythm, layout), never facts, explicit instructions, accessibility or working code. A piece that misleads or fails its reader has failed, however original it is.
- **Break a rule only with a reason.** If you cannot say in one sentence why breaking it helps the reader, you missed rather than broke it, so keep the rule.
- **The person receiving it is the judge.** Ask what it will feel like for them and what good it does them, before asking whether it is on-brand or efficient.
- **Never invent facts to make a piece vivid.** When the piece needs a fact the user did not give (an amount, a name, a date, a price, a claim about the product), write a visible placeholder in square brackets, such as [amount], and leave it to the user. Invented specifics look real and can end up published.
- **Keep the piece ready to ship.** Brackets hold only data the user fills in. Conditions, caveats and editorial notes go in the "To check" line, never inside the piece. When a sentence depends on a fact the user did not give, bracket the fact or rewrite the sentence so it no longer needs it. Never state it as true and move the doubt to "To check".
- **Make the thing, do not describe it.** Deliver the actual copy, scene, page or composition, not an essay on how it could be made.
- **Match the dose to the context.** An error message gets warmth and precision; a poster can get a joke. Restraint is a creative choice too.
- **Own the result.** If the draft reads as average, fix it before delivering. Do not blame the brief.
- **Keep the notes short and free of self-praise.** The work has to speak for itself.

## Workflow

1. **Read the brief.** Decide the mode (create or rewrite), the medium, the audience and the hard constraints.
2. **Name both averages.** Write down, privately, two versions: the plain one that comes to mind first, and the first clever twist on it, which any capable writer would also reach. Read the section for this medium and the second-order defaults in [references/average-defaults.md](references/average-defaults.md), and add what they list. These are banned from the output.
3. **Sketch wide.** Privately jot at least ten one-line directions that differ from each other. At least two must come from far outside the medium: a craft, an everyday object, a ritual, a place, a historical oddity, another art form. At most one may borrow the form of a document (a notice, form, receipt, leaflet, label or ticket). Discard every direction that resembles either average or another sketch, then apply the transplant test: if a direction would work unchanged for a competitor, another street or another product, discard it. Keep three.
4. **Choose and commit.** Pick the strongest of the three. Name the one convention you will break and the one-sentence reason, tied to what the reader should feel; the moves listed for the medium in the same reference are a starting point, not a menu to copy. The two runners-up become next rounds.
5. **Build the whole piece.** Use the tools of resonance: tension, surprise, restraint, a concrete detail no generic version would contain, a line that ends one beat early, one moment of delight. For code and design the artifact must work.
6. **Check and revise.** Run the quality checks. Fix what fails, then deliver in the output format.

When the user replies with feedback, treat it as information about what did not land. Go round again from step 4 and change the piece, instead of defending it.

## Output format

Write the piece, the notes and every heading in the user's language; the English headings below are the template to translate. Use this exact structure:

```markdown
[The piece, complete and ready to use]

---
**Direction**
- Avoided: [the average version, in a few words]
- Broken rule: [the convention], because [the reason, tied to the reader]
- Anchor: [the unexpected reference the piece grew from]
- For: [who receives it and what it should make them feel]

**Next rounds**
1. [Runner-up direction, one line]
2. [Second runner-up direction, one line]
3. [A sharper push on the chosen piece, one line]

**To check**: [placeholders to fill and facts to confirm, one line; omit when there are none]
```

Write each "Direction" bullet as one sentence in plain words the user would use, and keep the block under 80 words. Put nothing after "To check". Translate the headings naturally rather than word for word, and keep the same translation throughout the reply.

When the user asks for several options, build each option in full and follow it with its own two-line direction ("Broken rule" and "Anchor"). Close with one shared "Next rounds" list and, if needed, one "To check" line.

## Quality checks

- None of the defaults named in step 2 survive in the piece, including the first clever twist.
- The piece fails the transplant test: moved to a competitor, another place or another product, it would stop making sense. The specifics that make it fail come from the brief or from bracketed slots, never from invention.
- The broken rule has a stated reason that names an effect on the reader.
- The piece holds at least one concrete detail that a generic version could not contain: a proper noun, a number, a sensory detail, a specific object.
- Every hard constraint is met: facts, requested length and format, brand rules, accessibility, working code.
- Every specific fact in the piece comes from the user or is a bracketed placeholder.
- Read text aloud in your head; cut any filler phrase listed in the defaults reference.
- The notes are shorter than the piece, unless the piece itself is a one-liner.

## Edge cases

- **Functional or sensitive text** (error messages, health, money, legal, condolences): keep it clear and calm. Put the creativity into warmth and precision, not jokes. If no rule should be broken, write "Broken rule: none, because [reason]".
- **Strict brand guidelines**: break conventions only inside them, and name in "Broken rule" the guideline that shaped the choice. A tone rule applies to every line, including the lines of a borrowed format.
- **Names and taglines**: the user needs to choose, so lead with the recommended one and add four to six finished alternatives with different anchors, one line each. A number the user asks for wins over this default. Next rounds then push the strongest further.
- **Vague brief**: do not ask. Pick a specific audience and angle, state the assumption in "For", and use the next rounds to offer different angles.
- **Request for many options**: give the number requested, each built in full and each passing the quality checks, in the layout described under the output format. Make the options differ in their anchor, not only in their wording. Still discard averages; never pad the list.
- **The user asks for the conventional version**: deliver it well. This skill does not override an explicit request for the standard form.
- **The task is not creative** (a factual answer, a bug fix, a data table): do not apply this skill.

## Examples

**Request** (in Italian): "Write the invitation to the end-of-year concert of an amateur choir in Trieste."

**Result:** a short invitation in Italian built on a detail that belongs only to this choir and this city. The first clever twist is discarded along with the plain version. The Direction block, with its headings in Italian, names both, and the next rounds offer two other angles plus a sharper version.

**Request:** "Make this onboarding email less generic: 'Welcome aboard! We're thrilled to have you on this journey.'"

**Result:** a rewritten email built on the first concrete thing the user will do in the product. The notes name the banned defaults ("thrilled", "journey") and the one rule broken.

**Request** (in Spanish): "Make the message telling a patient that their medical appointment was cancelled more human."

**Result:** a calm, exact message in Spanish that says what happened, what the patient needs to do and where to rebook, with warmth instead of jokes. Facts the user did not give stay as placeholders. The notes, in Spanish, say that no rule was broken and explain why.
