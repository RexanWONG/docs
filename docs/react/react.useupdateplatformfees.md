---
slug: /react.useupdateplatformfees
title: useUpdatePlatformFees() function
hide_title: true
displayed_sidebar: react
---
<!-- Do not edit this file. It is automatically generated by API Documenter. -->


## useUpdatePlatformFees() function

> This feature is currently in beta and may change based on feedback that we receive.
> 

Use this to update the platform fees settings of your 

## Example


```jsx
const Component = () => {
  const {
    mutate: updatePlatformFees,
    isLoading,
    error,
  } = useUpdatePlatformFees(SmartContract);

  if (error) {
    console.error("failed to update platform fees", error);
  }

  return (
    <button
      disabled={isLoading}
      onClick={() => updatePlatformFees({ updatePayload: { fee_recipient: "0x123", platform_fee_basis_points: 5_00 } })}
    >
      Update Platform fees
    </button>
  );
};
```

**Signature:**

```typescript
export declare function useUpdatePlatformFees(contract: RequiredParam<ValidContractInstance>): import("@tanstack/react-query").UseMutationResult<Omit<{
    receipt: import("@ethersproject/abstract-provider").TransactionReceipt;
    data: () => Promise<unknown>;
}, "data">, unknown, {
    platform_fee_basis_points?: number | undefined;
    fee_recipient?: string | undefined;
}, unknown>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  contract | [RequiredParam](./react.requiredparam.md)&lt;ValidContractInstance&gt; | an instance of a  |

**Returns:**

import("@tanstack/react-query").UseMutationResult&lt;Omit&lt;{ receipt: import("@ethersproject/abstract-provider").TransactionReceipt; data: () =&gt; Promise&lt;unknown&gt;; }, "data"&gt;, unknown, { platform\_fee\_basis\_points?: number \| undefined; fee\_recipient?: string \| undefined; }, unknown&gt;

a mutation object that can be used to update the platform fees settings