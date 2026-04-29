# Quidli Connect — The Underlying Infrastructure

Quidli Connect (QC) is an open social identity registry & API that maps social accounts to blockchain wallets (EVM & Solana), enabling a new primitive: Wallet Routing.

It allows developers & users to send tokens to people using familiar identifiers (e.g., Telegram username, email address, Farcaster username, X username) instead of encoded string wallet addresses, while keeping the underlying onchain addresses private.

## Core Concept: Wallet Routing

Wallet routing enables users to associate their social accounts/identities with one or more wallets (e.g., one per ecosystem: EVM, Solana).

Instead of sharing a wallet address:
* A user links a wallet to a social handle (e.g., @username on Telegram)
* When a transaction is initiated, QC resolves that identity to the appropriate wallet

Users maintain full control and can:
* Route different social identities to different wallets
* Stay discoverable without exposing managing wallet addresses

## API Infrastructure

Quidli Connect is designed as a developer platform:
* All features are accessible via API
* Powers applications like [quidli.xyz](quidli.xyz), bots, and third-party integrations
* Enables programmable token distribution, identity resolution, and wallet interactions

### Agent-Native Access (x402)

All endpoints are compatible with the x402 payment standard:
* No API key required for agents
* Pay-per-request in stablecoins
* Autonomous access for AI agents & services

## Open Social Registry

Quidli Connect acts as a meta social graph layer:
* Links social accounts to wallets
* Resolves identities across platforms
* Aggregates multiple identity sources into a unified registry

Supported identities include:
* Email, phone number
* Telegram, Discord, X
* Farcaster, Lens Protocol
* ENS, Wallet addresses

This creates a portable & interoperable identity layer across Web 2.0 & web3.

## Frictionless Onboarding

When a recipient has no wallet or account at the time of a transfer:
* A non-custodial wallet is automatically generated
* It is linked to their social identity
* Access is granted once the user authenticates using that same identity

This ensures:
* No lost transfers
* No pre-registration required
* Seamless onboarding

Wallet infrastructure is powered by Privy, while Quidli handles identity resolution & routing.

## Wallet & Identity Management

Users can:
* Connect existing wallets (MetaMask, WalletConnect, Coinbase Wallet, etc.)
* Define a default receiving wallet
* Assign specific wallets to specific social identities
* Fully control routing logic for incoming transactions

Once configured:
Tokens can be sent using a social identifier, QC resolves it to the correct wallet.

## Smart Send (Delegated Transactions)

Quidli Connect introduces Smart Send, enabling delegated transaction execution via the API.

Users can:
* Authorize third parties or applications to send tokens on their behalf.
* Define granular limits (e.g., max tokens per week, per transaction, per recipient).

This enables:
* Automated distributions
* Programmatic payments
* Secure delegation for bots, apps, or agents

## Notifications & Monitoring

Quidli Connect includes a flexible per-wallet notification system.

Users can configure, for each wallet:
* Whether notifications are enabled
* Which blockchains to monitor (Ethereum, Base, Arbitrum, etc.)
* Which events (ERC20 transfers, native tokens, etc.)
* Which delivery channels to use

Notifications are delivered via Quidli-integrated channels:
* Email
* Telegram via Quidli Connect bot
* Discord via Quidli Connect bot
* Farcaster via Quidli Connect mini app

## Reputation Layer (API Accessible)

Quidli Connect integrates a multi-source reputation system, accessible via API.

Reputation scores combine onchain and offchain signals, including (more to come):
* Farcaster Score
* Neynar Score
* Lens Score
* Ethos Score
* World ID (in progress)

This layer enables:
* Trust-aware applications
* Sybil resistance mechanisms
* Smarter targeting and filtering
* Agents interactions

## Why Quidli Connect Matters

By abstracting wallets behind social identity, QC enables:
* Human-readable payments
* Seamless token distribution
* Cross-platform identity interoperability
* Privacy-preserving address management
* Agent-compatible infrastructure

# quidli.xyz — Social Token Distribution Infrastructure

[quidli.xyz](quidli.xyz) is a decentralized application that enables seamless token distribution using social graphs instead of wallet addresses.

It acts as a “Mailchimp for tokens”, allowing users to send, receive, and manage token campaigns as easily as sending a message—without requiring recipients to have prior blockchain knowledge or even a wallet.

## Overview

Quidli is a showcase & GTM app for Quidli Connect, an open social registry that maps social identities to Ethereum wallet addresses.

This introduces a new primitive: Wallet routing via social graphs

Instead of sending tokens to wallet addresses, users can filter for:

- Social contacts
- Community participants
- Onchain audiences (token/NFT holders)

## Key Capabilities

### Social-Based Token Distribution

Send tokens directly through social graphs:

- Telegram contacts or group members
- Farcaster users (e.g., reactions, casts, channels)
- Followers or communities across integrated platforms

No wallet address is required from recipients.

### Advanced Recipient Targeting

Quidli enables powerful filtering mechanisms:

- ERC20 token holders
- NFT holders
- Specific social audiences
- Cross-platform identity matching

This allows highly targeted & programmable distribution campaigns.

### Token Creation & Liquidity

Users can:

- Launch their own tokens directly from [quidli.xyz](quidli.xyz)
- Automatically includes liquidity pools

Token creation is streamlined through integrations like Clanker, reducing the complexity of launching onchain assets.

### Seamless User Experience

Compatible for recipients that:

- Do not need an account
- Do not need prior blockchain knowledge
- Can receive tokens instantly

Wallets are created automatically & tied to their social accounts, enabling timely access without friction.

### Multi-Platform Access

Quidli is designed to meet users where they already are:

- Web: https://quidli.xyz
- Telegram Mini App
- Farcaster Mini App

This ensures distribution can happen natively within social environments, not just on standalone dApps.

### Supported Social Identities

Quidli Connect integrates a wide range of identity layers:

- Email
- Phone number
- X (Twitter)
- Telegram
- Discord
- ENS
- Farcaster
- Lens Protocol
- Wallet addresses
- Multi-Chain Compatibility

### Quidli operates across major EVM ecosystems:

- Ethereum
- Base
- Optimism
- Arbitrum
- World Chain
- Avalanche
- Polygon

This ensures broad reach and composability across the Web3 landscape.

# Quidli architecture

<img width="2724" height="1540" alt="Quidli architecture" src="https://github.com/user-attachments/assets/76dce8f3-6807-4590-914b-9447ff67ee15" />

