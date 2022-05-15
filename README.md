# axum-tungstenite

WebSocket connections for [axum] directly using [tungstenite].

[![CI](https://github.com/davidpdrsn/axum-tungstenite/actions/workflows/CI.yaml/badge.svg)](https://github.com/davidpdrsn/axum-tungstenite/actions/workflows/CI.yaml)
[![Crates.io](https://img.shields.io/crates/v/axum-tungstenite)](https://crates.io/crates/axum-tungstenite)
[![Documentation](https://docs.rs/axum-tungstenite/badge.svg)](https://docs.rs/axum-tungstenite)

More information about this crate can be found in the [crate documentation][docs].

# Differences from `axum::extract::ws`

axum already supports WebSockets through [`axum::extract::ws`]. However the fact that axum uses
tungstenite under the hood is a private implementation detail. Thus axum doesn't directly
expose types from tungstenite, such as [`tungstenite::Error`] and [`tungstenite::Message`].
This allows axum to update to a new major version of tungstenite in a new minor version of
axum, which leads to greater API stability.

This library works differently as it directly uses the types from tungstenite in its public
API. That makes some things simpler but also means axum-tungstenite will receive a new major
version when tungstenite does.

# Which should you choose?

By default you should use `axum::extract::ws` unless you specifically need something from
tungstenite and don't mind keeping up with additional breaking changes.

## Safety

This crate uses `#![forbid(unsafe_code)]` to ensure everything is implemented in
100% safe Rust.

## License

This project is licensed under the [MIT license][license].

[docs]: https://docs.rs/axum-tungstenite
[license]: https://github.com/davidpdrsn/axum-tungstenite/blob/main/LICENSE
[axum]: https://crates.io/crates/axum
[tungstenite]: https://crates.io/crates/tungstenite
[`axum::extract::ws`]: https://docs.rs/axum/latest/axum/extract/ws/index.html
[`tungstenite::Error`]: https://docs.rs/tungstenite/latest/tungstenite/error/enum.Error.html
[`tungstenite::Message`]: https://docs.rs/tungstenite/latest/tungstenite/enum.Message.html
