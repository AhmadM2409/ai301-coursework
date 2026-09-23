# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

**Issue link**

https://github.com/codepath/pathreview-ai301-fa26-s1/issues/18

**Verdict output**

All three are in scope (codepath/pathreview-ai301-fa26-s1). Repo-level evidence is shared: not archived, last push 2026-09-16 (7 days ago), last 5 main commits all by collaborator Aburke225 (newest 2026-09-16), no release, and no AI policy in docs/CONTRIBUTING.md, the PR template, or README. Only one PR exists repo-wide (#74 → issue #60), so none of the three has a linked or mentioned PR, and none has an assignee or a single comment.

Ranked read-out — all three accepted

1. #18 — repo analyzer never receives a file list — Best fit: a concrete backend bug with the root cause already diagnosed (file_structure key is never set), a bounded two-file fix in agent/tools/github_tool.py + ingestion/parsers/repo_analyzer.py, and an obvious way to verify (has_tests/has_ci stop being always-False). It's exactly the "trace an issue across multiple files" practice you said you want, without architectural risk.
2. #36 — missing test for POST /reviews with no ingested documents — Squarely in your comfort zone: one test in one file (tests/unit/test_review_routes.py), API-layer, smallest effort estimate (2–3h). Ranked below #18 only because it teaches less about reading an unfamiliar codebase.
3. #12 — snapshot tests for prompt templates — Still accepted and test-focused, but the loosest of the three: you'd have to design the version-bump convention yourself, and it carries the largest effort estimate (3–5h), which cuts against your preference for a fix with clear evidence of what's wrong.

Preferred check note: all three carry good first issue + tier-1 labels from a collaborator, so that signal doesn't separate them.

One tension worth flagging: the rubric's maintainer-activity check passes on commit recency alone, and this repo has zero maintainer replies on any of these issues — in a normal repo that would be thin evidence, but it's a two-week-old classroom repo, so there's nothing to reply to yet.

```json
[
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/18",
    "checks": [
      {
        "name": "Maintainer activity",
        "grade": "pass",
        "evidence": "Newest main commit 2026-09-16 by non-bot collaborator Aburke225, 7 days before today"
      },
      {
        "name": "Repository active",
        "grade": "pass",
        "evidence": "archived: false; pushed_at 2026-09-16, within 180 days"
      },
      {
        "name": "Newcomer-sized scope",
        "grade": "pass",
        "evidence": "One outcome with a stated root cause: 'no code sets that key, so has_tests and has_ci are always False'; two named files, no design debate"
      },
      {
        "name": "Unclaimed work",
        "grade": "pass",
        "evidence": "assignees: []; 0 comments; only repo PR is #74 for issue #60"
      },
      {
        "name": "AI contribution allowed",
        "grade": "pass",
        "evidence": "No AI mention in docs/CONTRIBUTING.md, PULL_REQUEST_TEMPLATE.md, or README; silence passes"
      },
      {
        "name": "Helpful first-issue signal",
        "grade": "pass",
        "evidence": "Labels include 'good first issue' and 'tier-1'"
      },
      {
        "name": "Stalled history",
        "grade": "pass",
        "evidence": "Opened 2026-09-10 (13 days), no linked PRs, no abandoned attempts"
      }
    ],
    "verdict": "accept"
  },
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/36",
    "checks": [
      {
        "name": "Maintainer activity",
        "grade": "pass",
        "evidence": "Newest main commit 2026-09-16 by non-bot collaborator Aburke225, 7 days before today"
      },
      {
        "name": "Repository active",
        "grade": "pass",
        "evidence": "archived: false; pushed_at 2026-09-16, within 180 days"
      },
      {
        "name": "Newcomer-sized scope",
        "grade": "pass",
        "evidence": "'Add a test that verifies the endpoint returns an appropriate error rather than crashing' in tests/unit/test_review_routes.py"
      },
      {
        "name": "Unclaimed work",
        "grade": "pass",
        "evidence": "assignees: []; 0 comments; no cross-referenced PR in timeline"
      },
      {
        "name": "AI contribution allowed",
        "grade": "pass",
        "evidence": "No AI mention in docs/CONTRIBUTING.md, PULL_REQUEST_TEMPLATE.md, or README; silence passes"
      },
      {
        "name": "Helpful first-issue signal",
        "grade": "pass",
        "evidence": "Labels include 'good first issue' and 'tier-1'"
      },
      {
        "name": "Stalled history",
        "grade": "pass",
        "evidence": "Opened 2026-09-10 (13 days), never updated since, no attempts"
      }
    ],
    "verdict": "accept"
  },
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/12",
    "checks": [
      {
        "name": "Maintainer activity",
        "grade": "pass",
        "evidence": "Newest main commit 2026-09-16 by non-bot collaborator Aburke225, 7 days before today"
      },
      {
        "name": "Repository active",
        "grade": "pass",
        "evidence": "archived: false; pushed_at 2026-09-16, within 180 days"
      },
      {
        "name": "Newcomer-sized scope",
        "grade": "pass",
        "evidence": "Single outcome — 'Add snapshot tests that fail if a template's content changes without a version bump' — in tests/unit/test_prompt_templates.py; not an umbrella issue and no unresolved debate"
      },
      {
        "name": "Unclaimed work",
        "grade": "pass",
        "evidence": "assignees: []; 0 comments; no linked or mentioned PR"
      },
      {
        "name": "AI contribution allowed",
        "grade": "pass",
        "evidence": "No AI mention in docs/CONTRIBUTING.md, PULL_REQUEST_TEMPLATE.md, or README; silence passes"
      },
      {
        "name": "Helpful first-issue signal",
        "grade": "pass",
        "evidence": "Labels include 'good first issue' and 'tier-1'"
      },
      {
        "name": "Stalled history",
        "grade": "pass",
        "evidence": "Opened 2026-09-10 (13 days), no closed unmerged PRs or abandoned claims"
      }
    ],
    "verdict": "accept"
  }
]
```

---

## Eval iterations

**Run history**

`agreement: 0/0 scored items`

`agreement: 0/0 scored items`

`agreement: 16/20 scored items  (bar: 18/20: below the bar)`

`agreement: 4/4 scored items`

`agreement: 18/20 scored items  (bar: 18/20: PASS)`

The two 0/0 runs were environment/setup failures before Claude Code, Windows UTF-8 handling, and authentication were working. The first completed full grading run scored 16/20. I revised the rubric, re-ran the four disagreements with `--only`, got 4/4, and then ran the complete final evaluation, which scored 18/20.

**Issue analysis**

`issue-19` — my rubric's decision was `reject`, while the gold label was `accept`. The run failed the `Newcomer-sized scope` check. The issue describes two potential causes for the UI freeze and then lists additional suggestions involving multiprocessing, selective rewrite matching, and moving rewrite application to another thread. The rubric run interpreted that as scope that was not sufficiently bounded for a first contribution, even though the gold label treated the bug as acceptable.

**Check rationale**

`| Stalled history | Issue open date, linked PR states in Repo facts, and claim/attempt history in the comment thread | Pass unless the issue has been open for more than 2 years and shows at least 2 abandoned implementation attempts, such as closed unmerged PRs or claims that were later explicitly abandoned or unassigned for inactivity | required |`

I added this check after the first full run accepted `issue-15`, even though that issue had been open for years and had a long history of abandoned claims and closed attempts. I used both a time threshold and an attempt threshold so that an issue does not fail just because it is old; it also needs evidence that multiple contributors have already tried and failed to finish it.

**Trade-offs**

The `Stalled history` check also caused `issue-09` to be rejected in the final run even though its gold label was `accept`. The final eval reported `failed: Stalled history` for that issue. I accept that trade-off because the check is intentionally cautious about issues with a long history of abandoned implementation attempts, but it can reject an older issue that is still reasonable for a newcomer.

---

## Selection rationale

**Selection rationale**

1. Issue #18 fits my interests because it is a backend bug with a specific cause and only two relevant files. The estimated 2–4 hour effort also fits the time I have available, and it gives me practice tracing data through an unfamiliar codebase.

2. The verdict correctly identified that the repository is active, the issue is unclaimed, the scope is bounded, and there is a clear way to verify the fix because `has_tests` and `has_ci` should stop always returning `False`. Outside the rubric, I also weighed how much I could learn from the issue compared with the other accepted choices, which is why I preferred it over the smaller test-only issue.

3. I expect claiming it to be straightforward because it is currently open and the Path Review course rules allow students to work on shared issues. I will still need to follow the Unit 2 claiming process and make sure I understand the expected fix before starting work.

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.
