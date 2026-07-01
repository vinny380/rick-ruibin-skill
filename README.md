# Rick Rubin

<p align="center">
  <img src="./skills/rick-rubin/assets/rick-rubin-intuition.png" alt="Rick Rubin with text about making software from intuition and taste" width="720">
</p>

Most AI work is not bad.

It is worse.

It is fine.

It passes. It compiles. It satisfies the prompt. It explains itself too much. It has no pulse.

This is a final listen before shipping.

Not a spec check.

A taste check.

> Is this alive, or merely correct?

## Use It

For the open Agent Skills ecosystem:

```bash
npx skills add <owner>/<repo>
```

For Codex local development:

```bash
mkdir -p ~/.codex/skills
ln -s "$(pwd)/skills/rick-rubin" ~/.codex/skills/rick-rubin
```

For Claude Code local development:

```bash
claude --plugin-dir .
```

Then ask for the pass:

```text
/rick-rubin judge this landing page copy.
```

In Codex, mention the skill with `$`:

```text
Use $rick-rubin to judge this landing page copy.
```

In Claude Code marketplace installs, plugin skills are namespaced:

```text
/taste-check:rick-rubin
```

## Marketplace Shape

This repo is arranged for three paths with one canonical skill file:

- `skills/rick-rubin/SKILL.md` for skills.sh and direct Agent Skills installs
- `.claude-plugin/marketplace.json` plus `.claude-plugin/plugin.json` for Claude Code marketplace distribution
- `.agents/plugins/marketplace.json` plus `.codex-plugin/plugin.json` for Codex plugin marketplace distribution

Claude and Codex install the repo root as the `taste-check` plugin package. The skill itself lives once, under `skills/rick-rubin/`.

## The Point

Use `/rick-rubin` in Claude Code, or `$rick-rubin` in Codex, when the work needs judgment.

Not more features.

Not more polish.

Judgment.

- Is the interface pulling you in?
- Is the copy saying one true thing?
- Is the code simple because it found its shape, or simple because it gave up?
- Is the feature real, or did it grow extra limbs in a meeting?
- Is the name memorable, or just available?

The skill looks at the thing itself.

It ignores the pitch.

It removes what does not belong.

It says the quiet part plainly.

## The Output

```text
Verdict: alive, flat, overbuilt, or close
Essence: what the work is really trying to be
Cut: what should be removed
One change: the highest-leverage improvement
```

That is enough.

More would be decoration.

## What This Is Not

This is not an impersonation.

No guru voice.

No costume.

No incense in the terminal.

The skill does not talk like anyone. It decides with taste.

The goal is not to sound interesting.

The goal is to make the work better.

## Example

```text
User:
Judge this feature idea:

"AI dashboard with insights, tasks, team updates, automations, integrations,
and weekly strategic recommendations."

/rick-rubin:
Verdict: overbuilt. It sounds useful, but I already want to close it.

Essence: the real product is "tell me what changed and what needs me."

Cut: dashboards, weekly strategy, vague insights, generic automations.

One change: make the first version a daily operator brief:
5 changes, 3 risks, 1 thing to do now.
```

More demos live in [examples](./examples).

## Publish

Once the repo is public:

```bash
npx skills add <owner>/<repo>
```

That makes skills.sh see the repo after CLI telemetry updates.

For Claude Code:

```text
/plugin marketplace add <owner>/<repo>
/plugin install taste-check@rick-rubin-skills
```

Marketplace installs invoke the skill as:

```text
/taste-check:rick-rubin
```

For the shorter `/rick-rubin` command, install the skill directly instead:

```bash
npx skills add <owner>/<repo> -a claude-code
```

For Codex:

```bash
codex plugin marketplace add <owner>/<repo>
```

Then install `taste-check` from the `Rick Rubin Skills` marketplace.

## Launch Copy

Post this:

```text
I made a Codex/Claude skill for taste.

Most AI work does not fail because it is wrong.
It fails because it is competent-but-dead.

This skill gives the work a final listen:

Verdict.
Essence.
Cut.
One change.

Correct is the floor.
Alive is the bar.
```

Follow-up:

```text
The best AI reviewer may not ask:
"does this satisfy the prompt?"

It asks:
"do I want to keep looking at this?"

That changes the work.
```

## Files

- `skills/rick-rubin/SKILL.md` - the skill
- `skills/rick-rubin/agents/openai.yaml` - Codex skill metadata
- `skills.sh.json` - skills.sh repo page grouping
- `.claude-plugin/marketplace.json` - Claude marketplace catalog
- `.claude-plugin/plugin.json` - Claude plugin manifest
- `.agents/plugins/marketplace.json` - Codex marketplace catalog
- `.codex-plugin/plugin.json` - Codex plugin manifest
- `examples/` - before/after demos for launch posts and validation
- `skills/rick-rubin/assets/rick-rubin-intuition.png` - README and skill image

## License

MIT
