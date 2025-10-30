# ADR-0000: Use Architecture Decision Records

## Status
Accepted

## Context
We make architectural decisions all the time. Most get lost in Slack/Discord/someone's head.

## Decision
We'll use ADRs to document decisions that:
- Have lasting impact on the codebase
- Would confuse future developers without context
- Involve trade-offs worth remembering

## Format
Keep it simple:
- **Status**: Proposed/Accepted/Deprecated/Superseded
- **Context**: Why we needed to decide
- **Decision**: What we decided
- **Consequences**: What happens because of this

## What doesn't need an ADR
- Obvious choices
- Temporary hacks (mark them with TODO)
- Style preferences (use a linter)

## Consequences
- Future developers understand why things are the way they are
- We don't relitigate the same decisions repeatedly
- New team members can get up to speed faster