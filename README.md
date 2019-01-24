# dpp-spec

## Note: This is currently a WIP as we transition documentation over to this specification repo.

> Dash Platform Protocol Specification

The DPP spec defines a protocol for data objects which can be stored outside the
blockchain layer. These objects can be verified using the blockchain via the inclusion
of a cryptographic hash of the data objects into a DIP2 special transaction
(which are indeed part of the Dash blockchain).

## Table of Contents

- [Overview](#overview)
- [Contributing](#contributing)
- [Maintainers](#maintainers)
- [License](#license)

## Overview

We define data objects which themselves are JSON and validated using the
JSONSchema specification, using pre-defined JSON Schemas and meta-schemas which
are currently available at: <https://github.com/dashevo/js-dpp/tree/master/schema>.

In addition to adherence to pre-defined JSON Schemata, we also define rules for
hashing and serialization of these objects.

The included meta-schemas allow for creation of conforming schemas (called
DPP-schemas) which are used to define fields in a Dash Platform application.

## Contracts and Objects

Define and describe both contracts and objects

## State

## State Transitions

Broken into headers and packets

### ST Headers

See hashing & serialization section, will be CBOR serialized and hashed via
double-sha256, then added to the blockchain via the DIPx special transaction
type as a payload.

### ST Packets

Will not be added to the blockchain, but a hash of the serialized packet will
be in the ST header (which is included in the blockchain). ST Packets are
intended to be stored on masternodes via some storage service such as DashDrive
(which is out of the scope of this spec).

## Hashing and Serialization

Objects are hashed using double-sha256. All objects to be hashed must use CBOR
encoding as input to the hash function.

In pseudocode this example looks like:

```
const obj = {'dppid': 1234};
const cbor = CBORify(obj);
const theHash = hash(cbor);
```

## Maintainers

[@nmarley](https://github.com/nmarley)

## Contributing

Feel free to dive in! [Open an issue](https://github.com/nmarley/dpp-spec/issues/new) or submit PRs.

## License

[MIT](LICENSE) &copy; Dash Core Group, Inc.
