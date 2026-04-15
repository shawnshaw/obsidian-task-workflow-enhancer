# Task Workflow Enhancer

A comprehensive task management plugin for Obsidian with **inbox triage**, **subtasks**, **project views**, **weekly reports**, and **archive workflows**.

## Features

### Workspace Views

- **Today Panel**: Unified task workspace with tabs (Today / Tomorrow / Weekly / Projects)
- **Project Panel**: Browse and manage all tasks by project tag (`#P/project-tag`)
- **Time Scoping**: Filter tasks by today, tomorrow, this week, this month, overdue, or all
- **Folder Scoping**: Filter by all tasks, today's tasks, blocked, waiting, done, or archived

### Task Operations

- **Triage**: Quick-tag tasks with `#daily`, `#weekly`, `#WAIT`, or `#BLOCKED`
- **Time Blocking**: Inline time range picker (e.g., `09:00 - 09:15`)
- **Date Scheduling**: Attach `⏳ scheduled` and `📅 due` dates
- **Project Tags**: Organize tasks by `#P/project-tag`
- **Complexity Tags**: Classify tasks as `#C1` (quick) through `#C5` (epic)

### Subtasks

- **Rich Subtasks**: Embed structured subtasks in task notes
- **Subtask Metadata**: Time ranges, scheduled/due dates, workflow tags, owner, confirm-by, ETA
- **Validation**: WAIT/BLOCKED subtasks require owner + item; WAIT requires confirm-by; BLOCKED requires ETA
- **Subtask Archive**: Archive completed subtasks to knowledge or evidence folders

### Reports & Workflows

- **Weekly Report**: Auto-generate weekly summary (completed, in-progress, waiting, blocked, next week)
- **Task Digest**: One-click weekly report from any task file
- **Archive System**: Archive completed tasks to `_archives/tasks/knowledge` or `_archives/tasks/evidence`
- **Data Source Tabs**: Configure multiple inbox sources (default inbox + custom workspace files)

### Inline Editor Actions

Tasks in the editor get inline action buttons:

| Icon | Action |
|------|--------|
| ⏰ | Insert time range |
| ✓ | Triage task |
| 📅 | Set dates |
| 📁 | Set project tag |

### Code Block Integration

Render the task workspace inside any note:

~~~markdown
```task-workflow
view: today
```
~~~

## Workflow Tags

| Tag | Meaning | Required Fields |
|-----|---------|----------------|
| `#daily` | Do today | — |
| `#weekly` | This week | — |
| `#WAIT` | Waiting for someone | owner + item + confirm-by |
| `#BLOCKED` | Blocked | owner + item + ETA |

## Complexity Tags

| Tag | Meaning | Time Estimate |
|-----|---------|---------------|
| `#C1` | Quick win | < 30 min |
| `#C2` | Short session | 30 min – 2h |
| `#C3` | Focused work | 2h – 1 day |
| `#C4` | Needs breakdown | 1 – 3 days |
| `#C5` | Epic | Multi-day |

## Setup

1. Enable in **Settings → Community Plugins**
2. Configure data sources in **Settings → Task Workflow Enhancer**:
   - **Inbox Path**: Default `📥 任务收件箱.md`
   - **Archive Root**: Default `_archives/tasks`
   - **Workspace Root**: Default `_system/task-workflow/workspaces`

## Screenshots

*(Add screenshots here: today panel, project view, editor inline actions)*

## Changelog

See `versions.json` for full version history.

## License

MIT
