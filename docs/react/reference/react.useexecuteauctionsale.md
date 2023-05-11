---
slug: /reference/react.useexecuteauctionsale
title: useExecuteAuctionSale
hide_title: true
displayed_sidebar: react
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

# useExecuteAuctionSale

> This feature is currently in beta and may change based on feedback that we receive.

Execute an auction sale. Can only be executed once the auction has ended and the auction has a winning bid.

## Example

```jsx
const Component = () => {
  const {
    mutate: executeAuctionSale,
    isLoading,
    error,
  } = useExecuteAuctionSale(">>YourMarketplaceContractInstance<<");

  if (error) {
    console.error("failed to execute sale", error);
  }

  return (
    <button
      disabled={isLoading}
      onClick={() => executeAuctionSale({ listingId: 1 })}
    >
      Execute sale
    </button>
  );
};
```

**Signature:**

```typescript
export declare function useExecuteAuctionSale(
  contract: RequiredParam<Marketplace>,
): import("@tanstack/react-query").UseMutationResult<
  import("@ethersproject/abstract-provider").TransactionReceipt,
  unknown,
  ExecuteAuctionSale,
  unknown
>;
```

## Parameters

| Parameter | Type                                                         | Description                           |
| --------- | ------------------------------------------------------------ | ------------------------------------- |
| contract  | [RequiredParam](./react.requiredparam.md)&lt;Marketplace&gt; | an instance of a Marketplace contract |

**Returns:**

import("@tanstack/react-query").UseMutationResult&lt;import("@ethersproject/abstract-provider").TransactionReceipt, unknown, [ExecuteAuctionSale](./react.executeauctionsale.md), unknown&gt;

a mutation object that can be used to accept an offer on a direct listing