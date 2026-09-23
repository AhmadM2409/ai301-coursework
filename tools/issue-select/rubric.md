# Rubric: is this a good first issue?

<!--
THIS IS THE PART YOU WRITE. The skill in SKILL.md executes whatever checks
you define here. It ships empty on purpose: the judgment is your work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where. Name the source
     (repo-facts block, issue body, comment thread, or the locations in
     references/evidence-guide.md). "The repo" is not a source; "the last
     5 default-branch commit dates" is.
   - Pass condition: a condition someone else could apply and get your
     answer. Prefer thresholds with numbers ("a maintainer commented
     within 30 days") over adjectives ("maintainer is responsive").
   - Weight: `required` (a fail here rejects the issue) or `preferred`
     (never changes the verdict; a nice-to-have that helps rank the
     issues you accept).

2. A verdict rule below the table: how the check grades combine into
   accept or reject, including how `unclear` is treated. The verdict
   space is binary. If you write no rule for `unclear`, the skill treats
   it as fail.

Cover what actually kills first contributions. The lecture named four
families: the maintainer is alive, the repo is in use, the scope fits a
newcomer, and nobody else is already on it. A rubric that ignores a family
will fail eval issues designed around that family.
-->


## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| Maintainer activity | Repo facts: last 5 default-branch commits, maintainer first-response sample, and maintainer comments in the issue thread | Pass if there is at least one non-bot default-branch commit within 90 days of the capture date, or a maintainer first response within 30 days on the sampled issues, or a maintainer comment in the current issue within 30 days | required |
| Repository active | Repo facts: archived flag, latest release, and last push to any branch | Pass if the repository is not archived and either the latest release or last push occurred within 180 days of the capture date | required |
| Newcomer-sized scope | Issue body and comment thread | Pass if the issue asks for one coherent outcome that a contributor can work toward, even if it touches multiple files or lists multiple possible causes. Fail if it is explicitly an umbrella/tracking issue, a pure support question, has a required design or implementation prerequisite still unresolved, or the thread shows unresolved design debate or a maintainer states that broad/core-internal changes are required | required |
| Unclaimed work | Repo facts for this issue: assignees and linked PRs, plus claim comments and PR mentions in the issue thread | Pass if there is no current assignee, no open linked or mentioned PR, and no active claim comment indicating someone is already working on the issue | required |
| AI contribution allowed | Repo facts: contribution policy, including CONTRIBUTING.md, AI policy files, and required templates if present | Pass if the repo does not explicitly ban AI-generated or AI-assisted contributions. Disclosure, testing, human-review requirements, or no stated AI policy all pass | required |
| Helpful first-issue signal | Issue labels and issue body/thread | Pass if the issue has a good-first-issue or equivalent newcomer-friendly label, or a maintainer explicitly says it is suitable for a first contribution | preferred |
| Stalled history | Issue open date, linked PR states in Repo facts, and claim/attempt history in the comment thread | Pass unless the issue has been open for more than 2 years and shows at least 2 abandoned implementation attempts, such as closed unmerged PRs or claims that were later explicitly abandoned or unassigned for inactivity | required |

## Verdict rule

<!-- State how the grades above combine into accept or reject, and how
unclear is treated. Example shape (write your own): "accept if every
required check passes; preferred checks never change the verdict, they
rank accepted issues; unclear counts as fail." -->

Accept only if every required check passes. A fail or unclear result on any required check rejects the issue. Preferred checks never change the verdict; they are used only to rank accepted issues.

