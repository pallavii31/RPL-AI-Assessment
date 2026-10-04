# RPL AI Assessment Platform

## Master Specification — V1

**Project:** RPL AI Assessment Platform
**Version:** 1.0
**Status:** MVP / SIH 2026 Prototype
**Primary Goal:** Build a working, demo-ready prototype for AI-assisted Recognition of Prior Learning (RPL) assessment with offline-first capability.

---

# 1. Product Overview

The RPL AI Assessment Platform is an AI-assisted assessment system designed to support the assessment of workers who have acquired practical skills and experience through informal or non-formal learning but may not have formal certification.

The platform helps an assessor:

- Capture a worker's prior experience.
- Extract and organize skills from the worker's self-declaration.
- Recommend a suitable Qualification Pack (QP).
- Present structured competency criteria for assessment.
- Capture practical assessment responses and evidence.
- Provide AI-assisted observations and competency summaries.
- Apply standardized scoring.
- Maintain traceability between criteria, evidence, observations, and scores.
- Work in offline conditions.
- Synchronize locally stored assessment data when connectivity becomes available.
- Generate a competency profile/report.

The platform is **AI-assisted, not AI-controlled**.

The final competency decision must remain with the authorized human assessor.

---

# 2. Problem Statement

Many workers possess substantial practical knowledge and skills gained through work experience, apprenticeships, informal learning, or other non-formal pathways.

However, the absence of formal certification can make it difficult to:

- Demonstrate existing competencies.
- Map practical experience to recognized qualification standards.
- Conduct consistent assessments.
- Maintain structured evidence.
- Generate traceable assessment records.
- Complete assessments in locations with unreliable internet connectivity.

The platform addresses these challenges through an AI-assisted, standardized, evidence-based, and offline-first assessment workflow.

---

# 3. Product Objective

The objective of the MVP is to demonstrate a complete digital RPL assessment journey:

```text
Worker Experience
        ↓
Skill Extraction
        ↓
QP Recommendation
        ↓
Assessor Confirmation
        ↓
Structured Assessment
        ↓
Evidence Capture
        ↓
AI Assistance
        ↓
Standardized Scoring
        ↓
Assessor Review
        ↓
Final Competency Decision
        ↓
Competency Profile / Report
        ↓
Synchronization

```

The MVP should demonstrate this complete vertical slice for **one selected trade / Qualification Pack**.

For the prototype, an **Electrician-type trade** may be used as the sample assessment domain.

The QP and assessment data used for the prototype may be sample/demo data unless an official source is explicitly integrated.

---

# 4. MVP Goals

The MVP must demonstrate the following capabilities:

1. Worker registration/profile creation.
2. Worker self-declaration of experience and skills.
3. AI-assisted skill extraction.
4. QP recommendation.
5. Assessor confirmation of the recommended QP.
6. Structured practical assessment.
7. Evidence capture/attachment.
8. Criterion-level scoring.
9. AI-assisted evidence/observation support.
10. Assessor review.
11. Human-controlled final decision.
12. Competency profile generation.
13. Offline assessment capability.
14. Local storage of assessment data.
15. Synchronization after connectivity returns.
16. Assessment traceability.
17. Basic audit information.
18. Demo-ready user interface.

---

# 5. Explicit MVP Scope

The MVP focuses on one complete assessment workflow rather than supporting every possible trade or institutional workflow.

## Included

### Worker

- Create/select worker profile.
- Enter personal/basic information.
- Enter prior work experience.
- Enter skills and practical experience.
- Submit self-declaration.

### AI Skill Extraction

- Analyze worker's description.
- Extract relevant skills.
- Display extracted skills.
- Show the extracted skills to the user/assessor for review.

### Qualification Pack Matching

- Compare extracted skills with available sample QPs.
- Recommend the most relevant QP.
- Display matching/reasoning information.
- Allow assessor to confirm or change the QP.

### Assessment

- Display assessment criteria.
- Display tasks/questions/checklist items.
- Allow assessor to record responses.
- Record scores.
- Record assessor observations.
- Capture evidence metadata and attachments where supported.

### AI Assistance

- Assist with skill extraction.
- Assist with QP matching.
- Assist with evidence/observation interpretation.
- Generate a competency summary.

### Scoring

- Apply a defined scoring rubric.
- Calculate criterion-level scores.
- Calculate overall assessment results.
- Display score breakdown.

### Assessor Decision

- Assessor reviews evidence and scores.
- Assessor can accept or modify AI-assisted observations.
- Assessor makes the final competency decision.

### Competency Profile

- Display assessed competencies.
- Display scores.
- Display evidence.
- Display assessor observations.
- Display final decision.
- Generate a basic assessment report/profile.

### Offline

- Assessment package can be available locally.
- Assessment responses can be stored locally.
- Evidence metadata can be stored locally.
- Scores and notes can be stored locally.
- Pending changes can be placed in a synchronization queue.

### Synchronization

When connectivity becomes available:

```text
LOCAL
  ↓
PENDING_SYNC
  ↓
SYNCING
  ↓
SYNCED

```

If synchronization fails:

```text
SYNC_FAILED

```

The assessment data must remain locally available until synchronization succeeds.

---

# 6. Out of Scope for MVP

The following are not required for V1:

- Full production deployment.
- Multi-state production rollout.
- Complete national QP database.
- Integration with every official government system.
- Aadhaar integration.
- Payment systems.
- Advanced biometric verification.
- Full enterprise identity management.
- Complex role/permission administration.
- Large-scale distributed infrastructure.
- Production-grade cloud synchronization architecture.
- Advanced analytics dashboards.
- Automated certification issuance.
- AI-based automatic PASS/FAIL certification.
- Fully autonomous assessment.
- Complex video-processing pipelines.
- Large-scale model training.
- Real-time multi-assessor collaboration.
- Complete institutional administration system.

These may be considered future enhancements.

---

# 7. Target Users

## 7.1 Worker / Candidate

The worker provides:

- Personal/basic information.
- Work experience.
- Existing skills.
- Practical experience.
- Self-declaration.

The worker should not need to understand technical qualification terminology.

---

## 7.2 Assessor

The assessor:

- Reviews worker information.
- Reviews AI skill extraction.
- Confirms the Qualification Pack.
- Conducts/records assessment.
- Reviews evidence.
- Reviews scores.
- Reviews AI observations.
- Makes the final competency decision.

The assessor remains responsible for the final decision.

---

## 7.3 System / AI Assistant

The AI system assists with:

- Skill extraction.
- QP recommendation.
- Evidence/observation assistance.
- Competency summary generation.

The AI system does not independently certify the worker.

---

# 8. Core User Journey

## Journey 1 — Worker Registration

```text
Start
 ↓
Create Worker Profile
 ↓
Enter Experience
 ↓
Enter Skills / Work History
 ↓
Submit Self-Declaration

```

---

## Journey 2 — AI Skill Extraction

```text
Worker Experience
 ↓
AI Processing
 ↓
Extracted Skills
 ↓
Worker / Assessor Review

```

Example:

Worker input:

> "I have worked as an electrician for 5 years. I install wiring, switches,
> sockets, distribution boards and troubleshoot electrical faults."

Possible extracted skills:

- Electrical wiring
- Switch and socket installation
- Distribution board installation
- Electrical fault troubleshooting
- Electrical safety practices

The extracted skills must remain editable/reviewable.

---

## Journey 3 — QP Recommendation

```text
Extracted Skills
 ↓
Compare with Available QPs
 ↓
QP Recommendation
 ↓
Match Explanation
 ↓
Assessor Confirmation

```

The system should display why a QP was recommended.

Example:

```text
Recommended QP: Electrician

Skill Match:
✓ Electrical Wiring
✓ Installation
✓ Fault Diagnosis
✓ Electrical Safety

Match Confidence: High

```

The assessor must be able to select another QP if required.

---

# 9. Assessment Workflow

After the QP is confirmed:

```text
QP Confirmed
     ↓
Assessment Package Loaded
     ↓
Assessment Criteria
     ↓
Practical Tasks / Questions
     ↓
Evidence Capture
     ↓
Assessor Observations
     ↓
AI Assistance
     ↓
Criterion Scores
     ↓
Overall Score
     ↓
Assessor Review
     ↓
Final Decision

```

---

# 10. Assessment Structure

Each assessment should contain:

## Assessment

- Assessment ID
- Worker ID
- Assessor ID
- QP ID
- Start date/time
- End date/time
- Assessment status
- Overall score
- Final decision
- Sync status

## Assessment Criterion

Each criterion should contain:

- Criterion ID
- Criterion name
- Description
- Maximum score
- Score achieved
- Evidence reference
- Assessor observation
- AI observation, if available
- Review status

## Evidence

Each evidence item should contain:

- Evidence ID
- Assessment ID
- Criterion ID
- Evidence type
- File/reference
- Description
- Capture timestamp
- Source
- Integrity/reference information where applicable
- Sync status

---

# 11. Standardized Scoring

The MVP should use a simple and transparent scoring mechanism.

Each assessment criterion receives a score according to the configured rubric.

Example:

```text
Criterion Score
0 = Not demonstrated
1 = Partially demonstrated
2 = Competent
3 = Highly competent

```

The exact rubric may be configured for the selected demo QP.

The system should display:

```text
Criterion 1       3 / 3
Criterion 2       2 / 3
Criterion 3       3 / 3
Criterion 4       2 / 3
-------------------------
Overall           10 / 12

```

The system may calculate a competency status based on the configured rubric, but the final decision must remain with the assessor.

---

# 12. AI Responsibilities

AI is an assistant to the assessment process.

## AI Function 1 — Skill Extraction

Input:

```text
Worker self-declaration

```

Output:

```text
Structured list of relevant skills

```

The extracted skills should be reviewable.

---

## AI Function 2 — QP Recommendation

Input:

```text
Worker experience
+
Extracted skills
+
Available QPs

```

Output:

```text
Recommended QP
+
Matching skills
+
Explanation / confidence

```

The assessor confirms the QP.

---

## AI Function 3 — Evidence / Observation Assistance

AI may analyze available assessment information and assist the assessor by:

- Identifying relevant observations.
- Relating evidence to criteria.
- Highlighting missing or weak evidence.
- Suggesting structured observation text.

AI suggestions must be clearly distinguishable from assessor-entered observations.

---

## AI Function 4 — Competency Summary

AI may generate a structured summary from:

- Assessment criteria.
- Scores.
- Evidence.
- Assessor observations.
- Confirmed competency information.

The assessor must be able to review the generated summary.

---

# 13. AI Guardrails

The following rules are mandatory:

### Rule 1 — AI does not certify

AI must never independently issue a final competency certification.

### Rule 2 — AI does not replace the assessor

The assessor remains responsible for the final decision.

### Rule 3 — AI output must be reviewable

AI-generated:

- Skills
- QP recommendations
- Observations
- Summaries

must be visible and reviewable.

### Rule 4 — Evidence must be traceable

AI suggestions should be linked to the relevant assessment criterion/evidence whenever possible.

### Rule 5 — Human override

The assessor must be able to:

- Accept AI suggestions.
- Edit AI suggestions.
- Reject AI suggestions.
- Enter their own observation.

---

# 14. Offline-First Requirements

Offline capability is a core product requirement.

The platform should not depend on continuous internet connectivity during assessment.

## Before Going Offline

The system should allow the required assessment package to be available locally.

Example:

```text
QP
 ↓
Assessment Criteria
 ↓
Rubric
 ↓
Assessment Tasks
 ↓
Required Reference Data

```

---

## During Offline Assessment

The following information should be stored locally:

- Worker information.
- Assessment responses.
- Scores.
- Assessor notes.
- Evidence metadata.
- Evidence files where supported.
- Assessment state.
- Synchronization status.

The assessor should be able to continue the assessment without internet access.

---

## After Connectivity Returns

The system should identify locally stored changes and synchronize them.

```text
Local Data
    ↓
Pending Sync Queue
    ↓
Sync
    ↓
Server / Central Storage
    ↓
Synced

```

---

# 15. Synchronization States

Each locally stored assessment should have a synchronization state.

Supported states:

```text
LOCAL
PENDING_SYNC
SYNCING
SYNCED
SYNC_FAILED

```

### LOCAL

Data exists locally and has not been queued for synchronization.

### PENDING_SYNC

Data is ready to synchronize.

### SYNCING

Synchronization is currently in progress.

### SYNCED

Data has successfully synchronized.

### SYNC_FAILED

Synchronization failed.

The system should retain the local data after a synchronization failure.

---

# 16. Evidence and Traceability

Every important assessment result should be traceable.

The system should make it possible to understand:

```text
Final Decision
      ↓
Overall Score
      ↓
Criterion Scores
      ↓
Assessor Observations
      ↓
Evidence

```

For example:

```text
Criterion:
Install electrical wiring

Score:
3 / 3

Evidence:
Practical demonstration

Assessor Observation:
Worker correctly completed wiring and followed the required
safety procedure.

AI Assistance:
Identified evidence as relevant to the criterion.

Final Review:
Accepted by Assessor

```

This traceability is a core platform principle.

---

# 17. Competency Profile

After assessment completion, the platform should generate a competency profile containing:

## Worker Information

- Worker name
- Worker ID
- Assessment ID

## Qualification

- QP name
- QP ID
- Qualification/skill area

## Competencies

For each competency:

- Competency name
- Score
- Evidence
- Assessor observation

## Overall Assessment

- Total score
- Maximum score
- Competency status
- Final assessor decision

## Summary

A concise competency summary may be generated with AI assistance and reviewed by the assessor.

---

# 18. Assessor Review

Before finalizing an assessment, the assessor should have a review screen containing:

```text
Worker Information
        ↓
QP
        ↓
Assessment Criteria
        ↓
Evidence
        ↓
Scores
        ↓
AI Observations
        ↓
Assessor Observations
        ↓
Competency Summary
        ↓
Final Decision

```

The assessor must be able to review and modify relevant information before submission.

---

# 19. Final Decision

The final decision must be explicitly made by the assessor.

Example:

```text
Assessment Result

Overall Score: 10 / 12

AI Recommendation:
Competency demonstrated based on available evidence.

Assessor Decision:

[ Competent ]     [ Not Yet Competent ]

Assessor Comments:
____________________________

[ Finalize Assessment ]

```

The UI must make it clear that the final decision belongs to the human assessor.

---

# 20. Auditability

The MVP should maintain basic audit information.

Important events may include:

- Worker profile created.
- Assessment started.
- QP recommended.
- QP confirmed.
- Evidence added.
- Score entered/changed.
- AI suggestion generated.
- AI suggestion accepted/rejected/edited.
- Assessment finalized.
- Synchronization performed.

Where practical, store:

- Timestamp.
- User/assessor.
- Action.
- Relevant object/record.
- Status.

---

# 21. Data Model — MVP

The MVP should conceptually use the following entities.

```text
User
 ├── Worker
 └── Assessor

Worker
 └── Experience / Skills

QualificationPack
 ├── Competencies
 ├── Criteria
 └── Assessment Tasks

Assessment
 ├── Worker
 ├── Assessor
 ├── QualificationPack
 ├── Responses
 ├── Scores
 ├── Evidence
 ├── Observations
 └── Decision

Evidence
 └── Criterion

AIInteraction
 ├── Input
 ├── Output
 ├── Function
 └── Timestamp

SyncRecord
 ├── Entity
 ├── Status
 └── Last Attempt

AuditRecord
 ├── User
 ├── Action
 └── Timestamp

```

---

# 22. MVP Test Data

The MVP should use a small, controlled dataset.

Recommended demo scenario:

## Trade

Electrician

## Worker

Example worker with several years of informal electrical work experience.

## Experience

Example:

```text
5 years of electrical installation and maintenance experience.

Experience includes:
- Residential wiring
- Switch and socket installation
- Distribution board installation
- Electrical fault troubleshooting
- Basic electrical safety practices

```

## Sample QP

A sample Electrician-related QP containing:

- Competencies
- Assessment criteria
- Tasks
- Scoring rubric

The application must clearly distinguish demo/sample QP information from official certification data if official data has not been integrated.

---

# 23. MVP Screens

The prototype should contain the following major screens.

## Screen 1 — Landing / Login

Purpose:

- Enter the application.
- Select Worker or Assessor workflow.

---

## Screen 2 — Worker Profile

Display:

- Worker information.
- Experience.
- Skills.
- Self-declaration.

---

## Screen 3 — AI Skill Extraction

Display:

- Original worker description.
- Extracted skills.
- AI confidence/indication where available.
- Edit/confirm controls.

---

## Screen 4 — QP Recommendation

Display:

- Recommended QP.
- Skill matches.
- Explanation.
- Alternative QPs if available.
- Assessor confirmation.

---

## Screen 5 — Assessment Dashboard

Display:

- Worker.
- QP.
- Assessment progress.
- Criteria/tasks.
- Evidence status.
- Scores.

---

## Screen 6 — Practical Assessment

Display:

- Current task/criterion.
- Assessment instructions.
- Assessor observation.
- Evidence capture.
- Score input.

---

## Screen 7 — Evidence

Display:

- Evidence attached to criterion.
- Evidence description.
- Timestamp.
- Evidence status.
- Related criterion.

---

## Screen 8 — AI Assistance

Display:

- AI observation/suggestion.
- Evidence relation.
- Accept/Edit/Reject controls.

---

## Screen 9 — Assessor Review

Display:

- All criteria.
- Evidence.
- Scores.
- AI suggestions.
- Assessor observations.
- Overall result.

---

## Screen 10 — Final Decision

Display:

- Overall score.
- Competency summary.
- Assessor decision.
- Assessor comments.
- Finalize button.

---

## Screen 11 — Competency Profile

Display:

- Worker details.
- QP.
- Competencies.
- Scores.
- Evidence summary.
- Final decision.

---

## Screen 12 — Offline / Sync Status

Display:

```text
Connection: Offline

Assessment:
LOCAL

Pending Changes:
4

Sync Status:
Waiting for connection

```

After connection:

```text
Connection: Online

Pending Changes:
4

Syncing...

4 / 4 Synced

```

---

# 24. UI/UX Principles

The application should look like a serious assessment platform rather than a generic AI chatbot.

## Design Principles

- Professional.
- Clean.
- Accessible.
- Simple navigation.
- Clear assessment progress.
- Strong visual hierarchy.
- Evidence-first presentation.
- Clear separation between AI suggestions and assessor decisions.
- Clear offline/online state.
- Minimal unnecessary screens.
- Suitable for tablet/laptop demonstration.

The assessor should always understand:

1. What worker is being assessed.
2. Which QP is being used.
3. Which criterion is being assessed.
4. What evidence is available.
5. What score has been given.
6. What AI suggested.
7. What the assessor decided.

---

# 25. Technical Architecture — MVP

The implementation should remain simple enough to develop and demonstrate quickly.

Recommended architecture:

```text
                    ┌─────────────────────┐
                    │      Frontend       │
                    │ Worker / Assessor   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Application      │
                    │      Backend        │
                    └──────────┬──────────┘
                               │
             ┌─────────────────┼─────────────────┐
             │                 │                 │
             ▼                 ▼                 ▼
      ┌────────────┐    ┌────────────┐    ┌────────────┐
      │ Assessment │    │ AI Service │    │ QP Engine  │
      │   Engine   │    │            │    │            │
      └────────────┘    └────────────┘    └────────────┘
             │                 │                 │
             └─────────────────┼─────────────────┘
                               ▼
                    ┌─────────────────────┐
                    │      Data Store     │
                    │ Workers / QPs /     │
                    │ Assessments /       │
                    │ Evidence / Audit    │
                    └─────────────────────┘

                    Offline Local Storage
                            │
                            ▼
                      Sync Queue
                            │
                            ▼
                       Data Store

```

The exact implementation technology may be selected based on the development environment and prototype constraints.

For the MVP, a lightweight database and browser/local storage approach are preferred over complex infrastructure.

---

# 26. Recommended MVP Technology Approach

A practical implementation may use:

## Frontend

- React
- Vite
- Responsive web UI

## Backend

- Python
- FastAPI

## Database

- SQLite for MVP

## Offline Storage

- Browser local storage / IndexedDB
- Local assessment state
- Sync queue

## AI

The AI layer should be implemented as a replaceable service so that the prototype can use an available AI API/model or controlled mock/demo responses when required.

The application architecture should not tightly couple the assessment workflow to one specific AI provider.

---

# 27. AI Service Interface

The application should conceptually expose separate AI operations.

```text
extractSkills(workerExperience)

recommendQP(workerExperience, skills, availableQPs)

analyzeEvidence(evidence, criterion)

generateCompetencySummary(assessment)

```

Each AI operation should return structured information that the application can display and the assessor can review.

Example:

```json
{
  "skills": [
    "Electrical Wiring",
    "Switch Installation",
    "Fault Troubleshooting"
  ]
}

```

The exact implementation may differ.

---

# 28. Offline Data Strategy

The MVP should separate:

```text
Local Assessment State

```

from:

```text
Synchronized Assessment State

```

Example local record:

```text
assessment_id: A001
status: IN_PROGRESS
sync_status: PENDING_SYNC
last_updated: timestamp

```

Local data must not be lost simply because the network is unavailable.

---

# 29. Sync Strategy

The MVP synchronization flow should be simple.

```text
User performs action
        ↓
Save locally
        ↓
Add to sync queue
        ↓
Connection available?
       / \
     NO   YES
     │     │
     │     ▼
     │   Sync
     │     │
     │     ▼
     │   Success?
     │    /   \
     │  YES   NO
     │   │     │
     │   ▼     ▼
     │ SYNCED  SYNC_FAILED
     │
     └── Wait

```

The prototype should demonstrate this visually.

---

# 30. Demo Mode

The application should be easy to demonstrate.

The demo should not require a large dataset.

Recommended demo flow:

```text
1. Login / Open Application
        ↓
2. Select Worker
        ↓
3. Enter Worker Experience
        ↓
4. AI Extracts Skills
        ↓
5. QP Recommended
        ↓
6. Assessor Confirms QP
        ↓
7. Start Assessment
        ↓
8. Complete Practical Criteria
        ↓
9. Add Evidence
        ↓
10. AI Provides Assistance
        ↓
11. Assessor Reviews Scores
        ↓
12. Demonstrate Offline Mode
        ↓
13. Continue Assessment Offline
        ↓
14. Store Data Locally
        ↓
15. Reconnect
        ↓
16. Synchronize Data
        ↓
17. Assessor Makes Final Decision
        ↓
18. Generate Competency Profile

```

---

# 31. Recommended SIH Demonstration Scenario

The strongest prototype demonstration should show the problem and the solution clearly.

## Scenario

A worker has several years of practical electrician experience but no formal certification.

### Step 1

Worker enters their experience.

### Step 2

AI extracts relevant skills.

### Step 3

Platform recommends a suitable QP.

### Step 4

Assessor confirms the QP.

### Step 5

Assessor conducts a practical assessment.

### Step 6

Evidence and observations are captured.

### Step 7

AI assists with evidence interpretation and summary.

### Step 8

Internet connectivity is disabled.

### Step 9

Assessment continues offline.

### Step 10

Data is stored locally and marked pending sync.

### Step 11

Internet is restored.

### Step 12

Pending data synchronizes.

### Step 13

Assessor reviews the complete assessment.

### Step 14

Assessor makes the final competency decision.

### Step 15

Platform generates the competency profile.

This scenario should be the primary end-to-end demo.

---

# 32. Acceptance Criteria

The MVP is considered successful when the following are demonstrated.

## AC-01 — Worker Profile

A worker profile can be created and saved.

## AC-02 — Experience

Worker experience can be entered.

## AC-03 — Skill Extraction

The system can produce a structured list of skills from worker experience.

## AC-04 — QP Recommendation

The system can recommend a relevant sample QP.

## AC-05 — Assessor Confirmation

The assessor can confirm or change the recommended QP.

## AC-06 — Assessment

The assessor can complete structured assessment criteria.

## AC-07 — Evidence

Evidence can be attached or recorded against assessment criteria.

## AC-08 — Scoring

Criterion-level scores and an overall score are calculated/displayed.

## AC-09 — AI Assistance

AI-generated assistance is clearly identified and reviewable.

## AC-10 — Human Decision

The assessor can make the final decision.

## AC-11 — Traceability

Scores can be traced back to criteria and evidence.

## AC-12 — Offline

The assessment can continue without internet connectivity.

## AC-13 — Local Persistence

Assessment information remains available locally while offline.

## AC-14 — Sync

Pending information can be synchronized when connectivity returns.

## AC-15 — Competency Profile

A final competency profile/report can be displayed/generated.

## AC-16 — Demo

The complete workflow can be demonstrated from worker onboarding through final assessor decision.

---

# 33. Development Principles

## Principle 1 — Build the vertical slice first

Do not build isolated features that cannot connect to the complete assessment workflow.

Priority:

```text
Worker
 ↓
Skills
 ↓
QP
 ↓
Assessment
 ↓
Evidence
 ↓
Scoring
 ↓
Assessor Decision
 ↓
Report

```

---

## Principle 2 — Offline is a core capability

Offline functionality must not be treated only as a future feature.

The MVP should visibly demonstrate offline assessment and synchronization.

---

## Principle 3 — AI assists, humans decide

Every AI feature must preserve assessor control.

---

## Principle 4 — Evidence before automation

The platform should maintain a clear relationship between:

```text
Criterion
→ Evidence
→ Observation
→ Score
→ Decision

```

---

## Principle 5 — Keep the MVP small

One strong complete workflow is more valuable for the SIH prototype than many incomplete modules.

---

## Principle 6 — Avoid unnecessary infrastructure

Do not introduce complex cloud infrastructure, microservices, queues, or enterprise systems unless required for the prototype.

---

## Principle 7 — Make the demo visually understandable

The evaluator should be able to understand:

- What the worker provides.
- What AI does.
- What the assessor does.
- How evidence is used.
- How scoring works.
- How offline mode works.
- How synchronization works.
- How the final decision is made.

---

# 34. Future Scope

Future versions may expand the platform with:

- Multiple trades and QPs.
- Larger official QP repositories.
- Government/official system integrations.
- Advanced identity verification.
- Advanced evidence analysis.
- Image/video-based practical assessment assistance.
- Multilingual worker interaction.
- Voice-based worker interaction.
- Advanced analytics.
- Institution/assessment-center management.
- Advanced synchronization conflict resolution.
- Centralized audit infrastructure.
- Advanced assessor dashboards.
- Digital credential/certificate integration.
- Large-scale deployment infrastructure.

These are not required for MVP V1.

---

# 35. Project Structure

The repository should follow this structure:

```text
RPL-AI-Assessment/
│
├── docs/
│   └── MASTER_SPEC.md
│
├── frontend/
│
├── backend/
│
├── ai/
│
├── data/
│   ├── workers/
│   ├── qps/
│   └── sample_evidence/
│
├── tests/
│
├── README.md
│
└── .gitignore

```

Additional documentation files may be created later when implementation requires them.

---

# 36. Implementation Priority

Development should follow this order.

## Phase 1 — Foundation

- Application shell.
- Navigation.
- Worker profile.
- Assessor workflow.
- Basic data model.
- Sample QP.

## Phase 2 — AI Workflow

- Skill extraction.
- QP recommendation.
- AI observation assistance.
- Competency summary.

## Phase 3 — Assessment

- Assessment criteria.
- Practical tasks.
- Evidence capture.
- Scoring.
- Assessor observations.

## Phase 4 — Offline

- Local storage.
- Offline state.
- Pending sync queue.
- Sync status.

## Phase 5 — Reporting

- Assessor review.
- Final decision.
- Competency profile/report.

## Phase 6 — Demo Polish

- UI refinement.
- Loading/error states.
- Empty states.
- Demo data.
- Offline demonstration.
- Sync demonstration.
- End-to-end testing.

---

# 37. Definition of Done — MVP

The MVP is complete when a user can perform the following sequence without manually manipulating the database:

```text
Create Worker
      ↓
Enter Experience
      ↓
Extract Skills
      ↓
Recommend QP
      ↓
Confirm QP
      ↓
Start Assessment
      ↓
Complete Criteria
      ↓
Attach Evidence
      ↓
Record Scores
      ↓
Receive AI Assistance
      ↓
Review Assessment
      ↓
Continue Offline
      ↓
Store Data Locally
      ↓
Reconnect
      ↓
Sync
      ↓
Assessor Final Decision
      ↓
Competency Profile

```

If this complete sequence works reliably, the MVP has achieved its primary objective.

---

# 38. Key Product Statement

The RPL AI Assessment Platform should demonstrate:

> **AI-assisted, evidence-based, standardized and offline-first assessment of prior learning, with the human assessor retaining final decision authority.**

This statement should guide all MVP implementation decisions.

---

# 39. V1 Change Control

This document is the baseline specification for the MVP.

Any new feature should first be evaluated against:

1. Does it help complete the core RPL assessment journey?
2. Does it improve evidence/traceability?
3. Does it improve offline assessment?
4. Does it improve assessor decision-making?
5. Is it necessary for the SIH demonstration?

If the answer is no to all of the above, the feature should generally be deferred from MVP V1.