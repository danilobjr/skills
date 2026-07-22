# My Agent Skills

[![skills.sh](https://skills.sh/b/danilobjr/skills)](https://skills.sh/danilobjr/skills)

My personal collection of reusable agent skills – compatible with any agent harness.

## Install

Run the following command on your terminal and choose which skills you want:

```sh
npx skills@latest add danilobjr/skills
```

## Skills

| Skill                                                  | Purpose                                                                                    |
| ------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| [`caveman`](./skills/caveman/SKILL.md)                 | Keeps answers terse while preserving technical substance.                                  |
| [`commit`](./skills/commit/SKILL.md)                   | Plans and prepares safe, focused Git commits.                                              |
| [`front-structure`](./skills/front-structure/SKILL.md) | Enforces frontend folders/files structure, naming, exports, and responsibility boundaries. |
| [`handoff`](./skills/handoff/SKILL.md)                 | Captures session context in to a file for another agent to continue.                       |

## Usage

Ask your agent to use an installed skill by name. For example:

```text
Apply react-conventions skill on @src/components/ui/button.tsx
```

Some tools can invoke skills automatically from their descriptions. Invocation syntax and automatic discovery vary by tool.

## License

[MIT](LICENSE) © Made with <strike>love</strike> _a keyboard_ by Danilo Barros.
