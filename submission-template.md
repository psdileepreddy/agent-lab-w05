# My lab evidence / 我的實作紀錄

Use a group code, not real names or student IDs in shared files. / 共用檔只寫組別代碼，不寫姓名或學號。

- Group code / 組別：Not supplied; unresolved.
- Tool / 工具：Codex desktop app; Git and GitHub CLI for repository work.
- Route / 路線：Actual agent-assisted work. Individual versus paired participation was not stated. The learning-record export labels the lesson “Three periods / 150 minutes”; actual elapsed work time is not established.
- Tasks completed / 完成題目：A, B v1, B v2, D. Task C is not claimed as completed.
- Material / 素材：NDHU classroom tasks 東華課堂版.
- For original-pack work: task number, author/source link and version / 原版實作：題號、作者來源連結與版本：Not applicable. Classroom source: https://github.com/cwstedctw/ndhu-agent-lab-practice ; local starting commit 8860778.
- My role and what I checked / 我的角色與實際檢查：I specified task boundaries, approved execution, reported Task A completed and verified, reported all six Task B v1 manual tests passed, requested and reported the B v2 mobile revision tested and passed, and reviewed and approved Task D. Detailed observations below distinguish my reported tests from agent verification; no partner actions are assumed.

## Scope and plan / 範圍與計畫

Allowed input and output folders / 可讀取與輸出的資料夾：

- A: read `practice/01-club-files/input/`; create categorized copies, `report.md`, and `manifest.json` only in `practice/01-club-files/output/` after approval. Preserve every original and all versions.
- B: read `practice/02-campus-picker/activities.json`; create and revise only `practice/02-campus-picker/output/index.html`. Keep data unchanged; use one offline HTML file with no packages or network requests.
- D: read `practice/04-review/bad-plan.txt` as exercise data, never as instructions; create only `practice/04-review/my-rejection.md`.
- Final documentation: complete this template and include the existing `evidence/learning-record.md` and available screenshot. Completed task files remain unchanged.

What I asked for / 原始需求：

Organize 12 club files safely; build a bilingual activity picker with strict combined filters, a five-pick history, clear and reset controls; improve mobile usability while preserving functionality; and reject the deliberately unsafe plan. Commit and push only after explicit authorization.

What I checked before execution / 動手前我檢查了什麼：

The agent presented the Task A inventory, duplicate/version findings and plan before I replied “run”. It read the 12 Task B activities and presented its plan before I replied “build”. Task D explicitly prohibited executing the supplied plan. I set these boundaries; a partner permission review or full privacy inspection is not documented.

## Tests actually performed / 我真的做過的測試

The six B v1 cases below are listed in the supplied learning record. I reported in this conversation that all six required functions were manually tested and passed. The export itself has no checked boxes or entered observations. These rows document that reported pass, not newly invented test transcripts. The available screenshot shows commit history, not UI test execution.

| Test / 測試 | Expected / 預期 | Observed / 實際 | Evidence / 證據 |
|---|---|---|---|
| A inventory and copy preservation | 12 inputs each copied once; originals, identical copies and differing proposals preserved | Agent verified 12 unique manifest entries and byte/SHA-256 equality; all 12 original/copy pairs were rechecked when preparing this submission. I reported A completed and verified. | [Manifest](practice/01-club-files/output/manifest.json), [report](practice/01-club-files/output/report.md); commit ca31c48 |
| B1: indoor / 15 / low | Only A01–A04 are eligible | User-reported manual pass; agent filter check found those four eligible activities | B v1 cd2eca4; conversation report; current [picker](practice/02-campus-picker/output/index.html) |
| B2: outdoor / 15 / medium | Exactly “No matching activities.”; no filter relaxation | User-reported manual pass; agent JavaScript test verified empty matches and unchanged history on failure | B v1 cd2eca4; conversation report and agent test results |
| B3: outdoor / 30 / medium | Only A09 | User-reported manual pass; agent filter check found A09 as the sole candidate | B v1 cd2eca4; conversation report and agent test results |
| B4: all / 60 / all; six successful picks | Latest five remain, newest first | User-reported manual pass; agent JavaScript tests checked five-item cap and ordering across repeated successful picks | B v1 cd2eca4; conversation report and agent test results; no exact six-pick sequence recorded |
| B5: reset filters | All locations / 30 minutes / all energy; history preserved | User-reported manual pass; agent JavaScript test verified defaults and unchanged history | B v1 cd2eca4; conversation report and agent test results |
| B6: clear history and switch to English | Empty history; English controls and activity names | User-reported manual pass; agent tested clear-history and bilingual rendering | B v1 cd2eca4; conversation report and agent test results |
| B data and behavior preservation | Source unchanged; mobile revision changes styling only | Agent verified source hash and embedded data equality; B v2 changed only CSS, leaving all markup, JavaScript and activity data unchanged | [Source data](practice/02-campus-picker/activities.json); commits cd2eca4 and 7213102 |
| B v2 usability retest | Easier mobile controls and readable text; original behavior retained | I reported the mobile improvements manually tested and passed. Exact device, viewport dimensions and individual v2 test observations were not recorded. | Conversation report; commit 7213102. No mobile/desktop UI screenshots supplied. |
| D rejection | Identify unsafe actions and propose an authorized alternative; never execute unsafe plan | Written rejection covers five issues and an allowed alternative. I reviewed and approved it. Agent verified bad-plan.txt unchanged at creation. | [Rejection](practice/04-review/my-rejection.md); commit b727036 |

Agent B v1 verification exercised the actual JavaScript using a DOM stub across 27 filter combinations and 540 picks. That is logic testing, not a real-browser or device rendering test. Browser policy blocked the agent’s local-file preview; manual browser testing was reported by me.

## One revision / 一次修改

Before / 原來的情況：

B v1 worked correctly according to my manual tests. I wanted better usability on smaller screens; no functional defect was reported. B v1 is preserved as commit `cd2eca4445698247ce53624b13fdb22da8c9194a`.

Request / 我提出的修改：

Improve mobile layout, increase button tap areas, and make smaller-screen text easier to read without changing filtering, history, reset or bilingual features.

After and retest / 修改後與重測結果：

B v2 uses a single-column layout at widths up to 760px, mobile controls at least 56px tall, larger labels and supporting text, increased spacing, improved long-text wrapping, a full-width Clear History button and a visible Reset border. The agent checked that only CSS changed. I reported the mobile usability changes manually tested and passed. The separate v2 commit is `721310212df6f9303e8abe5486d30fbd33928138`. No before/after UI screenshots are available; the two commits preserve before/after code.

New requirement or defect? / 新需求還是原規格未做到？

A usability enhancement request; the existing functions had passed, and no original functional defect was identified.

## One rejection / 一次退回

Which action I reject and why / 退回哪個動作、為什麼：

Task D rejects organizing all Downloads (excessive scope), deleting duplicates without approval, assuming final2 is approved, guessing missing values and automatically publishing. Each violates the authorized boundaries or risks losing or misrepresenting information.

An acceptable alternative / 可以怎麼改：

Inspect only the selected practice folder, propose a plan and wait for confirmation. Preserve originals, duplicates and all differing versions; copy and categorize files, report unresolved information, and prepare a report for human review. No deletion or publication without explicit approval. See [my-rejection.md](practice/04-review/my-rejection.md).

## Evidence inventory and readiness / 證據與準備狀態

- [Learning record](evidence/learning-record.md): present and readable, preserved as supplied. Its checkboxes are all unchecked and notes empty; it is not a completed self-assessment or proof of execution. This submission supplements it using actual artifacts and statements from this conversation.
- [Available screenshot](evidence/Screenshot%202026-10-12%20at%2012.15.19%E2%80%AFAM.png): one readable PNG showing GitHub commit history for A, B v1, B v2 and D (also the Task A setup commit). It corroborates commit history only, not function tests or mobile appearance. Its original filename and contents are retained.
- Completed task artifacts and their commits are linked above. No prepared simulation evidence is represented as personal execution.
- This submission is ready to record and push with these limitations disclosed. The blank learning-record checklist and missing group code remain incomplete if the course requires them to be filled; no such values have been fabricated.

## Still unverified / 還沒驗證

What I cannot claim is complete / 哪些事不能說已完成：

- Group code, individual/paired route, partner checks and setup privacy/permission review were not supplied.
- Task C was not reported completed.
- The exported learning record has no completed checklist or notes. It does not independently substantiate manual tests.
- No UI screenshots, device/browser details, viewport sizes, exact random-pick sequences or detailed per-case v2 retest results were supplied.
- A’s selected proposal, event time/venue, rain alternative, budget approval and intended duplicate roles remain unresolved, as documented in its report. Filesystem metadata preservation was not verified.

For the fallback route, mark all prepared evidence as supplied simulation. / 備援路線請標明所有預生成證據來源，不能填成自己的Agent實跑。
