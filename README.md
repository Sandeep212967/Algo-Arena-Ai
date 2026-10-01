# Algo-Arena-Ai
                                     ┌─────────────────────────────┐
                    │       Algo-Arena-Ai Web      │
                    │       Next.js + React         │
                    │       TypeScript              │
                    │       App Router              │
                    │       Tailwind CSS             │
                    └──────────────┬──────────────┘
                                   │
                                   ▼
                    ┌─────────────────────────────┐
                    │          App Shell           │
                    │                              │
                    │ Sidebar │ Header │ Content    │
                    └──────────────┬──────────────┘
                                   │
                     ┌─────────────┴─────────────┐
                     │                           │
                     ▼                           ▼
              UI Components               Feature Screens
                     │                           │
       ┌─────────────┴──────────┐       ┌───────┴────────┐
       │                        │       │                │
    Button                    Card   Problems          AI
    Input                     Modal  Contests        Dashboard
    Badge                     Toast  Profile         Skills
    States                           etc.            etc.
                     │
                     ▼
              API Integration
                     │
                     ▼
              /api/v1/*
                     │
                     ▼
            ┌─────────────────┐
            │ NestJS API      │
            └────────┬────────┘
                     │
          ┌──────────┴──────────┐
          ▼                     ▼
     PostgreSQL                Redis
     System of Record       Cache/Queue/State
          │                     │
          │              ┌──────┴──────┐
          │              ▼             ▼
          │         AI Workers    Judge Workers
          │              │             │
          │              ▼             ▼
          │             AI      Secure Sandbox
          │
          ▼
      Core Modules

             apps/api/src/modules/

auth/
users/
profiles/
problems/
submissions/
judge/
contests/
ratings/
skills/
recommendations/
ai/
research/
variants/
sql/
dbms/
system-design/
interviews/
projects/
collaboration/
community/
notifications/
organizations/
career/
billing/
integrity/
admin/
analytics/

GET    /api/v1/health

POST   /api/v1/auth/register
POST   /api/v1/auth/login
POST   /api/v1/auth/logout

GET    /api/v1/me

GET    /api/v1/problems
GET    /api/v1/problems/:slug

POST   /api/v1/problems/:id/submissions
GET    /api/v1/submissions/:id

GET    /api/v1/daily-challenge

GET    /api/v1/contests
GET    /api/v1/contests/:slug

{
  "success": true,
  "data": {},
  "message": "Request successful",
  "error": null,
  "requestId": "..."
}

Error
{
  "success": false,
  "data": null,
  "message": "Validation failed",
  "error": {
    "code": "VALIDATION_ERROR",
    "details": []
  },
  "requestId": "..."
}
user.created
user.onboarded

problem.created
problem.published

submission.created
submission.queued
submission.started
submission.completed

skill.updated
recommendation.created

ai.job.created
ai.job.completed
ai.job.failed

contest.joined
contest.submitted
contest.completed

assessment.started
assessment.completed

project.created
project.completed

USER
AUTHOR
MENTOR
MODERATOR
ADMIN
ORGANIZATION_ADMIN
RECRUITER
problem.read
problem.create
problem.edit
problem.publish

submission.create

contest.create
contest.manage

assessment.create

organization.manage

user.moderate
PRIVATE
PUBLIC
UNLISTED
ORGANIZATION_ONLY
Profile
Submission
Contest
Project
Skill Passport
Assessment
Social activity
Organization content

# today target 
Algo.Anera.Ai Web
       │
       ├── App Shell
       │    ├── Sidebar
       │    ├── Header
       │    └── Main Content
       │
       ├── Design Tokens
       │    ├── Colors
       │    ├── Typography
       │    ├── Spacing
       │    ├── Radius
       │    └── Shadows
       │
       └── UI Primitives
            ├── Button
            ├── Card
            ├── Input
            ├── Modal
            ├── Toast
            ├── Badge
            └── States

## today command used in nest/next js
`cd /workspaces/Algo-Arena-Ai
ls apps/web`

`npm exec --yes create-next-app@latest apps/web`


### these are intall in today

TypeScript        → Yes
ESLint            → Yes
Tailwind CSS      → Yes
src/ directory    → Yes
App Router        → Yes
Turbopack         → Yes
Import alias      → Yes
Alias             → @/*

P1
UI components + layout

P2
API contract ke according future integration

P3
AI screens ke component requirements

P4
responsive + accessibility + UI testing
# run command
`pnpm --filter web dev`
