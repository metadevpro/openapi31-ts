# OpenApi31-TS

TypeScript help library to help building **OpenAPI 3.1.x** compliant API contracts.

For **OpenAPI 3.0.x** contracts see instead: [openapi3-ts](https://github.com/metadevpro/openapi3-ts).

[![Coverage Status](https://coveralls.io/repos/github/metadevpro/openapi31-ts/badge.svg?branch=master)](https://coveralls.io/github/metadevpro/openapi31-ts?branch=master)
[![Known Vulnerabilities](https://snyk.io/test/github/metadevpro/openapi31-ts/badge.svg?targetFile=package.json)](https://snyk.io/test/github/metadevpro/openapi31-ts?targetFile=package.json)
[![npm version](https://badge.fury.io/js/openapi31-ts.svg)](http://badge.fury.io/js/openapi31-ts)

[![NPM](https://nodei.co/npm/openapi31-ts.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/openapi31-ts/)

## How to use

This library provides an internal DSL and Typescript interfaces to help to build and produce OpenAPI Specfications and to format them as JSON and YAML.

See the test in the `*.spec.ts` files to see how to use it.

## Main differences between OpenAPI 3.0 and OpenAPI 3.1

For working with [OpenAPI v. 3.1.0](https://github.com/OAI/OpenAPI-Specification/blob/main/versions/3.1.0.md) use this library, for [OpenAPI 3.0.0](https://github.com/OAI/OpenAPI-Specification/blob/main/versions/3.0.0.md) use this other twin one: [openapi3-ts](https://github.com/metadevpro/openapi3-ts).

Main differences in implementation are:

1. Semantic version is dropped.
2. Different JSON Schema rules applies (this library is not providing support for JSON Schema validation).
    - OpenAPI 3.0.0 uses [JSON Schema Specification Wright Draft 00](https://datatracker.ietf.org/doc/html/draft-wright-json-schema-00#section-4.2)
    - OpenAPI 3.1.0 uses [JSON Schema Specification Draft 2020-12](https://datatracker.ietf.org/doc/html/draft-bhutton-json-schema-00#section-4.2.1)
3. Derived from the JSON Schema version change:
    - `exclusiveMaximum` was a `boolean` on OpenAPI 3.0, now is a number in OpenAPI 3.1.
    - `exclusiveMinimum` was a `boolean` on OpenAPI 3.0, now is a number in OpenAPI 3.1.
4. Added support for Webhooks on OpenAPI 3.1.0
5. Single `example` is deprecated in favour of `examples`.
6. Type can now be an array.
7. Type can be null with: `nullable: true`.
8. Paths are optional.

[Read](https://blog.stoplight.io/difference-between-open-v2-v3-v31) for a more detailed comparison.

## Includes

* `/src/model` TS typed interfaces for helping building a contract.
* `/src/dsl` Fluent DSL for building a contract.

## Install

Install package via **npm**:

```bash
npm i --save openapi31-ts
```

## Versions and Changelog

See [changelog](Changelog.md).

## References

* OpenAPI spec 3.1.0. [https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.1.0.md](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.1.0.md)

## License

Licensed under the MIT License.

## Credits

**Contact:** Pedro J. Molina | github: [pjmolina](https://github.com/pjmolina) | twitter: [pmolinam](https://twitter.com/pmolinam)

(c) 2017-2023. [Pedro J. Molina](http://pjmolina.com) at Metadev S.L. [https://metadev.pro](https://metadev.pro) & contributors.
