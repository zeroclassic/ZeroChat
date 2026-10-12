<div align="center">

# ZeroChat

### Freedom to talk.

Blockchain messaging powered by ZeroClassic.

Open ZeroChat (https://zerochat.zeroclassic.org) · ZeroClassic (https://github.com/zeroclassic/ZeroClassic)
</div>

<hr/>

## 💬 What is ZeroChat?

ZeroChat is a blockchain-based messaging platform built to support freedom of expression and reduce dependence on centralized messaging services.

Messages are carried by ZeroClassic transactions. Public conversations are readable on-chain, while private conversations use Sapling shielded addresses to encrypt message contents.

ZeroChat brings public discussions, hashtag rooms, and private messaging together in a simple interface.

## ✨ Features

- Public chat — Join the general discussion using a transparent T1 address.
- Hashtag rooms — Start a message with a #hashtag to create or join a topic.
- Private messaging — Exchange encrypted messages between Sapling zs addresses.
- Pending and confirmed messages — See messages before confirmation and follow their transaction status.
- Stable conversation order — Messages observed by the shared API retain their first-received order, even when blockchain confirmations arrive in a different order.
- Unread indicators — Easily identify new activity in rooms and private conversations.
- Images and clickable links — Open links and choose whether to load externally hosted images.
- Local hide and public reports — Control what appears in your interface.
- Responsive design — Light and dark themes for desktop and mobile screens.

## 🔐 Your keys, your control

Transactions are prepared and signed on your device.

Wallet private keys are not sent to the shared node or API.

The HTTPS API acts as a bridge between the application and the ZeroClassic network. It provides network data and broadcasts transactions that have already been signed locally.

### Android

The Android app works without a ZeroChat account:

- Wallet keys and scan indexes are saved locally.
- The local wallet is encrypted using Android Keystore.
- A device screen lock is required.
- Individual private keys can be explicitly backed up.

> [!WARNING]
> Back up your private keys before funding an address. Uninstalling the Android app, clearing its data, or losing access to the device can result in losing access to your wallet. Exported private-key backups are unencrypted and must be kept secret.

## 🌍 Why ZeroChat?

Public discussion should not depend entirely on a single company, website, or operator.

ZeroChat was created to offer an alternative where messages are recorded on a decentralized blockchain rather than stored exclusively in a platform's private database.

The web interface and shared API make access convenient, but they are not the blockchain itself. Other compatible clients, including full-node software, can access the underlying network independently.

> [!NOTE]
> Censorship resistance is not a guarantee of uninterrupted access. Websites, APIs, and network connections can still be blocked or become unavailable. An interface can hide content without removing its transaction from the blockchain.

## 🛡️ Moderation without deleting blockchain records

ZeroChat supports two forms of content filtering:

### Hide locally

Hide a public message on your own device. Your preference persists across reloads and does not send a transaction.

### Report publicly

Publish an on-chain report identifying the target transaction by its TXID.

The interface hides a message after reports from five distinct verified transparent addresses.

Reports are public transactions and require a transaction fee.

> [!IMPORTANT]
> Hiding or reporting a message does not delete it from the blockchain. Distinct addresses do not necessarily represent distinct people.

## 📱 Platforms and message formats

ZeroChat is available on the web and Android, with support for reading existing Windows message formats.

| Platform | Nickname prefix | Display label |
|:---|:---|:---|
| Web | $nickname$ | Web |
| Android | &nickname& | Android |
| Windows | Existing :nickname: envelopes | win |

The interface displays the nickname, the last four characters of the sender's address, and the declared platform format.

Nicknames are included in message memos rather than retrieved from a shared profile directory.

> [!NOTE]
> Nicknames, short address suffixes, and platform labels are not certified identities. Platform labels describe the message format; they do not prove which application sent the transaction.

## 🚀 Getting started

1. Open ZeroChat (https://zerochat.zeroclassic.org) or install the Android app.
2. Create a dedicated address or import an existing private key.
3. Back up your private key securely.
4. Fund the address with a small amount of ZERC.
5. Use a T1 address for public messages or a Sapling zs address for private conversations.

We recommend using a new address dedicated to messaging rather than your main wallet address.

Imported shielded addresses may require an initial scan before their spendable funds and message history are available. Saved scan indexes help avoid repeating that work.

## ⚙️ How it works

Your device
    │
    ├── Holds wallet keys locally
    ├── Reads and decrypts messages
    └── Prepares and signs transactions
            │
            ▼
       HTTPS API
            │
            ├── Provides blockchain data
            └── Broadcasts signed transactions
                    │
                    ▼
            ZeroClassic network

Sending a message creates a blockchain transaction and requires ZERC for the applicable network fee and burn.

Public messages are readable by anyone with access to the public channel's viewing data. Private Sapling message contents are encrypted and are not publicly readable on blockchain explorers.

## ⚠️ Privacy and security considerations

- **Public messages are public and durable.** Never publish private keys, passwords, or sensitive personal information.
- Shielded messaging protects message contents, but does not guarantee anonymity against every form of network or device observation.
- A compromised device or application can expose wallet keys.
- External images are hosted outside the blockchain. Loading them contacts their hosting provider and may reveal your IP address.
- Transaction confirmation times depend on network conditions.
- Backups remain your responsibility.

---

<div align="center">

### Freedom to talk. Built on ZeroClassic.

**[Join the conversation](https://zerochat.zeroclassic.org)**

</div>
