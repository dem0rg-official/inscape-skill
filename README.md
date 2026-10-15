# Inscape — Claude Code Skill

**Inscape** is a [Claude Code](https://claude.com/claude-code) skill that helps you
reply to a message or formulate your position in a conflict without getting swept
up in emotions.

The name blends *Insight* + *Landscape/Scope*: the inner landscape of a situation,
a panoramic look at a problem from the inside. Inscape gives you that panorama,
then hands back words you can actually send.

## What it does

- Reads a chat/messenger/email correspondence file (or a situation described in
  your own words).
- Optionally asks for your **goal** (make peace, get them to back off, settle the
  practical matter, or voice dissatisfaction).
- Produces **1–3 reply options**, 1–2 sentences each, in the tone you choose.
- Can give a short **situation breakdown** (what's really going on, what the other
  person actually wants, hidden catches, what not to do) when you ask for
  "разбери ситуацию" / "break down the situation".

## Tones

| Tone | Feel |
|---|---|
| `calm` (default) | level, uncolored, no emotional loading |
| `warm` | friendly, cares about preserving the relationship |
| `humor` | irony and light sarcasm; never attacks the person |
| `harsh` | firm, no softening; reinforces a boundary without insults |
| `cold` | distance and dryness |
| `light` | breezy, as if nothing is happening |
| `blunt` | short and to the facts |

## Install

```bash
ln -s /path/to/inscape ~/.claude/skills/inscape
```

or copy the `inscape/` folder into `<your-project>/.claude/skills/`.

Restart Claude Code afterwards.

## Usage

Just paste a correspondence or describe the situation — the skill triggers on its
own. Or invoke it explicitly:

```
/inscape path/to/chat.txt get them to back off harsh
```

Arguments: `<correspondence file or situation description> [goal] [tone]`.
Tone defaults to `calm`; if the goal is missing, Inscape asks exactly one
clarifying question.

## Development

`evals/` contains test scenarios (chat fixtures + expectations) used to evaluate
the skill's behavior.
