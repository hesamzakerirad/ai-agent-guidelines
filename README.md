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

* `TASKS.md` in the project root holds the task list. The file is not tracked by Git.
* Write the task in `TASKS.md` before starting the work.
* Add new tasks to the "Open" section using `[ ]`.
* Change the task to `[~]` immediately before starting work.
* When the task is complete, move it to the "Done" section and mark it `[x]`.
* Do not mark a task as done until the requested work is complete and verified.
* Add newly discovered work to the "Open" section instead of doing it silently.
* If newly discovered work is required to complete the current task, add it as a subtask of the current task.
* Do not modify files or behavior that are unrelated to the current task.

## Notes

* `notes/` in the project root holds plans, research, decisions, and notes for future work. The folder is not tracked by Git.
* Use one Markdown file per topic.
* Do not put project notes anywhere else.

## Documentation

* Write code comments and technical documentation in ASD-STE100 Simplified Technical English where practical.
* Update `README.md` when new behavior is added or existing behavior is changed.
* Keep the setup and usage instructions in `README.md` up to date.
* Do not document behavior that does not exist.

## Writing

* Write page content and blog posts in a clear, natural, human tone.
* Avoid generic AI phrasing, filler, unnecessary repetition, and exaggerated claims.
* Do not mention AI unless the content specifically requires it.
* Use American English.
* Always use Chicago Manual of Style title case for page titles.
* Do not use the `—` character in sentences.

### Blog Posts

* Optimize content for search intent, semantic relevance, readability, useful headings, natural keyword usage, and appropriate metadata.
* Do not use keyword stuffing or sacrifice readability for SEO.
* Always end the post with a `Summary` section that summarizes the entire post in clear language.

## Committing

When making a Git commit:

* Use a concise imperative commit subject.
* Follow conventional commit-writing practices used by the project.
* Do not add a commit body.
* Do not include your name or the agent name in the commit message.
* Do not add a `Co-authored-by` trailer.

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
