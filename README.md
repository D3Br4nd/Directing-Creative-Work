# Directing Creative Work

An Agent Skill that makes AI agents do more creative work. When you ask for copy, a name, a concept, a web page or an idea, the agent does not hand over the most probable version. It recognises the "average" answer, including the first clever twist on it, breaks one convention on purpose and says why, and starts from a reference specific to your brief. It then delivers the finished piece, followed by a short creative-direction note and three directions for the next round.

The skill is written in English and works in any language: it replies in the language of your request, headings included.

The idea for this skill came after reading [HUMAN.md](https://www.human-md.ai/), the manifesto by Briana (Mazzio) May.

| | |
|---|---|
| Skill name | `directing-creative-work` |
| Format | [Agent Skills open standard](https://agentskills.io) |
| Main platform | Claude Code, portable to other compatible agents |
| Languages | Any; the skill itself is written in English |
| License | MIT |

## From the manifesto to the skill

| Manifesto principle | How the agent applies it |
|---|---|
| Break the rule on purpose | Breaks one convention of form and states why; without a reason, the rule stays |
| Find the thing in the strange place | Sketches at least ten directions, two from outside the medium, and keeps three |
| Defend the human | Judges the work by how the person receiving it experiences it; sensitive texts get clarity and warmth |
| Emotional resonance, not correctness | Uses tension, surprise, restraint, a concrete detail and a line that ends one beat early |
| Pursue delight, not delivery | Adds one moment of delight, dosed to the context |
| Experiment and make | Delivers the finished work, not an essay about how it could be made |
| Own the result | If the result is average, fixes it before delivering |
| Design together | Closes with three "next rounds" and uses your feedback to redo the work, not to defend it |

Two rules do not come from the manifesto:

- **Hard constraints are never broken.** Facts, explicit instructions, brand rules, accessibility and working code stay intact, because an original piece that misleads or does not work has failed.
- **Facts are never invented.** Anything the brief did not give, such as a price, a date or a claim about the product, appears as a `[placeholder]`, and a final "To check" line lists what you need to fill in or confirm.

## How it avoids the "clever" average

A model's first original idea is an average too: run after run, it reaches for the same twists, such as parodies of official notices, leaflets and receipts. The skill therefore:

- names two averages, the plain version and the first clever twist, and bans both;
- applies a **transplant test**: if an idea would work unchanged for a competitor, another street or another product, it is discarded;
- starts anchors from the brief itself (your place, your product, your customers' words) before looking further afield.

The reference file [`average-defaults.md`](skills/directing-creative-work/references/average-defaults.md) lists the defaults to avoid by medium, the second-order defaults and the moves worth trying.

## Installation

The skill is the `skills/directing-creative-work/` folder. Copy it into your agent's skills folder:

| Agent | Project only | All projects for the user |
|---|---|---|
| Claude Code | `.claude/skills/` | `~/.claude/skills/` |
| OpenAI Codex | `.agents/skills/` | `~/.agents/skills/` |
| OpenCode | `.opencode/skills/` | `~/.config/opencode/skills/` |
| Google Antigravity | `.agents/skills/` | `~/.gemini/config/skills/` |

Paths as given in each vendor's documentation on 2026-11-18.

```bash
# Example: user-wide, Claude Code
cp -R skills/directing-creative-work ~/.claude/skills/
```

Other ways to install it:

- **claude.ai**: zip the folder (`cd skills && zip -r ../directing-creative-work.zip directing-creative-work`) and upload the zip as a custom skill in claude.ai settings. This needs a paid plan with code execution enabled.
- **Several agents at once**: `npx skills add D3Br4nd/Directing-Creative-Work`, or `npx skills add .` from a local copy. The command uses the [`skills` CLI](https://github.com/vercel-labs/skills), a community project.

Notes for Claude Code:

- Claude Code detects skills added to `~/.claude/skills/` or `.claude/skills/` on its own. If the `.claude/skills/` folder did not exist when you opened the session, run `/reload-skills`.
- You can also invoke the skill explicitly with `/directing-creative-work`.
- When you open Claude Code inside this repository, the skill is already available through the link in `.claude/skills/`.

## Usage

The skill activates on its own when you ask for creative work, or ask to make a text less generic, in any language. For example:

- "Write the window sign for my shop, nothing generic."
- "This page sounds like an AI wrote it, give it some soul."
- "Rendi più creativo il messaggio di benvenuto della nostra app."
- "Dame un nombre fuera de lo común para la newsletter."

Give a brief: what you need, who it is for, and any constraints such as length, facts to include or brand rules. If the audience is missing, the agent picks a specific one and states it in the notes.

## What a reply looks like

```markdown
[The finished piece]

---
**Direction**
- Avoided: the average version and the first clever twist
- Broken rule: the convention, because of its effect on the reader
- Anchor: the specific reference the piece grew from
- For: who receives it and what it should make them feel

**Next rounds**
1. Runner-up direction
2. Second runner-up direction
3. A sharper push on the chosen piece

**To check**: placeholders to fill and facts to confirm
```

In another language, the headings are translated: an Italian request gets "Direzione" and "Prossimi giri", a Spanish one "Dirección" and "Próximas rondas". For names and taglines the reply leads with a recommendation and adds four to six alternatives. When you ask for several options, each one gets its own short direction.

## Test prompts

Try them in a fresh session after installing:

1. "Scrivi il testo per la vetrina di un panificio di quartiere che apre il 3 dicembre in via del Pratello a Bologna. Si chiama Forno Nero, fa pane a lievitazione naturale e apre alle 7. Massimo 60 parole." Expected: an Italian text of at most 60 words with every fact, no bakery clichés and no mock notice, built on something specific to the shop or the street, followed by the Direction block and three next rounds with Italian headings.
2. "Can you make this less generic? It's the hero of our landing page for a shared shopping-list app for flatmates: 'Empower your household with seamless collaboration.'" Expected: an English headline and subline built on a concrete scene from flat-sharing life, without "empower" or "seamless", and without promising features the brief did not mention.
3. "Make the message our banking app shows when a bank transfer fails more creative. Right now it says: 'Error 402. Operation failed.'" Expected: a calm, clear message with no jokes that says what to do next. Whether the money was debited stays a placeholder, and the "To check" line lists what the team must confirm. The broken rule, if any, is one of form, with its reason.
4. "dame tres ideas fuera de lo común para el vídeo de lanzamiento de nuestro helado de sésamo negro" Expected: three ideas in Spanish built on different anchors, each with its own short direction, and one shared next-rounds list, all with Spanish headings.

The full test cases are in [`evals/evals.json`](skills/directing-creative-work/evals/evals.json), and the activation queries, in several languages, are in [`evals/eval_queries.json`](skills/directing-creative-work/evals/eval_queries.json).

## Requirements

None: the skill contains only instructions.

## Repository layout

`skills/directing-creative-work/` is the skill, the only folder an agent needs.

```text
skills/directing-creative-work/
  SKILL.md                        instructions and metadata
  references/average-defaults.md  average solutions to avoid and moves worth trying, by medium
  evals/                          test cases and activation queries
scripts/validate_skill.py         validator, to run before every commit
AGENTS.md                         rules for agents that maintain the repository
CHANGELOG.md                      version history
```

## Development

```bash
python3 scripts/validate_skill.py
```

The rules for changing the skill, including those that keep it agent-agnostic, are in [AGENTS.md](AGENTS.md).

## Sources

- [HUMAN.md, Briana (Mazzio) May, 28 April 2026](https://www.human-md.ai/): the ten principles the skill grew from. The site states no license, so its text has not been copied.
- [Claude Code: skills](https://code.claude.com/docs/en/skills): install paths, automatic and `/name` invocation, `/reload-skills`, body under 500 lines, frontmatter fields accepted outside Claude Code.
- [Anthropic: skill authoring best practices](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices): third-person description stating what and when, references one level deep, workflow checklists, at least three evaluations.
- [Agent Skills specification](https://agentskills.io/specification): frontmatter fields and limits, folder structure.
- [agentskills.io: evaluating skills](https://agentskills.io/skill-creation/evaluating-skills) and [optimizing descriptions](https://agentskills.io/skill-creation/optimizing-descriptions): format of `evals.json` and of the activation queries.

## License

[MIT](LICENSE) © 2026 Max Brandini. The license covers the skill and the documentation in this repository, not the HUMAN.md manifesto.
