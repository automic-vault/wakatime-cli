# Automic Vault Fork Notes

This repository is the Automic Vault fork of WakaTime CLI.

Automic Vault is a macOS-first system that keeps developer credentials in
custody and applies them only after policy or the user allows the complete
operation requested by verified software.

The [WakaTime CLI Hardener work](https://github.com/automic-vault/automic-vault/issues/186)
uses WakaTime's API-key vault boundary without leaving API keys in plaintext
configuration. This fork validates the effective API destination, key sources,
proxy, and TLS posture before invoking Automic Vault directly; project config
cannot silently redirect an Automic Vault credential.

Automic Vault's reviewed release process builds and signs the executable with
Hardened Runtime and no entitlements. This source fork alone does not establish
Hardened State. The remainder of this README is the original upstream README.

---

# WakaTime CLI

[![Tests](https://img.shields.io/github/actions/workflow/status/wakatime/wakatime-cli/on_push.yml?branch=develop&label=tests)](https://github.com/wakatime/wakatime-cli/actions)
[![Coverage](https://img.shields.io/codecov/c/gh/wakatime/wakatime-cli/develop)](https://codecov.io/gh/wakatime/wakatime-cli)
[![Downloads](https://img.shields.io/github/downloads/wakatime/wakatime-cli/total?color=007ec6)](https://github.com/wakatime/wakatime-cli/releases)
[![wakatime](https://wakatime.com/badge/github/wakatime/wakatime-cli.svg)](https://wakatime.com)

Command line interface to [WakaTime][wakatime] used by all WakaTime [text editor plugins][editors].

Go to [http://wakatime.com/editors][editors] to install the plugin for your text editor or IDE.

## Usage

Normally you don't need to use wakatime-cli directly unless you're building a new WakaTime plugin.
If you're building a plugin using the [WakaTime API][api], follow the [Creating a Plugin][creating-plugin] guide.

WakaTime plugins and wakatime-cli share a common [INI][usage] config file:

`$WAKATIME_HOME/.wakatime.cfg`

IDE plugins log to the IDE’s console, and wakatime-cli writes JSONL logs to:

`$WAKATIME_HOME/.wakatime/wakatime.log`

With the `~/.wakatime.cfg` config `debug = true` enabling verbose logs.

See [Usage][usage] or the [WakaTime FAQ][faq] for more details.

## Contributing

Pull requests and issues are welcome!
See [Contributing][contributing] for more details.

## Troubleshooting

See [Troubleshooting][troubleshooting] for more details.

Many thanks to all [contributors][authors]!

Made with :heart: by the WakaTime Team.

[wakatime]: http://wakatime.com
[editors]: http://wakatime.com/editors
[api]: https://wakatime.com/developers/
[creating-plugin]: https://wakatime.com/help/misc/creating-plugin
[faq]: https://wakatime.com/faq
[usage]: USAGE.md
[contributing]: CONTRIBUTING.md
[troubleshooting]: TROUBLESHOOTING.md
[authors]: AUTHORS
