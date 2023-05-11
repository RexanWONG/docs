---
slug: /reference/sdk.nft
title: NFT type
hide_title: true
displayed_sidebar: typescript
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

# NFT type

**Signature:**

```typescript
export type NFT = {
  metadata: NFTMetadata;
  owner: string;
  type: "ERC1155" | "ERC721" | "metaplex";
  supply: number;
  quantityOwned?: number;
};
```

**References:** [NFTMetadata](./sdk.nftmetadata.md)