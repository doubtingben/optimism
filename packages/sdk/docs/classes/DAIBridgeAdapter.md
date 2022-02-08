[@eth-optimism/sdk](../README.md) / [Exports](../modules.md) / DAIBridgeAdapter

# Class: DAIBridgeAdapter

Bridge adapter for DAI.

## Hierarchy

- [`StandardBridgeAdapter`](StandardBridgeAdapter.md)

  ↳ **`DAIBridgeAdapter`**

## Table of contents

### Constructors

- [constructor](DAIBridgeAdapter.md#constructor)

### Properties

- [estimateGas](DAIBridgeAdapter.md#estimategas)
- [l1Bridge](DAIBridgeAdapter.md#l1bridge)
- [l2Bridge](DAIBridgeAdapter.md#l2bridge)
- [messenger](DAIBridgeAdapter.md#messenger)
- [populateTransaction](DAIBridgeAdapter.md#populatetransaction)

### Methods

- [deposit](DAIBridgeAdapter.md#deposit)
- [getDepositsByAddress](DAIBridgeAdapter.md#getdepositsbyaddress)
- [getTokenBridgeMessagesByAddress](DAIBridgeAdapter.md#gettokenbridgemessagesbyaddress)
- [getWithdrawalsByAddress](DAIBridgeAdapter.md#getwithdrawalsbyaddress)
- [supportsTokenPair](DAIBridgeAdapter.md#supportstokenpair)
- [withdraw](DAIBridgeAdapter.md#withdraw)

## Constructors

### constructor

• **new DAIBridgeAdapter**(`opts`)

Creates a StandardBridgeAdapter instance.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `opts` | `Object` | Options for the adapter. |
| `opts.l1Bridge` | [`AddressLike`](../modules.md#addresslike) | L1 bridge contract. |
| `opts.l2Bridge` | [`AddressLike`](../modules.md#addresslike) | L2 bridge contract. |
| `opts.messenger` | [`ICrossChainMessenger`](../interfaces/ICrossChainMessenger.md) | Provider used to make queries related to cross-chain interactions. |

#### Inherited from

[StandardBridgeAdapter](StandardBridgeAdapter.md).[constructor](StandardBridgeAdapter.md#constructor)

#### Defined in

[packages/sdk/src/adapters/standard-bridge.ts:37](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/adapters/standard-bridge.ts#L37)

## Properties

### estimateGas

• **estimateGas**: `Object`

Object that holds the functions that estimates the gas required for a given transaction.
Follows the pattern used by ethers.js.

#### Type declaration

| Name | Type |
| :------ | :------ |
| `deposit` | (`l1Token`: [`AddressLike`](../modules.md#addresslike), `l2Token`: [`AddressLike`](../modules.md#addresslike), `amount`: [`NumberLike`](../modules.md#numberlike), `opts?`: { `l2GasLimit?`: [`NumberLike`](../modules.md#numberlike) ; `overrides?`: `Overrides` ; `recipient?`: [`AddressLike`](../modules.md#addresslike)  }) => `Promise`<`BigNumber`\> |
| `withdraw` | (`l1Token`: [`AddressLike`](../modules.md#addresslike), `l2Token`: [`AddressLike`](../modules.md#addresslike), `amount`: [`NumberLike`](../modules.md#numberlike), `opts?`: { `overrides?`: `Overrides` ; `recipient?`: [`AddressLike`](../modules.md#addresslike)  }) => `Promise`<`BigNumber`\> |

#### Inherited from

[StandardBridgeAdapter](StandardBridgeAdapter.md).[estimateGas](StandardBridgeAdapter.md#estimategas)

#### Defined in

[packages/sdk/src/adapters/standard-bridge.ts:307](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/adapters/standard-bridge.ts#L307)

___

### l1Bridge

• **l1Bridge**: `Contract`

L1 bridge contract.

#### Inherited from

[StandardBridgeAdapter](StandardBridgeAdapter.md).[l1Bridge](StandardBridgeAdapter.md#l1bridge)

#### Defined in

[packages/sdk/src/adapters/standard-bridge.ts:26](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/adapters/standard-bridge.ts#L26)

___

### l2Bridge

• **l2Bridge**: `Contract`

L2 bridge contract.

#### Inherited from

[StandardBridgeAdapter](StandardBridgeAdapter.md).[l2Bridge](StandardBridgeAdapter.md#l2bridge)

#### Defined in

[packages/sdk/src/adapters/standard-bridge.ts:27](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/adapters/standard-bridge.ts#L27)

___

### messenger

• **messenger**: [`ICrossChainMessenger`](../interfaces/ICrossChainMessenger.md)

Provider used to make queries related to cross-chain interactions.

#### Inherited from

[StandardBridgeAdapter](StandardBridgeAdapter.md).[messenger](StandardBridgeAdapter.md#messenger)

#### Defined in

[packages/sdk/src/adapters/standard-bridge.ts:25](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/adapters/standard-bridge.ts#L25)

___

### populateTransaction

• **populateTransaction**: `Object`

Object that holds the functions that generate transactions to be signed by the user.
Follows the pattern used by ethers.js.

#### Type declaration

| Name | Type |
| :------ | :------ |
| `deposit` | (`l1Token`: [`AddressLike`](../modules.md#addresslike), `l2Token`: [`AddressLike`](../modules.md#addresslike), `amount`: [`NumberLike`](../modules.md#numberlike), `opts?`: { `l2GasLimit?`: [`NumberLike`](../modules.md#numberlike) ; `overrides?`: `Overrides` ; `recipient?`: [`AddressLike`](../modules.md#addresslike)  }) => `Promise`<`TransactionRequest`\> |
| `withdraw` | (`l1Token`: [`AddressLike`](../modules.md#addresslike), `l2Token`: [`AddressLike`](../modules.md#addresslike), `amount`: [`NumberLike`](../modules.md#numberlike), `opts?`: { `overrides?`: `Overrides` ; `recipient?`: [`AddressLike`](../modules.md#addresslike)  }) => `Promise`<`TransactionRequest`\> |

#### Inherited from

[StandardBridgeAdapter](StandardBridgeAdapter.md).[populateTransaction](StandardBridgeAdapter.md#populatetransaction)

#### Defined in

[packages/sdk/src/adapters/standard-bridge.ts:236](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/adapters/standard-bridge.ts#L236)

## Methods

### deposit

▸ **deposit**(`l1Token`, `l2Token`, `amount`, `signer`, `opts?`): `Promise`<`TransactionResponse`\>

Deposits some tokens into the L2 chain.

#### Parameters

| Name | Type |
| :------ | :------ |
| `l1Token` | [`AddressLike`](../modules.md#addresslike) |
| `l2Token` | [`AddressLike`](../modules.md#addresslike) |
| `amount` | [`NumberLike`](../modules.md#numberlike) |
| `signer` | `Signer` |
| `opts?` | `Object` |
| `opts.l2GasLimit?` | [`NumberLike`](../modules.md#numberlike) |
| `opts.overrides?` | `Overrides` |
| `opts.recipient?` | [`AddressLike`](../modules.md#addresslike) |

#### Returns

`Promise`<`TransactionResponse`\>

Transaction response for the deposit transaction.

#### Inherited from

[StandardBridgeAdapter](StandardBridgeAdapter.md).[deposit](StandardBridgeAdapter.md#deposit)

#### Defined in

[packages/sdk/src/adapters/standard-bridge.ts:205](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/adapters/standard-bridge.ts#L205)

___

### getDepositsByAddress

▸ **getDepositsByAddress**(`address`, `opts?`): `Promise`<[`TokenBridgeMessage`](../interfaces/TokenBridgeMessage.md)[]\>

Gets all deposits for a given address.

#### Parameters

| Name | Type |
| :------ | :------ |
| `address` | [`AddressLike`](../modules.md#addresslike) |
| `opts?` | `Object` |
| `opts.fromBlock?` | `BlockTag` |
| `opts.toBlock?` | `BlockTag` |

#### Returns

`Promise`<[`TokenBridgeMessage`](../interfaces/TokenBridgeMessage.md)[]\>

All deposit token bridge messages sent by the given address.

#### Inherited from

[StandardBridgeAdapter](StandardBridgeAdapter.md).[getDepositsByAddress](StandardBridgeAdapter.md#getdepositsbyaddress)

#### Defined in

[packages/sdk/src/adapters/standard-bridge.ts:80](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/adapters/standard-bridge.ts#L80)

___

### getTokenBridgeMessagesByAddress

▸ **getTokenBridgeMessagesByAddress**(`address`, `opts?`): `Promise`<[`TokenBridgeMessage`](../interfaces/TokenBridgeMessage.md)[]\>

Finds all cross chain messages that correspond to token deposits or withdrawals sent by a
particular address. Useful for finding deposits/withdrawals because the sender of the message
will appear to be the StandardBridge contract and not the actual end user.

#### Parameters

| Name | Type |
| :------ | :------ |
| `address` | [`AddressLike`](../modules.md#addresslike) |
| `opts?` | `Object` |
| `opts.direction?` | [`MessageDirection`](../enums/MessageDirection.md) |

#### Returns

`Promise`<[`TokenBridgeMessage`](../interfaces/TokenBridgeMessage.md)[]\>

All token bridge messages sent by the given address.

#### Inherited from

[StandardBridgeAdapter](StandardBridgeAdapter.md).[getTokenBridgeMessagesByAddress](StandardBridgeAdapter.md#gettokenbridgemessagesbyaddress)

#### Defined in

[packages/sdk/src/adapters/standard-bridge.ts:55](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/adapters/standard-bridge.ts#L55)

___

### getWithdrawalsByAddress

▸ **getWithdrawalsByAddress**(`address`, `opts?`): `Promise`<[`TokenBridgeMessage`](../interfaces/TokenBridgeMessage.md)[]\>

Gets all withdrawals for a given address.

#### Parameters

| Name | Type |
| :------ | :------ |
| `address` | [`AddressLike`](../modules.md#addresslike) |
| `opts?` | `Object` |
| `opts.fromBlock?` | `BlockTag` |
| `opts.toBlock?` | `BlockTag` |

#### Returns

`Promise`<[`TokenBridgeMessage`](../interfaces/TokenBridgeMessage.md)[]\>

All withdrawal token bridge messages sent by the given address.

#### Inherited from

[StandardBridgeAdapter](StandardBridgeAdapter.md).[getWithdrawalsByAddress](StandardBridgeAdapter.md#getwithdrawalsbyaddress)

#### Defined in

[packages/sdk/src/adapters/standard-bridge.ts:123](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/adapters/standard-bridge.ts#L123)

___

### supportsTokenPair

▸ **supportsTokenPair**(`l1Token`, `l2Token`): `Promise`<`boolean`\>

Checks whether the given token pair is supported by the bridge.

#### Parameters

| Name | Type |
| :------ | :------ |
| `l1Token` | [`AddressLike`](../modules.md#addresslike) |
| `l2Token` | [`AddressLike`](../modules.md#addresslike) |

#### Returns

`Promise`<`boolean`\>

Whether the given token pair is supported by the bridge.

#### Overrides

[StandardBridgeAdapter](StandardBridgeAdapter.md).[supportsTokenPair](StandardBridgeAdapter.md#supportstokenpair)

#### Defined in

[packages/sdk/src/adapters/dai-bridge.ts:13](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/adapters/dai-bridge.ts#L13)

___

### withdraw

▸ **withdraw**(`l1Token`, `l2Token`, `amount`, `signer`, `opts?`): `Promise`<`TransactionResponse`\>

Withdraws some tokens back to the L1 chain.

#### Parameters

| Name | Type |
| :------ | :------ |
| `l1Token` | [`AddressLike`](../modules.md#addresslike) |
| `l2Token` | [`AddressLike`](../modules.md#addresslike) |
| `amount` | [`NumberLike`](../modules.md#numberlike) |
| `signer` | `Signer` |
| `opts?` | `Object` |
| `opts.overrides?` | `Overrides` |
| `opts.recipient?` | [`AddressLike`](../modules.md#addresslike) |

#### Returns

`Promise`<`TransactionResponse`\>

Transaction response for the withdraw transaction.

#### Inherited from

[StandardBridgeAdapter](StandardBridgeAdapter.md).[withdraw](StandardBridgeAdapter.md#withdraw)

#### Defined in

[packages/sdk/src/adapters/standard-bridge.ts:221](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/adapters/standard-bridge.ts#L221)
