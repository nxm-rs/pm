# Upgrade Nim Usage

**Estimated date of completion**: 19 Dec

**Resources Required for 2025H2**:
- 1 nwaku eng for 2 months
- Support from Vac/Nim team

Improve usage of Nim related tooling and design patterns by proceedings with PoCs to discover potential gains and caveats.
This includes adoption of Nimble, dogfooding VSCode plugin and iteration on C-Binding methodology.

## Strategic Objective

Logos Movement Community Enabling: Dev Journey

## FURPS

See deliverables.

## Risks

| Risk                | (Accept, Own, Mitigation)                                                                                                                                                                                           |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Maturity of tooling | This milestone focusing on trying out fresh Nim tooling, hence it may not be possible to output a PoC, but instead raising a series of upstream issues.                                                             |
| Actual value/impact | The direct value on dev ex is not always clear, especially for Nimble. There is hope on bette contributor experience, but the end impact may mostly be on improving Nim tooling by providing constructive feedback. |

## Deliverables

### Migrate nwaku to Nimble PoC

Note: maybe taken over by Vac-Nim

**Owner**: nwaku

**Feature**: [nwaku](/FURPS/application/nwaku.md)

**FURPS**:
- U1. Uses nimble for package management and build.
- U2. Can be imported as a nim library using nimble.

**Checklist**:
- [ ] Specs: link to specs and/or API definition
- [ ] Code: link to GitHub issues/PRs/Epic
- [ ] Dogfood: link to dogfooding session/artefact
- [ ] Docs: links to README.md or docs.waku.org (TBD)

### Dogfood VSCode Plugin and Nimsuggest

**Owner**: nwaku

**No FURPS**

**Depends on Migrate nwaku to Nimble PoC** 

**Output**:
- [ ] Test nimsuggest in the nwaku codebase
- [ ] Create reproducible setup for crashes and poor performance, open upstream issues.
- [ ] Optional: provide a plan to make nwaku better compatible with nimsuggest (eg. no git submodule, less macros, etc)


### Streamline FFI API Creation by using Protobuf types instead of JSON PoC

**Owner**: nwaku

**Feature**: [Waku SDK](/FURPS/core/waku_sdk.md)

**FURPS**:
- F8. When wrapping the C API, conversion from native types to Protobuf is needed by the wrapper (PoC).

- U7. When wrapping the C API, a protobuf definition can be used to generate native types for the host language (PoC).

**Checklist**:
- [ ] Specs: link to specs and/or API definition
- [ ] Code: link to GitHub issues/PRs/Epic
- [ ] Dogfood: link to dogfooding session/artefact
- [ ] Docs: links to README.md or docs.waku.org (TBD)