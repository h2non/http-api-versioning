# HTTP API Versioning

This document aims to analysis and provide a discussion frame about multiple HTTP API versioning design approachs and strategies.

**This is a work in progress**

## Introduction

I think that software is social by nature. Software is about mainly building abstract things that a computer can understand. Software is also about interfaces. Interfaces are an concrete and mostly consistent way to give the hability to the software to became social, and therefore, talk with other software based components.

## Motivation

This repository aims to collect and provide an open debate 
about design best practices and approachs for a consistent HTTP API versioning

Additionally, it aims to mitigate your dilemmas about it, and avoid unproductive 
chats with your team about this kind of decissions.

## Rationale

The idea about creating an specific documentation for this topic was originated as result of a [discusision thread](https://github.com/interagent/http-api-design/issues/8) at [http-api-design](https://github.com/interagent/http-api-design) repository.

## Versioning strategies

### Custom Header

Using `Version` or `X-Version` headers

Example:
```
HTTP/1.1
GET /resource
Version: 1.0
```

#### Pros

- More explitict Explicit

#### Cons

### Accept header

Proposed mechanism from http-api-design.

Example:
```
HTTP/1.1
GET /resource
Accept: application/json; version=1.0
```

### URI path

Example:
```
HTTP/1.1
GET /v1/resource
```

## License

Copyright the [project contributors](CONTRIBUTORS.md).

Released under a [Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/).
