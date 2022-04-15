# Description

Gosling is a protocol specification and reference library implementation for said protocol. The protocol is meant to solve the problem of building anonymous, metadata-resistant, and secure peer-to-peer applications using tor onion services.

It is meant to generalize (and improve upon) the authentication scheme used by [Ricochet-Refresh](https://github.com/blueprint-freespeech/ricochet-refresh) clients use to talk to each other. Details can be found in the protocol specification here:

- [Gosling Protocol](./docs/protocol.md)

## Dependencies

Libgosling currently has the following dependencies:

- rust >= 1.60.0
- cmake >= 3.16.6

## Building

The reference implementation is currently a work-in-progress and not fully implemented.

You will need to initialize the git submodules by:

```
$ git submodule update --init
```

All of the usual cmake build types can be generated by invoking `make` from the `out` directory:

- **Debug** - No optimization, asserts enabled, debug symbols
- **MinSizeRel** - Optimize for size, no asserts, no symbols
- **Release** - Optimize for speed, no asserts, no symbols
- **RelWithDebInfo** - Optimize for speed, no asserts, debug symbols

Further information can be found in the cmake documentation:
- https://cmake.org/cmake/help/v3.16/variable/CMAKE_BUILD_TYPE.html

From within one of the generated target directories, the projects may be built by:

```
$ make
```

and tests may then by run by:

```
$ make test
```