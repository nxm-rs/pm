# Streamline DevEx: Mobile, Rust and Web dev

**Estimated date of completion**: 30 Nov

**Resources Required for 2025H2**:
- nwaku 3 eng during 6 weeks
- js-waku 2 eng 6 Week Sep

Complete the Waku API implementation in nwaku by implementing edge node mode (Status' Light Mode).

Streamline the Developer Experience by delivering a Rust SDK that implements the full Waku API and is available on crates.io.
As well as building an easy-to-use local dev environment from the browser, enabling developers to build web apps without
relying on external connectivity. Provide a similar harness to deploy a local RLN dev environment.

Finalize the integration of nwaku in Status application by setting up nwaku-based build for Mobile platforms.

Lastly, develop a PoC protocol to demonstrate the usage of Waku as a Signal network, using WebRTC as example.
This was identified as a demanded demonstration of Waku's capabilities as part of the [Waku MVP analysis](https://www.notion.so/Waku-MVP-1838f96fb65c8039acabf8a6a1e689e7).

## Strategic Objective

Logos Movement Community Enabling via Dev-X

## FURPS

See deliverables.

## Risks

| Risk                    | (Accept, Own, Mitigation)                                                                                                                                                |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nwaku performance       | Performance of nwaku in comparison to go-waku will be measured by DST during H2 and may raise issues that will become blockers for pratical usage of nwaku in Mobile.    |
| Publishing to crates.io | One of the challenge to publish libwaku on crates.io is the package size. Several strategy may be developed and tried to find a way to distribute Nim-based Rust crates. |
| Local dev harness       | Creating a local dev environment may be a challenge due to the nature of Waku and RLN, as we would need to locally coordinate bootstrap and blockchain emulation.        |

## Deliverables

### Edge Mode in Nwaku

**Owner**: nwaku

#### **Feature**: [status-go](/FURPS/application/status_go.md)

**FURPS**:
- F2. Nwaku is the used Waku implementation for light mode.
- S3. Light mode is supported. 

#### **Feature**: [nwaku](/FURPS/application/nwaku.md)

**FURPS**:
- S6. libwaku support edge node functionalities. 

**Checklist**:
- [ ] Specs: link to specs and/or API definition
- [ ] Code: link to GitHub issues/PRs/Epic
- [ ] Dogfood: link to dogfooding session/artefact
- [ ] Docs: links to README.md or docs.waku.org (TBD)

### Nwaku in Status Mobile

**Owner**: nwaku

**Feature**: [status-go](/FURPS/application/status_go.md)

**FURPS**:
- S4. Status Mobile binary for Android and iOS.
- S5. Status Tablet binary for Android and iOS. 

- +2. Status Mobile and Tablet CI builds binaries with nwaku, alongside go-waku-based binaries.

**Checklist**:
- [ ] Specs: link to specs and/or API definition
- [ ] Code: link to GitHub issues/PRs/Epic
- [ ] Dogfood: link to dogfooding session/artefact
- [ ] Docs: links to README.md or docs.waku.org (TBD)

### Waku Rust SDK

**Owner**: nwaku

**Feature**: [Waku API](/FURPS/core/waku_api.md)

**FURPS**:
- S4. Rust; available on crates.io.

**Checklist**:
- [ ] Specs: link to specs and/or API definition
- [ ] Code: link to GitHub issues/PRs/Epic
- [ ] Dogfood: link to dogfooding session/artefact
- [ ] Docs: links to README.md or docs.waku.org (TBD)

### Local Web Dev Harness

**Owner**: js-waku

**Feature**: [Local Web Dev Harness](/FURPS/application/local_web_dev_harness.md)

**FURPS**:

- F1. Runs local Waku node to test Web application without relying on external connectivity.
- F2. js-waku runs in NodeJS for testing and CI purposes.

- U1. Developer only need to run a script or preset to start local Waku node and have their web app connect to it.
- U2. Potential WSS/HTTPS issues are worked around so that developer does need to manually generate or import SSL certificates.
- U3. There is an easy option for the developer to bootstrap and connect to local node, instead of external peers.

- S1. Linux and Mac development environments.
- S2. Local network without RLN.
- S3. Chrome and Firefox browsers.

**Checklist**:
- [ ] Specs: link to specs and/or API definition
- [ ] Code: link to GitHub issues/PRs/Epic
- [ ] Dogfood: link to dogfooding session/artefact
- [ ] Docs: links to README.md or docs.waku.org (TBD)

### Local Dev RLN Harness

**Owner**: nwaku

**Feature**: [Local Dev RLN Harness](/FURPS/application/local_dev_rln_harness.md)

**FURPS**:
- F1. Runs local Ethereum environment.
- F2. Deploys ERC-20 and RLN smart contract.
- F3. Utility to fund wallet addresses with necessary tokens for deposit for RLN membership registration.

- U1. Developer only need to run a script to setup local blockchain environment.
- U2. Developers can run documented RPC calls to fund wallet addresses.
- U3. Developers can run documented RPC calls to interact with RLN smart contract.

**Checklist**:
- [ ] Specs: link to specs and/or API definition
- [ ] Code: link to GitHub issues/PRs/Epic
- [ ] Dogfood: link to dogfooding session/artefact
- [ ] Docs: links to README.md or docs.waku.org (TBD)

### [Waku as a Signal Network (WebRTC) PoC](https://github.com/waku-org/pm/issues/298)

**Owner**: js-waku

**Feature**: [Waku as a Signal Network](/FURPS/application/signal_network.md)

**FURPS**:

- F1. Establishes a direct connection between two peers using Waku as a signaling layer

- U1. Developers have access to a simple API: single entry `connect` function and event-based inbound handling.

- R1. End-to-end reliability is implemented for the signaling conversation.
- R2. No provided reliability for established connections, left to the developer (e.g. keep alive).

- S1. Developers can use this protocol in web application, imported from npmjs.com.
- S2. Developers can use this protocol to initiate WebRTC connections.

- +1. Signaling payloads are end-to-end encrypted.
- +2. STUN and TURN servers may be required for WebRTC usage.

**Checklist**:
- [ ] Specs: link to specs and/or API definition
- [ ] Code: link to GitHub issues/PRs/Epic
- [ ] Dogfood: link to dogfooding session/artefact
- [ ] Docs: links to README.md or docs.waku.org (TBD)