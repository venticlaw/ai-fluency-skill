# ai-fluency

A Claude Code plugin that applies Anthropic's **4D AI Fluency Framework** — *Delegation, Description, Discernment, Diligence* — silently in the background to produce sharper, more trustworthy outputs.

Based on the framework by Prof. Rick Dakan (Ringling College) and Prof. Joseph Feller (University College Cork), taught in [Anthropic's AI Fluency: Frameworks & Foundations](https://anthropic.skilljar.com/ai-fluency-framework-foundations) course.

## What it does

When invoked, Claude runs an internal loop on any substantive creative, analytical, or decision-shaping task:

- **Delegation** — restates the goal in one sentence; splits work into *human-judgment-only*, *AI-leverageable*, and *must-verify* buckets; names the single constraint that would kill the output.
- **Description** — writes the spec (target audience, shape, anti-goals, voice) before generating the deliverable.
- **Discernment** — scores the draft against 3–5 explicit criteria, finds the weakest line, asks "am I confident, or performing confidence?"
- **Diligence** — verifies load-bearing claims or marks them `[unverified]`, flags uncertainty precisely, takes ownership.

It is designed **not** to be narrated at the user. The framework is overhead; the output is the product. For trivial requests, the skill explicitly tells Claude to skip the frame.

## Contents

```
.claude-plugin/
  plugin.json           # plugin manifest
  marketplace.json      # marketplace manifest (self-hosted install)
skills/
  ai-fluency/
    SKILL.md            # the skill
```

## Install

### Via the marketplace (recommended)

```
/plugin marketplace add venticlaw/ai-fluency-skill
/plugin install ai-fluency@venticlaw-marketplace
```

### Manual (user-level skill, no plugin)

```bash
mkdir -p ~/.claude/skills/ai-fluency
curl -fsSL https://raw.githubusercontent.com/venticlaw/ai-fluency-skill/main/skills/ai-fluency/SKILL.md \
  -o ~/.claude/skills/ai-fluency/SKILL.md
```

Restart Claude Code after installing.

## Use

- Invoke explicitly: `/ai-fluency:ai-fluency` (when installed as a plugin) or `/ai-fluency` (when installed as a user skill)
- Auto-apply: Claude reaches for the skill when the task description matches — substantive writing, research, planning, strategic work, non-trivial code.

## When to skip it

The skill itself says so: don't spec a one-line answer, don't pre-structure a trivial lookup, don't bureaucratize brainstorming. The framework serves the output — if applying it makes the output worse, you're using it wrong.

## Verify the plugin locally

```bash
claude plugin validate .
```

## Credits

- Framework: Rick Dakan & Joseph Feller — [aifluencyframework.org](https://aifluencyframework.org/)
- Practical summary: [Ringling College AI LibGuide](https://ringling.libguides.com/ai/framework)
- Course: [Anthropic Academy](https://anthropic.skilljar.com/ai-fluency-framework-foundations)

## License

MIT — see `LICENSE`.
