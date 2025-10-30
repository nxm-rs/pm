# nxm-rs Project Management

Where we pretend to plan things before diving into code. Sometimes it even works.

## How we work

1. **Issues first** - Problems get discussed before solutions get coded
2. **Epics for big stuff** - When something needs multiple PRs, make an epic
3. **Milestones for deadlines** - When we actually have deadlines (rare)
4. **ADRs for decisions** - When we make choices that'll confuse future us

## What's here

### `/adr`
Architecture Decision Records. For when we make non-obvious technical choices that future developers will wonder about.

### `/roadmap`
High-level direction. What we're building and roughly when. Emphasis on "roughly".

### `/templates`
Issue and PR templates specific to the PM repo. For tracking epics and milestones.

## How to use this repo

### Creating an Epic

Use the epic template. An epic should:
- Solve a real problem
- Be too big for one PR
- Have clear success criteria
- Link to related issues

### Tracking Progress

- Use GitHub Projects for visual tracking (if you're into that)
- Use issue labels consistently (see `.github` repo for label definitions)
- Update epic descriptions as scope changes (it always does)

### Roadmap Planning

- Quarterly planning in `/roadmap/YYYY-QX.md`
- Focus on outcomes, not features
- Be realistic about velocity
- Leave room for fixing things that break

## Working Principles

1. **Ship working code** - Better to ship something that works than plan something perfect
2. **Fix it in post** - Launch, learn, iterate
3. **Communicate changes** - If scope/timeline changes, say so early
4. **No process theater** - If a process doesn't help ship better code, kill it

## Repository Links

### Main Products
- [nexum](https://github.com/nxm-rs/nexum) - Ethereum wallet for people who read docs
- [vertex](https://github.com/nxm-rs/vertex) - Swarm node that actually works

### Infrastructure
- [.github](https://github.com/nxm-rs/.github) - Org-wide templates and community files
- [pm](https://github.com/nxm-rs/pm) - This repo

## Label System

We use pragmatic labels across all repos:

- **Priority**: `p0-fire`, `p1-broken`, `p2-annoying`, `p3-maybe`
- **Status**: `blocked`, `investigating`, `pr-welcome`
- **Type**: `bug`, `feature`, `dx`, `perf`, `debt`, `docs`
- **Effort**: `effort/minutes`, `effort/hours`, `effort/days`, `effort/weeks`

## Contributing

See [CONTRIBUTING.md](https://github.com/nxm-rs/.github/blob/main/CONTRIBUTING.md) for how to contribute without wasting everyone's time.

---

**Remember**: Plans are worthless, but planning is everything. Write code, ship features, fix bugs. Everything else is negotiable.