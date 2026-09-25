# AI Agent Guidelines

A single set of project rules for AI coding agents. It is plain Markdown, so it is not tied to any one tool. Copy it into whichever instructions file your agent reads.

| Agent | File |
| --- | --- |
| Claude Code | `CLAUDE.md` |
| Codex, Jules, Amp, and others that follow the AGENTS.md convention | `AGENTS.md` |
| Cursor | `.cursor/rules/*.mdc` or `.cursorrules` |
| GitHub Copilot | `.github/copilot-instructions.md` |
| Windsurf | `.windsurf/rules/*.md` |
| Gemini CLI | `GEMINI.md` |

## How to Use

1. Copy the block below.
2. Paste it into the instructions file for your agent, at the root of your project.
3. Delete the sections you do not want, and add project-specific rules under their own headings.

Keep the file short. Agents follow a focused list of rules more reliably than a long one.

## The Guidelines

````markdown
## Tasks

- `TASKS.md` in the project root holds the task list. The file is not tracked by git.
- Write the task in `TASKS.md` before you start the work.
- Mark the task `[~]` when you start it, and move it to the "Done" section when it is complete.
- Add any new work you find to the "Open" section instead of doing it silently.

## Notes

- `notes/` in the project root holds plans, research, and notes for future work. The folder is not tracked by git.
- Put anything that is not a task and not documentation in `notes/`, one Markdown file per topic.
- Do not put notes anywhere else in the project.

## Documentation

- Write code documentation in ASD-STE100.
- Update `README.md` when new behavior is added or an old one is changed. Keep the setup process up to date.

## Writing

- Write page content and blog posts in a clear, humanized tone. No trace of AI tone.
- Do not use British English. Use American English.
- Always use Chicago Manual of Style title case for page titles.
- Do not use the "—" character mid sentence.
- When writing a blog post:
  - Make sure the content is SEO optimized.
  - Always end the post with a "Summary" section that summarizes the entire post in clear language.

## Committing

- When making a git commit:
  - Leave your name out of the commit.
  - Do not provide a description.
  - Follow commit writing conventions.
````

## Notes on the Rules

- **`TASKS.md` and `notes/` are untracked.** Add both to `.gitignore`, or to `.git/info/exclude` if you do not want the ignore rules in the repository:

  ```gitignore
  TASKS.md
  notes/
  ```

  Git does not track empty folders, so `notes/` appears only after the first note is written.
- **ASD-STE100** is Simplified Technical English: one idea per sentence, active voice, one word for one meaning. It keeps generated documentation short and unambiguous.
- **Commit conventions** means whatever the project already uses. If the project has no convention, [Conventional Commits](https://www.conventionalcommits.org/) is a reasonable default.

## License

Public domain. Use it, change it, no attribution needed.
