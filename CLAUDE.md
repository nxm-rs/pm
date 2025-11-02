# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is the `pm` (project management) repository for the nxm-rs organization. It tracks planning, architecture decisions, and roadmaps for the main products: nexum (Ethereum wallet) and vertex (Swarm node).

**Key principle**: This org values shipping working code over process theater. Documentation should be pragmatic and decision-focused.

## Repository Structure

- `/adr` - Architecture Decision Records for non-obvious technical choices
- `/roadmap` - Quarterly planning documents (YYYY-QX.md format)
- `/.github/ISSUE_TEMPLATE` - Epic and milestone issue templates

## Working with ADRs

ADRs document architectural decisions that have lasting impact and would confuse future developers without context.

**When to create an ADR**:
- Decisions with lasting codebase impact
- Trade-offs worth remembering
- Non-obvious technical choices

**When NOT to create an ADR**:
- Obvious choices
- Temporary hacks (use TODO comments)
- Style preferences (use linters)

**Format** (keep simple):
- Status: Proposed/Accepted/Deprecated/Superseded
- Context: Why we needed to decide
- Decision: What we decided
- Consequences: What happens because of this

## Working with Roadmaps

Quarterly plans are in `/roadmap/YYYY-QX.md`. Use `TEMPLATE.md` for new quarters.

**Structure**:
- Theme: One-line focus for the quarter
- Goals: 3 maximum, outcome-focused
- Key Deliverables: Organized by product (nexum, vertex, infrastructure)
- Metrics: Specific success measurements
- What we're NOT doing: Explicitly state scope boundaries

**Philosophy**:
- Plan in quarters (anything longer is unreliable)
- Focus on outcomes, not features
- Leave buffer for bugs and breakage
- Plans change when reality hits

## Working with Epics and Milestones

**Epics** (via .github/ISSUE_TEMPLATE/epic.md):
- For features too big for one PR
- Must have clear problem statement (2 sentences max)
- Include success criteria, sub-tasks, and non-goals
- Link related issues as sub-tasks

**Milestones** (via .github/ISSUE_TEMPLATE/milestone.md):
- Quarterly or release-based planning
- 3-5 key deliverables maximum
- Link to constituent epics
- Include success metrics and risks

## Label System

The org uses consistent labels across all repos:

- **Priority**: p0-fire, p1-broken, p2-annoying, p3-maybe
- **Status**: blocked, investigating, pr-welcome
- **Type**: bug, feature, dx, perf, debt, docs
- **Effort**: effort/minutes, effort/hours, effort/days, effort/weeks

## Related Repositories

- [nexum](https://github.com/nxm-rs/nexum) - Ethereum wallet
- [vertex](https://github.com/nxm-rs/vertex) - Swarm node
- [.github](https://github.com/nxm-rs/.github) - Org-wide templates and CONTRIBUTING.md

## Working Principles

1. **Ship working code** - Working implementation beats perfect planning
2. **Fix it in post** - Launch, learn, iterate
3. **Communicate changes** - Alert early when scope/timeline changes
4. **No process theater** - Kill processes that don't help ship better code
