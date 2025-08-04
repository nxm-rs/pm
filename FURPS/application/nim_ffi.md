# Nim-FFI FURPS

## Functionality

1. Provides the core logic needed to expose any synchronous or asynchronous Nim library to a C-FFI library.

## Usability

1. Introduce new pragma definitions, such as `{.ffi.}`, to appropriately annotate types and procedures.
2. Any Nim project can use it and can be installed using Nimble,
   similarly to how nim-chronos is imported.
3. The interaction with the exposed C library can be done using JSON.
4. The interaction with the exposed C library can be done using protobuf.

## Reliability

1. Nim-FFI does not leak memory.
2. The exposed C library never hangs when working asynchronously.

## Performance

## Supportability

1. The exposed C library can be used in Golang.
2. The exposed C library can be used in Rust.
3. The exposed C library can be used in Python.

## + (Privacy, Anonymity, Deployments)

1. `nwaku` repository uses `nim-ffi` to expose the existing `libwaku` functionality.

