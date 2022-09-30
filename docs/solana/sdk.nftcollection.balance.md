---
slug: /sdk.nftcollection.balance
title: NFTCollection.balance() method
hide_title: true
displayed_sidebar: solana
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

## NFTCollection.balance() method

Get the NFT balance of the connected wallet

**Signature:**

```typescript
balance(nftAddress: string): Promise<number>;
```

## Parameters

| Parameter  | Type   | Description |
| ---------- | ------ | ----------- |
| nftAddress | string |             |

**Returns:**

Promise&lt;number&gt;

the NFT balance

## Example

```jsx
// The mint address of the NFT to check the balance of
const mintAddress = "...";
// Get the NFT balance of the currently connected wallet
const balance = await program.balance(mintAddress);
console.log(balance);
```