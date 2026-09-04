# TronForged releases

Release binaries for **TronForged**, the shop-hosted RMM / PSA platform for computer repair shops.
This repository holds **release assets only**; the product source lives in a separate private repository.

## Getting TronForged

Download the newest `TronForged-<version>.exe` from the **Latest** release. That one file is the whole
product: run it on any Windows 10/11 PC to install a console there (it checks this feed first and
fetches a newer release if one has been published, so a stale download never installs a stale console).

Every release carries exactly four assets:

| asset | what it is |
| --- | --- |
| `TronForged-<version>.exe` | the console installer (technician / customer / server console) |
| `TronForged-<version>.exe.sha256` | its SHA-256, as `sha256sum` writes it |
| `TronForged.Server-<version>.exe` | the shop server program (installed from the Server Console) |
| `TronForged.Server-<version>.exe.sha256` | its SHA-256 |

Shop servers pull new releases from this feed into their own signed update catalog, and enrolled
consoles update from their shop server, never from here directly. The installer verifies every download
against the `.sha256` beside it before running it.

The binaries are not yet code-signed; expect the SmartScreen "unrecognized app" prompt.
