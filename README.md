# Devy Interview Task

> **Practice take-home tasks, simulated by Devy AI.**
> Every task built here is a practice exercise that Devy writes for a job you are preparing for.
> It is **not** an assignment from that company, and it is not part of any hiring process there.

This repository is your workspace for Devy's technical tasks. You fork it **once**, then build each
task on its own branch in your fork. Devy finds your branch, reviews your code, and then holds a
practice tech interview with you about what you built.

Your task brief (what to build, the deadline, your branch name and your task token) is in the
**Devy app**, in the **task email** and in the **task PDF** attached to it.

---

## Contents

- [Quick start: your first task](#quick-start-your-first-task)
- [Your next tasks](#your-next-tasks)
- [The task file: `.devy/task.json`](#the-task-file-devytaskjson)
- [Rules](#rules)
- [What Devy reviews](#what-devy-reviews)
- [Troubleshooting](#troubleshooting)
- [Your submission](#your-submission): the four sections you fill in

---

## Quick start: your first task

**1. Fork this repository**

Click **Fork** (top right), keep the name **`devy-interview-task`**, and leave
**"Copy the `main` branch only"** ticked.

**2. Clone your fork and create your task branch**

Use the exact branch name from your brief (`devyai-task-` followed by 6 characters):

```bash
git clone https://github.com/<your-github-username>/devy-interview-task.git
cd devy-interview-task
git checkout -b devyai-task-<code>
```

**3. Add your task token**

Open `.devy/task.json` and paste the full task token from your brief:

```json
{
  "task_token": "<your 32-character task token>",
  "status": "in_progress"
}
```

**4. Push right away**

This lets Devy find your branch before you start building:

```bash
git add .devy/task.json
git commit -m "Start Devy task"
git push -u origin devyai-task-<code>
```

Devy checks every few minutes and shows **"We found your branch"** in the app, usually within 10 minutes.

**5. Build the task**

Work on this branch, commit as you go, and fill in the four sections under
[Your submission](#your-submission) before you finish.

**6. Hand it in**

Set the status to `done`, then commit and push:

```json
{
  "task_token": "<your 32-character task token>",
  "status": "done"
}
```

```bash
git add .devy/task.json
git commit -m "Done"
git push
```

Or tap **I'm done** in the Devy app. Either way, Devy locks the commit you handed in and starts the review.

---

## Your next tasks

Already forked this repository for an earlier task? Skip steps 1 and 2. Start the new branch from a
fresh `main`, then follow steps 3 to 6:

```bash
cd devy-interview-task
git checkout main
git pull
git checkout -b devyai-task-<new code>
```

Each task has its own branch, its own token and its own copy of this README.

---

## The task file: `.devy/task.json`

This file is how Devy recognises your work. It lives on your task branch.

| Field        | Value                                                                          |
| ------------ | ------------------------------------------------------------------------------ |
| `task_token` | The full 32-character token from your brief. It must match exactly.            |
| `status`     | `in_progress` while you work. `done` when you hand the task in.                |

- Keep it valid JSON: double quotes, no comments, no trailing commas.
- Don't rename or move it. The path must stay `.devy/task.json`.
- The token proves the branch is yours. Use each token for one task only.

---

## Rules

| Rule | Why |
| ---- | --- |
| One branch per task, with the **exact** name from your brief | Devy looks for that branch name in your fork |
| **No pull requests** to this repository | Your work stays in your fork; pull requests here are closed automatically |
| Keep your fork **public** until your report is ready | Devy reads your code from your public fork |
| Never reuse a task token | Each token belongs to one task |

Work pushed after the deadline is still accepted, marked as late.

---

## What Devy reviews

When you hand in, Devy reviews the commit you locked:

| Area | What Devy looks at |
| ---- | ------------------ |
| Correctness | Each requirement and acceptance criterion from the brief: met, partly met or missed |
| Code standards | Readability, naming, structure and error handling |
| Design and architecture | How responsibilities are split, patterns used where they help |
| Scalability and performance | Sensible data structures and the obvious bottlenecks |
| Testing | What your tests cover and whether they would catch real mistakes |
| Security | Input handling, secrets and common pitfalls |
| Fit for the role | How well the solution matches the job's stack and level |
| Documentation and Git | Your README sections and how your commits tell the story |
| AI usage | Whether what you declare matches the code you hand in |

Every finding points to a file and line in your commit.

Then Devy invites you to a practice tech interview where you walk through your code and defend your
choices. Using AI tools is fine. Say how you used them under [AI usage](#ai-usage), and be ready
to explain every part of your code.

---

## Troubleshooting

<details>
<summary><strong>Devy can't find my branch</strong></summary>

Check that:

- your fork is **public** and still named `devy-interview-task`;
- the branch name matches your brief **exactly** (`devyai-task-` plus 6 characters);
- `.devy/task.json` holds the **full** token, as valid JSON;
- you **pushed** the branch (`git push -u origin devyai-task-<code>`).

You can also paste your fork's link in the Devy app with **Paste repo link**.
</details>

<details>
<summary><strong>I forked before and my <code>main</code> is out of date</strong></summary>

On GitHub, open your fork and click **Sync fork**, or run:

```bash
git checkout main
git pull https://github.com/Dev-Jets/devy-interview-task.git main
git push
```
</details>

<details>
<summary><strong>I missed the deadline</strong></summary>

Push your work anyway and set `"status": "done"`. It is still reviewed, marked as late.
</details>

<details>
<summary><strong>Can I delete my fork afterwards?</strong></summary>

Yes, once your report is ready in Devy.
</details>

Any other question about your task: ask Devy in the app.

---

# Your submission

Fill in the four sections below on your task branch. Devy reads them during the review, so keep
the headings exactly as they are. Replace the comments with your own text.

## Approach

<!--
How you solved the task:
- the overall design and how the code is organised (main folders and files)
- the key decisions and why you made them
-->

## Trade-offs

<!--
What you chose not to do, and why.
What you would improve or add with more time.
Any known limitations or bugs.
-->

## AI usage

<!--
Which AI tools you used (if any), and for what: e.g. "Copilot for boilerplate, ChatGPT to compare two
caching approaches". Write "None" if you didn't use any. You will be asked about your code either way.
-->

## How to run

<!--
Exact commands to install, run and test your solution, e.g.:

    npm install
    npm start
    npm test

Mention the language/runtime versions you used and any environment variables needed.
-->
