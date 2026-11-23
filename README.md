# Tab Content Studio

A Claude Code plugin that supports the full content-development workflow for **Tab**, from discovering an idea to assembling and reviewing a complete episode.

## Skills

The plugin contains seven focused Skills:

| Skill | Responsibility |
|---|---|
| **Idea Development** | Discover, compare, define, and approve playlist or standalone episode ideas. |
| **Content Connection** | Maintain educational and narrative continuity across playlist episodes. |
| **Episode Blueprint** | Define the episode's high-level internal structure and section order. |
| **Content Development & Research** | Verify technical claims and discover relevant knowledge on demand. |
| **Storytelling** | Design the narrative, explanation flow, examples, analogies, character interaction, dialogue, and educational Episode Summary. |
| **Hook Writing** | Develop the Intro Sketch, Outro Hook, and the flexible-but-required Tab entry and closing elements. |
| **Episode Development** | Assemble approved components into a complete script and perform the holistic final editorial review. |

## Working Principles

- **Shared project context:** Information and decisions supplied anywhere in the Tab project are available to the relevant Skills. Do not ask the creator to repeat information that is already available.
- **Clear ownership:** Each Skill owns its specialist decisions and respects the boundaries of the other Skills.
- **Creator approval:** The creator retains authority over creative direction, scope, and other decisions that require approval.
- **Technical accuracy:** Research verifies important technical claims and resolves genuine uncertainty. It is on-demand, not a mandatory research pass for every episode.
- **Flexible workflow:** Start from the task and information already available. Do not force every episode through a rigid sequence or require separate handoff documents when the necessary context already exists.
- **One episode at a time:** A playlist may be planned as a whole, but each episode is developed individually.

## Important Ownership Notes

- The **Episode Summary** is an educational recap owned by **Storytelling**. Hook Writing uses it as context for the Outro Hook; Episode Development assembles it into the Outro.
- The Tab entry element at the end of the Intro Sketch and the Tab closing element at the end of the Outro are required parts of Tab's identity. Their wording may be naturally rephrased, but their presence, essential meaning, and function must not be removed or changed.
- Internal Hooks are optional. Storytelling decides whether and how they support the episode; Episode Development integrates approved ones.
- Final Review is part of **Episode Development**. It is not a separate Skill.
- Character interaction and dialogue are part of **Storytelling**. They are not a separate Skill.

## Repository Structure

```text
.claude-plugin/
  plugin.json
skills/
  content-connection/
    SKILL.md
  content-development-research/
    SKILL.md
  episode-blueprint/
    SKILL.md
  episode-development/
    SKILL.md
  hook-writing/
    SKILL.md
  idea-development/
    SKILL.md
  storytelling/
    SKILL.md
```

Claude Code discovers Skills from the plugin's standard `skills/` directory. The manifest therefore provides plugin metadata; it does not need a manually maintained list of each Skill directory.
