# OctoAcme — Cross-Functional Collaboration & Communication

## Purpose
Provide clear guidance on how different roles communicate, make decisions together, and collaborate effectively to reduce delays, confusion, and rework.

## Communication Matrix

| From / To | PM | PdM | Dev | QA | Tech Lead | DevOps | Security | Sponsor |
|---|---|---|---|---|---|---|---|---|
| **PM** | — | Daily | Daily standup | Daily standup | Weekly tech sync | Pre-release | Security sign-off | Weekly status |
| **PdM** | Daily | — | Sprint planning | Sprint review | Design review | N/A | Req. review | Priority sync |
| **Dev** | Standup | Sprint planning | Code review | PR/QA handoff | Design questions | Deployment prep | Security review | N/A |
| **QA** | Quality report | Acceptance test | Test feedback | Test planning | Quality risks | Deploy validation | Security testing | Release sign-off |
| **Tech Lead** | Tech escalation | Feasibility input | Design guidance | N/A | Architecture sync | Scalability input | Architecture review | N/A |
| **DevOps** | Deployment status | N/A | Env support | Env/monitoring | Infrastructure plan | Pipeline sync | Infra security | Deployment ready |
| **Security** | Risk escalation | Security req. | Code review | Security testing | Architecture review | Infra security | — | Compliance status |
| **Sponsor** | Status review | Decisions | N/A | Release sign-off | Tech risks | N/A | Compliance risks | — |

**Key**: Daily = at least once per day; Weekly = at least once per week; N/A = not typical unless issue-specific

---

## Decision-Making Framework (RACI)

### Critical Decision Types

| Decision | Responsible | Accountable | Consulted | Informed |
|---|---|---|---|---|
| **Project Approval** | PM + PdM | Sponsor | Tech Lead, Stakeholders | Team |
| **Scope Changes** | PdM | PM + Sponsor | Tech Lead, QA Lead | Team |
| **Release Timeline** | PM | Sponsor + PdM | Tech Lead, DevOps | Team |
| **Technical Design** | Tech Lead | PM + Tech Lead | Developers, DevOps, Security | QA |
| **Acceptance Criteria** | PdM | PdM | Developers, QA, Tech Lead | PM |
| **Quality/Test Strategy** | QA Lead | QA Lead + PdM | Tech Lead, Developers | PM |
| **Architecture Decisions** | Tech Lead | CTO/Tech Lead | Developers, DevOps, Security | PM, PdM |
| **Security Requirements** | Security Lead | Security Lead | Tech Lead, DevOps, Developers | PM, PdM, QA |
| **Deployment Go/No-Go** | DevOps + QA | PM + DevOps | Tech Lead, Security | Team, Sponsor |
| **Risk Escalation** | PM | PM + Sponsor | Relevant leads | Team |
| **Resource Allocation** | PM | Sponsor | PdM, Tech Lead | Team |
| **Process Changes** | Scrum Master | PM + Scrum Master | Team, Tech Lead | Stakeholders |

**RACI Definitions**:
- **Responsible**: Does the work or makes the decision
- **Accountable**: Final authority; approves the decision
- **Consulted**: Provides input before decision
- **Informed**: Notified after decision is made

---

## Meeting Cadence & Agendas

### 1. Daily Standup (15 min)
**Participants**: Full delivery team (Dev, QA, Tech Lead, Scrum Master)
**Frequency**: Daily at [agreed time]
**Owner**: Scrum Master

**Agenda**:
- What did each person accomplish yesterday?
- What will they work on today?
- What blockers or dependencies exist?

**Success Metrics**:
- Completed within 15 minutes
- Blockers identified and assigned owners for resolution
- No detailed problem-solving (take offline)

---

### 2. Sprint Planning (2-4 hours)
**Participants**: PM, PdM, Developers, QA, Tech Lead, Scrum Master
**Frequency**: Start of each sprint
**Owner**: Scrum Master (facilitation) + PdM (prioritization)

**Agenda**:
- Review sprint goal and priorities from PdM
- Discuss high-level approach (Tech Lead)
- Team estimates story points / T-shirt sizes
- Confirm team capacity and sprint commitment
- Identify risks and dependencies
- Confirm Definition of Done

**Success Metrics**:
- Team commits to realistic sprint scope
- All stories have acceptance criteria and estimates
- Risks and dependencies identified
- QA has test plan drafted

---

### 3. Weekly PM-PdM Sync (30 min)
**Participants**: PM, PdM, (Tech Lead if issues)
**Frequency**: Weekly (midweek)
**Owner**: PM

**Agenda**:
- Progress against plan and metrics
- Risks and mitigations
- Scope or timeline changes needed?
- Upcoming dependencies or blockers
- Sponsor communication needs
- Decision log updates

**Success Metrics**:
- Risk register updated
- Sponsor aware of critical issues
- Clear next steps documented

---

### 4. Weekly Technical Sync (45 min)
**Participants**: Tech Lead, Senior Developers, DevOps, Security (if applicable)
**Frequency**: Weekly
**Owner**: Tech Lead

**Agenda**:
- Architecture / design decisions needed
- Technical blockers or risks
- Code quality and testing coverage
- Performance and scalability concerns
- Infrastructure or DevOps needs
- Security implications of current work

**Success Metrics**:
- Technical risks identified and escalated
- Design decisions documented
- Team consensus on approach

---

### 5. Sprint Review / Demo (1 hour)
**Participants**: Full team, Sponsor (optional), stakeholders
**Frequency**: End of sprint
**Owner**: PM / PdM

**Agenda**:
- Demo completed stories / working increments
- Review what met acceptance criteria
- Gather feedback from stakeholders
- Discuss what to adjust for next sprint
- Review metrics (velocity, defects, etc.)

**Success Metrics**:
- All completed stories demoed
- Stakeholder feedback captured
- Velocity tracked for planning

---

### 6. Retrospective (45-75 min)
**Participants**: Full delivery team, Scrum Master (facilitator)
**Frequency**: End of sprint or milestone
**Owner**: Scrum Master

**Agenda**:
- What went well?
- What could be improved?
- What should we stop doing?
- Select 2-3 action items for next sprint
- Review action items from previous retros

**Success Metrics**:
- Blameless, psychological safety maintained
- 2-3 actionable improvements identified
- Team feels heard and engaged

---

### 7. Weekly Stakeholder Update (20 min)
**Participants**: PM, PdM, Sponsor, key stakeholders
**Frequency**: Weekly or milestone-based
**Owner**: PM

**Agenda**:
- Progress summary (% complete, velocity)
- Key accomplishments this week
- Upcoming milestones
- Risks requiring sponsor awareness or decision
- Budget or resource implications

**Success Metrics**:
- Sponsor informed and confident
- Clear escalation path for decisions
- Aligned on timeline and priorities

---

### 8. Pre-Release Readiness Review (1 hour)
**Participants**: PM, QA Lead, Tech Lead, DevOps, Security (if applicable)
**Frequency**: 2-3 days before planned release
**Owner**: PM

**Agenda**:
- All acceptance criteria met and tested?
- CI pipeline passing?
- Security and compliance checks complete?
- Release notes drafted and accurate?
- Rollback plan documented?
- Deployment procedure reviewed?
- Post-deploy verification plan defined?
- Sponsor approval obtained?

**Success Metrics**:
- Go/No-Go decision made with confidence
- All risk mitigation plans in place
- Team ready to execute deployment

---

## Handoff Protocols

### Handoff 1: Design → Development
**Trigger**: Acceptance criteria finalized and design approved

**Owner** (making handoff): PdM + Tech Lead  
**Owner** (receiving): Tech Lead + Dev team  

**Checklist**:
- [ ] Acceptance criteria clear and non-ambiguous
- [ ] Technical design document reviewed and approved
- [ ] Dependencies identified and documented
- [ ] Spike work (if needed) completed
- [ ] Test approach discussed with QA
- [ ] Dev team confident in estimates
- [ ] Acceptance criteria signed off by PdM
- [ ] Dev team commits to sprint goal

**Success Criteria**: Dev team begins work without clarification delays

---

### Handoff 2: Development → QA
**Trigger**: Feature code-complete and merged to main/staging branch

**Owner** (making handoff): Developers + Tech Lead  
**Owner** (receiving): QA Lead + Testers  

**Checklist**:
- [ ] All unit tests pass (min. XX% coverage)
- [ ] Code review completed and approved
- [ ] Feature deployed to staging environment
- [ ] Release notes updated
- [ ] Known limitations documented
- [ ] QA test plan ready
- [ ] QA aware of dependencies or integrations
- [ ] Dev team available for questions during testing

**Success Criteria**: QA can begin testing without blocker questions

---

### Handoff 3: QA → Deployment
**Trigger**: Feature passes QA acceptance testing

**Owner** (making handoff): QA Lead + Testers  
**Owner** (receiving): DevOps + PM  

**Checklist**:
- [ ] All acceptance criteria validated and passing
- [ ] No critical or high-severity defects open
- [ ] Smoke tests documented and ready
- [ ] Known low-severity defects logged (with workarounds)
- [ ] Release notes finalized and reviewed
- [ ] Rollback procedure documented
- [ ] Deployment window scheduled
- [ ] Post-deploy verification checklist prepared
- [ ] Security sign-off obtained
- [ ] Sponsor approval obtained

**Success Criteria**: Release ready to deploy with confidence

---

## Escalation Process

### Level 1: Team Triage (Daily Standup)
**Trigger**: Blocker, dependency, or issue identified in standup

**Steps**:
1. Blocker owner identified in standup
2. Take offline with relevant team members
3. Resolve within 24 hours if possible
4. If unresolved, escalate to Level 2

**Owner**: Scrum Master

---

### Level 2: PM / Technical Escalation (Daily)
**Trigger**: Team cannot resolve within 24 hours, or decision needed from PM/Tech Lead

**Steps**:
1. PM / Tech Lead convenes relevant parties
2. Diagnosis: root cause, impact, options
3. Decision or mitigation plan within 24 hours
4. Update team with resolution
5. If decision still unresolved or high impact, escalate to Level 3

**Owner**: PM or Tech Lead (depending on type)

**Examples**:
- Technical design choice between options
- Resource constraint requiring reallocation
- Dependency blocked by another team
- Quality concern requiring scope trade-off

---

### Level 3: Sponsor / Executive Escalation
**Trigger**: Decision impacts timeline, scope, budget, or involves cross-org dependencies

**Steps**:
1. PM prepares escalation memo:
   - What's the issue?
   - What's the impact?
   - What are the options?
   - What's the recommendation?
   - What decision is needed?
2. Present to Sponsor with timeline for decision
3. Sponsor decision within 24-48 hours
4. PM communicates decision and next steps

**Owner**: PM (on behalf of project)

**Examples**:
- Timeline slippage affecting release date
- Scope change requiring new resources
- Cross-org dependency requiring prioritization
- Budget implications of approach
- Security or compliance violation

---

## Conflict Resolution

### Common Conflict Scenarios

#### Scenario 1: PdM vs. Dev on Acceptance Criteria
**Typical Issue**: Dev says story is "done" but doesn't meet all PdM's acceptance criteria

**Resolution Process**:
1. Scrum Master facilitates discussion in standup or after
2. Review each acceptance criterion
   - Is it achievable in current sprint?
   - Is it testable and clear?
   - Is it necessary for release?
3. Options:
   - Add clarification and Dev continues work
   - Move criterion to future story
   - Adjust criterion to be achievable
4. Document decision and move forward

---

#### Scenario 2: Tech Lead vs. PdM on Technical Feasibility
**Typical Issue**: PdM wants feature, Tech Lead says it's too risky or complex

**Resolution Process**:
1. Tech Lead explains technical risks/concerns
2. PdM explains business need/customer value
3. Explore options:
   - Phased approach (MVP first, advanced features later)
   - Technical refactoring work (spike)
   - Alternative approach with less technical debt
4. If still disagreement, escalate to PM for decision
5. Document trade-offs and decision rationale

---

#### Scenario 3: QA vs. Dev on Defect Severity
**Typical Issue**: QA found bug; Dev says it's low priority or "works as designed"

**Resolution Process**:
1. QA and Dev review together
2. Assess impact: What's affected? How many users? What's the workaround?
3. Agree on severity level
4. If QA and Dev disagree:
   - QA Lead + Tech Lead + PM convene
   - Assess business impact and decide priority
   - Document decision
5. Proceed based on severity (fix now or defer)

---

#### Scenario 4: Scope vs. Timeline Trade-off
**Typical Issue**: Can't deliver everything by deadline

**Resolution Process**:
1. PM + PdM identify which features are must-have for deadline
2. Discuss deferral options with Sponsor
3. Options:
   - Reduce scope (defer lower-priority features)
   - Extend timeline
   - Add resources (if feasible)
   - Reduce quality acceptance (not recommended)
4. Sponsor decision
5. Update plan and team commitments

---

## Quick Reference: Who to Contact

### If you have a question about...

**Acceptance Criteria or Feature Requirements** → Product Manager (PdM)  
**Technical Design or Architecture** → Technical Lead  
**Timeline, Scope, or Risks** → Project Manager (PM)  
**Test Strategy or Quality Concerns** → QA Lead  
**Development Standards or Code Quality** → Technical Lead  
**Deployment or Infrastructure** → DevOps Engineer  
**Security Requirements or Concerns** → Security Lead  
**Process Questions** → Scrum Master or PM  
**Budget or Resource Allocation** → Project Manager + Sponsor  
**Strategic Decisions or Blocking Issues** → Project Manager + Sponsor  

---

## Communication Tips

### Effective Sync Meetings
- ✅ Start and end on time
- ✅ Agenda shared in advance
- ✅ Decisions documented
- ✅ Action items assigned with owners and dates
- ❌ Don't use for detail problem-solving (take offline)
- ❌ Don't skip meetings to "save time" (creates misalignment)

### Effective Escalations
- ✅ Include context and options
- ✅ Explain impact and timeline needed
- ✅ Make a recommendation
- ❌ Don't escalate to avoid making a decision
- ❌ Don't blindside decision-maker without prep

### Effective Handoffs
- ✅ Use the handoff checklist
- ✅ Confirm receiver is ready
- ✅ Document unknowns and risks
- ✅ Make receiver aware of dependencies
- ❌ Don't assume receiver knows all context
- ❌ Don't hand off incomplete work

---

## Next Steps & Improvements

- Review this guide at project kickoff
- Tailor meeting cadence to your project (may adjust frequency)
- Capture actual decision patterns in Retrospectives
- Update based on team feedback and lessons learned
- Reference this guide when conflict arises
