# Change log

All notable changes to the project will be documented in this file. This project adheres to [Semantic Versioning](http://semver.org).

## [0.12.0](https://github.com/launchdarkly/rust-eventsource-client/compare/0.11.0...0.12.0) (2023-11-15)


### ⚠ BREAKING CHANGES

* Remove re-export of hyper_rustls types ([#59](https://github.com/launchdarkly/rust-eventsource-client/issues/59))
* Bump dependencies ([#58](https://github.com/launchdarkly/rust-eventsource-client/issues/58))

### deps

* Bump dependencies ([#58](https://github.com/launchdarkly/rust-eventsource-client/issues/58)) ([a7174e3](https://github.com/launchdarkly/rust-eventsource-client/commit/a7174e328f168af0a96f8c9671453a29c028d0f0))


### Features

* make Error implement std::fmt::Display, std::error::Error` and Sync  ([#47](https://github.com/launchdarkly/rust-eventsource-client/issues/47)) ([0eaab6e](https://github.com/launchdarkly/rust-eventsource-client/commit/0eaab6eefb8d69aac01ded4ab53c527c84084ba6))


### Bug Fixes

* Remove re-export of hyper_rustls types ([#59](https://github.com/launchdarkly/rust-eventsource-client/issues/59)) ([ec24970](https://github.com/launchdarkly/rust-eventsource-client/commit/ec24970d4a9ed875a44fb9c84c67b587d46ca23d))

## [0.11.0] - 2022-11-07
### Fixed:
- Add missing retry interval reset behavior.
- Add missing jitter to retry strategy.

## [0.10.2] - 2022-10-28
### Fixed:
- Correctly handle comment payloads.

## [0.10.1] - 2022-04-14
### Fixed:
- Comment events were incorrectly consuming non-comment event data. Now comment events are emitted as they are parsed and can no longer affect non-comment event data.

## [0.10.0] - 2022-03-23
### Added:
- Added support for following 301 & 307 redirects with configurable redirect limit.

### Fixed:
- Fixed `Last-Event-ID` handling when server sends explicit empty ID.

## [0.9.0] - 2022-03-15
### Added:
- Added support for SSE test harness.

### Changed:
- Change `ClientBuilder` to return `impl Client`, where `Client` is a sealed trait that exposes a `stream()` method. 

### Fixed:
- Fixed various bugs related to SSE protocol.

## [0.8.2] - 2022-02-03
### Added:
- Support for creating an event source client with a pre-configured connection.

## [0.8.1] - 2022-01-19
### Changed:
- Added missing changelog
- Fixed keyword for crates.io publishing

## [0.8.0] - 2022-01-19
### Changed:
- Introduced new Error variant
