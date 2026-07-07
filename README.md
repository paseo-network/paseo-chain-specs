# paseo-chain-specs

All chain specification files are hosted **directly in this repository**. Download them from the
`main` branch via the raw URLs below (they are no longer served from external storage).

## Available chain specs

Each chain ships in two flavours: a **full** raw spec for node operators, and a **light-client**
(`.smol`) checkpoint spec for smoldot-based clients. See [Chain Spec Types](#chain-spec-types) below.

| Chain | Chain ID | Para ID | Full spec | Light-client spec |
|-------|----------|---------|-----------|-------------------|
| **Paseo** (relay) | `paseo` | — | [`paseo.raw.json`](./paseo.raw.json) | [`paseo.raw.smol.json`](./paseo.raw.smol.json) |
| **Paseo Asset Hub** | `asset-hub-paseo` | 1000 | _zip archive — see below_ | [`paseo-asset-hub.smol.json`](./paseo-asset-hub.smol.json) |
| **Paseo People** | `paseo-people` | 1004 | [`paseo-people.raw.json`](./paseo-people.raw.json) | [`paseo-people.raw.smol.json`](./paseo-people.raw.smol.json) |
| **Bulletin Paseo** | `bulletin-paseo` | 1010 | [`paseo-bulletin.raw.json`](./paseo-bulletin.raw.json) | _pending — added once the chain is onboarded_ |

Download any file with wget/curl, e.g.:

```bash
wget https://raw.githubusercontent.com/paseo-network/paseo-chain-specs/main/paseo.raw.json
```

> **Asset Hub full-node spec:** the full (non-smoldot) Asset Hub spec is too large to track in
> this repo directly and is distributed as a zip archive:
>
> ```bash
> wget https://github.com/paulormart/ahpaseo-specs/raw/refs/heads/main/paseo-asset-hub-2.json.zip
> ```

> **Substitute-relay relaunch:** Paseo has been relaunched from block 0 with a new genesis
> (`Paseo`, protocol-id `pad`, ss58 `42`). The previous chain specs — the original relay
> (`Paseo Testnet`, protocol-id `pas`, ss58 `0`) and all its system-chain specs — are archived under
> [`paseo-legacy/`](./paseo-legacy) for historical reference. They are **not** the live network; do
> not use them to sync the current Paseo. Additional system-chain specs for the new network will be
> added here as those chains are onboarded.

## Chain Spec Types

This repository contains two types of chain specifications:

- **Full specs** (e.g., `paseo.raw.json`): Standard chain specification files with the full raw
  genesis, for most node operators.
- **Light client friendly specs** (e.g., `paseo.raw.smol.json`): Checkpoint specs (genesis state
  root + a warp-sync `lightSyncState`) optimized for light clients such as smoldot.

## Contributing

### Bootnode Contributions

We welcome bootnode contributions to improve network connectivity! To add your bootnode:

1. Fork this repository
2. Add your bootnode multiaddr to the `bootNodes` array of the appropriate chain spec file(s) —
   add it to **both** the full and light-client spec for a chain (e.g. `paseo.raw.json` and
   `paseo.raw.smol.json`) so the two stay in sync
3. Submit a Pull Request

Your contributions help strengthen the Paseo testnet infrastructure.
