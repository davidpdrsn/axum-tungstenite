# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

# Unreleased

- None.

# 0.3.0 (02. August, 2022)

- **changed:** Update to tokio-tungstenite 0.20 ([#9])

[#9]: https://github.com/davidpdrsn/axum-tungstenite/pull/9

# 0.2.0 (10. December, 2022)

- **changed:** Update to axum-core 0.3, which requires axum 0.6 ([#6])
- **changed:** Update to tokio-tungstenite 0.18 ([#6])
- **added:** Allow configuration of client frame masking ([#3])
- **added:** Add `on_failed_upgrade` callback to `WebSocketUpgrade` ([#7])

[#3]: https://github.com/davidpdrsn/axum-tungstenite/pull/3
[#6]: https://github.com/davidpdrsn/axum-tungstenite/pull/6
[#7]: https://github.com/davidpdrsn/axum-tungstenite/pull/7

# 0.1.0 (15. May, 2022)

- Initial release.
