# PyTorch Accelerator Integration Working Group Charter

## 1. Mission

The Accelerator Integration Working Group ("WG") operates under the PyTorch Technical Advisory Council (TAC). It works to improve and streamline the integration of diverse AI hardware accelerators with PyTorch, building a scalable and inclusive PyTorch hardware ecosystem.

## 2. Scope

* Integration guidance for out-of-tree accelerators.
* Improvements to PyTorch's accelerator integration mechanisms.
* CI infrastructure and automated integration tests for out-of-tree accelerators.
* Development and execution of the [Additional Compute Platforms Admission Process](url-to-be-added) (admission, periodic review, offboarding).

## 3. Roles

### Co-Chair

* Sets agendas, chairs meetings, and reports to the TAC; pre-reviews (or delegates pre-review of) compute platform submissions and initiates votes; maintains the voting-member roster and records decisions.
* Two (2) Co-Chairs, from different organizations; elected by the voting members under Section 4 and confirmed by the TAC.
* Term: one (1) year, renewable, no term limit. The incumbents' term starts when this charter takes effect.
* May resign with thirty (30) days' notice; removable by WG vote under Section 4 or by the TAC. Vacancies are filled by election within sixty (60) days for a full new term.

### Voting Members

* Vote on WG matters (additional compute platform admissions, Co-Chair elections, charter changes).
* An organization is eligible to hold a voting seat once it (a) holds a TAC voting seat, and (b) is active in the WG — evidenced by meeting attendance, contribution to WG-scoped repositories, or maintaining an accelerator integration effort within the WG's scope, within the preceding six (6) months. Eligible organizations designate one (1) voting representative (and optionally one alternate) by notifying the Co-Chairs.
* No fixed term: status lasts while conditions (a) and (b) hold. The Co-Chairs review the roster every six (6) months; an organization with no activity under (b) across that period has its voting status suspended until it re-engages, at which point it resumes automatically — no re-election needed. An organization may replace its representative at any time by notifying the Co-Chairs, who maintain the current roster (name, organization) in this repository's README.

### Contributors

* Open to anyone in the community; join by participating (GitHub, Slack, meetings). Non-voting; no term or approval required.

All participants are subject to the PyTorch Foundation Code of Conduct.

### 4. Voting

Voting in this WG functions as a lightweight confirmation step rather than an adversarial process: substantive decisions, particularly platform admissions, are typically resolved during Co-Chair technical pre-review, and the procedures below are designed to keep technical work moving rather than to invite extended deliberation.

1. One (1) vote per organization, cast by its eligible voting representative (or alternate, per Section 3). The representative of record at the time a vote opens casts the organization's vote.
2. Eligibility follows Section 3 — a TAC voting seat plus active WG participation, reviewed every six (6) months by the Co-Chairs.
3. Quorum: more than half of the eligible voting members participate; a vote passes by a simple majority of participants.
4. Default is lazy consensus; formal votes are used when consensus cannot be reached or a process requires one.

## 5. Amendments

Amendments are proposed by pull request, adopted by WG vote under Section 4, and take effect upon TAC acknowledgment.
