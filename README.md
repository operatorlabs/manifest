# Agent Manifest Standard

A lightweight standard for defining AI agent identities across platforms.

## Overview
An Agent Manifest defines the identity of an AI agent by specifying its visual representation, description, blockchain addresses, social accounts, and other important links. The manifest is minimal by design and platform-agnostic.

## Getting Started
1. Create a new JSON file named `manifest.json`
2. Copy the example manifest below and customize it for your AI agent
3. Validate that your JSON is properly formatted

## Example Manifest
```json
{
  "avatar": "https://www.daos.fun/assets/ai16z.jpeg",
  "description": "ai16z is the first venture capital firm led by AI agents.",
  "instructions": "You can buy ai16z tokens on the Solana blockchain at daos.fun.",
  "addresses": [
    {
      "chain": "solana",
      "address": "HeLp6NuQkmYB4pYWo2zYs22mESHXPQYzXbB8n4V98jwC",
      "description": "CA"
    }
  ],
  "social": [
    {
      "platform": "github",
      "id": "ai16z",
      "description": "Source Code"
    }
  ],
  "uris": [
    {
      "uri": "https://discord.com/invite/ai16z",
      "description": "Discord Invite"
    }
  ]
}
```

## Field Specifications

### Required Fields
- **avatar**: URL linking to the agent's visual representation
- **description**: Summary of the agent's purpose and mission
- **instructions**: Guidelines for how to interact with the agent

### Optional Arrays
If not needed, use empty arrays (`[]`) for:
- **addresses**: Blockchain addresses
- **social**: Social media profiles  
- **uris**: Resource links

### Address Object
```json
{
  "chain": "solana",        // See chains dictionary below
  "address": "Abc123...",   // Case-sensitive
  "description": "CA"       // Standard keywords: CA, NFT, wallet
}
```

### Social Object
```json
{
  "platform": "github",     // See social platforms dictionary
  "id": "username",        // Case-insensitive, no @ symbol
  "description": "label"    // Purpose/instructions for the account
}
```

### URI Object
```json
{
  "uri": "https://...",    // URL, IPFS hash, etc.
  "description": "label"   // Purpose of the resource
}
```

## Standard Keywords

### Address Descriptions

#### CA (Contract Address)
```json
{
  "chain": "solana",
  "address": "HeLp6NuQkmYB4pYWo2zYs22mESHXPQYzXbB8n4V98jwC",
  "description": "CA"
}
```

#### NFT (Collection)
```json
{
  "chain": "polygon",
  "address": "0x3258838E15DA1815784482318C165683CB8Cd5d4",
  "description": "NFT"
}
```

#### Wallet
```json
{
  "chain": "polygon",
  "address": "0x1f2dd6d473f3e824cd2f8a89d9c69fb96f6ad0cf",
  "description": "wallet"
}
```

## Standard Dictionary
> Note: To add new chains to the dictionary, please open an issue.

### Chains
```json
{
  "ethereum": "Ethereum Mainnet",
  "solana": "Solana Mainnet",
  "arbitrum": "Arbitrum One",
  "optimism": "Optimism Mainnet",
  "base": "Base",
  "polygon": "Polygon PoS",
  "bsc": "BNB Smart Chain",
  "avalanche": "Avalanche C-Chain",
  "gnosis": "Gnosis Chain",
  "zksync": "zkSync Era",
  "cosmos": "Cosmos Hub",
  "near": "Near Mainnet",
  "aptos": "Aptos Mainnet",
  "sui": "Sui Mainnet",
  "bitcoin": "Bitcoin",
  "starknet": "Starknet"
}
```

### Social Platforms
```json
{
  "github": "GitHub",
  "x": "Twitter/X",
  "discord": "Discord",
  "ens": "Ethereum Name Service",
  "telegram": "Telegram",
  "lens": "Lens Protocol",
  "reddit": "Reddit",
  "medium": "Medium",
  "linkedin": "LinkedIn",
  "youtube": "YouTube",
  "tiktok": "TikTok",
  "farcaster": "Farcaster",
  "instagram": "Instagram",
  "bluesky": "Bluesky",
  "paragraph": "Paragraph"
}
```

## Adoption
- [operator.io](https://operator.io) - The first platform to implement the manifest standard

