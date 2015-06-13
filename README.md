# HTTP API versioning

This document aims to analyze and provide a discussion frame for multiple HTTP API versioning design approachs and strategies.

**This is a work in progress**

## Introduction

I believe that software is social by nature. Software is about building abstract things that a computer can understand. Software is also about interfaces. Interfaces are a concrete and consistent provided by software components to achieve the hability to became social, and therefore, getting the hability to interchange information with other software components.

## Motivation

This repository aims to collect and provide an open debate 
about design best practices and approachs for a consistent HTTP API versioning

Additionally, the goal is to mitigate common dilemmas about how to apply a proper HTTP versioning, and avoid unproductive and repetivie chats with your team about this kind of decissions.

The idea about creating an specific documentation for this topic was originated as result of a [discusision thread](https://github.com/interagent/http-api-design/issues/8) at [http-api-design](https://github.com/interagent/http-api-design) repository.

## Strategies

### Custom Header

Using `Version` or `X-Version` headers

Example:
```
GET /resource HTTP/1.1
Version: 1.0
```

#### Pros

- More explitict Explicit.
- HTTP is an extensible application protocol. Adding custom headers is fine.

#### Cons

- No fully HTTP standard focused.
- All the HTTP must have the ability to add custom headers.

### Accept header

Proposed mechanism from http-api-design.

Example:
```
GET /resource HTTP/1.1
Accept: application/json; version=1.0
```

### URI path

Example:
```
GET /v1/resource HTTP/1.1
```

## License

Copyright the [project contributors](CONTRIBUTORS.md).

Released under a [Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/).
