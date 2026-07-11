# My Agent Skills

Personal collection of reusable skills for Agent Skills-compatible tools.

## Skills

| Skill                                                        | Purpose                                                                                    |
| ------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| [`caveman`](.agents/skills/caveman/SKILL.md)                 | Keeps answers terse while preserving technical substance.                                  |
| [`commit`](.agents/skills/commit/SKILL.md)                   | Plans and prepares safe, focused Git commits.                                              |
| [`front-structure`](.agents/skills/front-structure/SKILL.md) | Enforces frontend folders/files structure, naming, exports, and responsibility boundaries. |
| [`handoff`](.agents/skills/handoff/SKILL.md)                 | Captures session context in to a file for another agent to continue.                       |

## Structure

Each skill lives in its own directory:

```text
.agents/skills/<skill-name>/SKILL.md
```

## Install

Just copy whatever skill content you want directly from GitHub repository and paste into the skills path supported by your tool. Or clone this repo locally and copy using terminal:

```sh
cp -R .agents/skills/caveman /path/to/your/skills/
```

Or symlink it to keep the installed skill synced with this repository:

```sh
ln -s .agents/skills/caveman /path/to/your/skills/caveman
```

**Note**: _Consult your tool's documentation for its skills path and discovery rules._

## Usage

Ask your agent to use an installed skill by name. For example:

```text
Apply front-structure skill on @src/components/ui/button.tsx
```

Some tools can invoke skills automatically from their descriptions. Invocation syntax and automatic discovery vary by tool.

## License

[MIT](LICENSE) © Made with <strike>love</strike> _a keyboard_ by Danilo Barros.
