# Waku API FURPS

(proposing to move away from "messaging api" to avoid confusion)

## Functionality

1. Setup, start and stop a Waku node.
2. Support edge node operation mode.
3. Support relay node operation mode.
4. Does automatic peer discovery based on the node platform and operation mode.
5. Returns health and connectivity information using proven heuristics.
6. Previously discovered peers are persisted across restarted, and potentially used for future connections.
7. When wrapping the C API, conversion from native types to JSON is needed by the wrapper.
8. When wrapping the C API, conversion from native types to Protobuf is needed by the wrapper (PoC).

## Usability

1. When setting up a Waku node, no need to specify what protocols to mount, only an operational mode (edge or relay).
2. Disconnection detection and recovery, and other peer management matters are automatically handled.
3. Developers do not need to specify the protocols used to send and receive messages; it is deduced from the mode of operation.
4. Developers pass and receive data to the API in types native to the wrapping language.
5. By default, auto-sharding is applied, meaning developers do not need to be concerned by sharding; pubsub topics are never exposed.
6. Developers only need to handle errors in cases of irretrievable failure requiring end-user action. Internal errors are not bubbled up if they can be recovered internally.
7. When wrapping the C API, a protobuf definition can be used to generate native types for the host language (PoC).

## Reliability

1. Sends a message using peer-to-peer reliability (service node redundancy for edge, optional store confirmation)
2. Receives messages using peer-to-peer reliability (service node redundancy for edge, periodic store query, periodic filter ping)

## Performance

## Supportability

1. Developers can use the SDK in nim software, importing it via git path.
2. Developers can use the SDK in Golang software, importing it from on pkg.go.dev.
3. Developers can use the SDK in Browser software, importing it from npmjs.com.
4. Developers can use the SDK in Rust software, importing it from crates.io.

## + (Privacy, Anonymity, Deployments)

1. C API uses JSON format for data passing.
2. C API uses Protobuf format for data passing.