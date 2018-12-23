# dpp-spec

> Dash Platform Protocol Specification

The DPP spec defines a protocol for data object which can be stored outside the
blockchain layer, and these objects verified using the blockchain via inclusion
of a cryptographic hash of the data objects into a DIP3 special transaction
(which are indeed part of the Dash blockchain).

## Table of Contents

- [Overview](#overview)
- [Contributing](#contributing)
- [Maintainer](#maintainer)
- [License](#license)

## Overview

The data objects themselves are JSON and validated using the JSONSchema
specification, using pre-defined JSON Schemas which are currently available at:
<https://github.com/dashevo/dpp-schemas/>.

In addition to adherance to pre-defined JSON Schemata, we also define rules for
hashing and serialization of these objects.

## Maintainers

[@nmarley](https://github.com/nmarley)

## Contributing

Feel free to dive in! [Open an issue](https://github.com/nmarley/dpp-spec/issues/new) or submit PRs.

## License

[MIT](LICENSE) &copy; Dash Core Group, Inc.
