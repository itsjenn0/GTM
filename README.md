# GTM Skills

A collection of [Claude Code](https://claude.ai/claude-code) custom slash commands for Go-To-Market operations.

## Skills

### `/update-weekly-tasks`

Reads a Notion progress-tracking page and auto-generates a weekly to-do checklist grouped by date and assignee.

**What it does:**
- Parses each channel/section on the page to extract the owner and their plan
- Generates daily checkbox tasks (Mon–Sat) based on plan content
- Replaces the checklist section on the Notion page with the updated version

**Usage:**
1. Copy `.claude/commands/update-weekly-tasks.md` into your project's `.claude/commands/` directory
2. In Claude Code, type `/update-weekly-tasks`
3. Provide your Notion page ID when prompted

**Page structure requirements:**
- Channel sections as toggle headings with `@mention` assignees
- A "计划" (Plan) toggle inside each section describing daily tasks
- A "每日任务清单" (Daily Task Checklist) section at the bottom for output

## Setup

```bash
# Clone into your project
git clone https://github.com/itsjenn0/GTM.git

# Or copy the skill you need
cp GTM/.claude/commands/update-weekly-tasks.md your-project/.claude/commands/
```

## Requirements

- [Claude Code](https://claude.ai/claude-code) CLI
- Notion MCP integration enabled in Claude Code

## License

MIT
