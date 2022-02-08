[@eth-optimism/sdk](../README.md) / [Exports](../modules.md) / L2Provider

# Interface: L2Provider

Represents an extended version of an normal ethers Provider that returns additional L2 info and
has special functions for L2-specific interactions.

## Hierarchy

- `Provider`

  ↳ **`L2Provider`**

## Table of contents

### Properties

- [\_isProvider](L2Provider.md#_isprovider)

### Methods

- [addListener](L2Provider.md#addlistener)
- [call](L2Provider.md#call)
- [emit](L2Provider.md#emit)
- [estimateGas](L2Provider.md#estimategas)
- [estimateL1Gas](L2Provider.md#estimatel1gas)
- [estimateL1GasCost](L2Provider.md#estimatel1gascost)
- [estimateL2GasCost](L2Provider.md#estimatel2gascost)
- [estimateTotalGasCost](L2Provider.md#estimatetotalgascost)
- [getBalance](L2Provider.md#getbalance)
- [getBlock](L2Provider.md#getblock)
- [getBlockNumber](L2Provider.md#getblocknumber)
- [getBlockWithTransactions](L2Provider.md#getblockwithtransactions)
- [getCode](L2Provider.md#getcode)
- [getFeeData](L2Provider.md#getfeedata)
- [getGasPrice](L2Provider.md#getgasprice)
- [getL1GasPrice](L2Provider.md#getl1gasprice)
- [getLogs](L2Provider.md#getlogs)
- [getNetwork](L2Provider.md#getnetwork)
- [getStorageAt](L2Provider.md#getstorageat)
- [getTransaction](L2Provider.md#gettransaction)
- [getTransactionCount](L2Provider.md#gettransactioncount)
- [getTransactionReceipt](L2Provider.md#gettransactionreceipt)
- [listenerCount](L2Provider.md#listenercount)
- [listeners](L2Provider.md#listeners)
- [lookupAddress](L2Provider.md#lookupaddress)
- [off](L2Provider.md#off)
- [on](L2Provider.md#on)
- [once](L2Provider.md#once)
- [removeAllListeners](L2Provider.md#removealllisteners)
- [removeListener](L2Provider.md#removelistener)
- [resolveName](L2Provider.md#resolvename)
- [sendTransaction](L2Provider.md#sendtransaction)
- [waitForTransaction](L2Provider.md#waitfortransaction)

## Properties

### \_isProvider

• `Readonly` **\_isProvider**: `boolean`

#### Inherited from

Provider.\_isProvider

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:150

## Methods

### addListener

▸ **addListener**(`eventName`, `listener`): `Provider`

#### Parameters

| Name | Type |
| :------ | :------ |
| `eventName` | `EventType` |
| `listener` | `Listener` |

#### Returns

`Provider`

#### Inherited from

Provider.addListener

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:147

___

### call

▸ `Abstract` **call**(`transaction`, `blockTag?`): `Promise`<`string`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `transaction` | `Deferrable`<`TransactionRequest`\> |
| `blockTag?` | `BlockTag` \| `Promise`<`BlockTag`\> |

#### Returns

`Promise`<`string`\>

#### Inherited from

Provider.call

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:131

___

### emit

▸ `Abstract` **emit**(`eventName`, ...`args`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `eventName` | `EventType` |
| `...args` | `any`[] |

#### Returns

`boolean`

#### Inherited from

Provider.emit

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:142

___

### estimateGas

▸ `Abstract` **estimateGas**(`transaction`): `Promise`<`BigNumber`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `transaction` | `Deferrable`<`TransactionRequest`\> |

#### Returns

`Promise`<`BigNumber`\>

#### Inherited from

Provider.estimateGas

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:132

___

### estimateL1Gas

▸ **estimateL1Gas**(`tx`): `Promise`<`BigNumber`\>

Estimates the L1 (data) gas required for a transaction.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `tx` | `TransactionRequest` | Transaction to estimate L1 gas for. |

#### Returns

`Promise`<`BigNumber`\>

Estimated L1 gas.

#### Defined in

[packages/sdk/src/interfaces/l2-provider.ts:22](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/interfaces/l2-provider.ts#L22)

___

### estimateL1GasCost

▸ **estimateL1GasCost**(`tx`): `Promise`<`BigNumber`\>

Estimates the L1 (data) gas cost for a transaction in wei by multiplying the estimated L1 gas
cost by the current L1 gas price.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `tx` | `TransactionRequest` | Transaction to estimate L1 gas cost for. |

#### Returns

`Promise`<`BigNumber`\>

Estimated L1 gas cost.

#### Defined in

[packages/sdk/src/interfaces/l2-provider.ts:31](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/interfaces/l2-provider.ts#L31)

___

### estimateL2GasCost

▸ **estimateL2GasCost**(`tx`): `Promise`<`BigNumber`\>

Estimates the L2 (execution) gas cost for a transaction in wei by multiplying the estimated L1
gas cost by the current L2 gas price. This is a simple multiplication of the result of
getGasPrice and estimateGas for the given transaction request.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `tx` | `TransactionRequest` | Transaction to estimate L2 gas cost for. |

#### Returns

`Promise`<`BigNumber`\>

Estimated L2 gas cost.

#### Defined in

[packages/sdk/src/interfaces/l2-provider.ts:41](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/interfaces/l2-provider.ts#L41)

___

### estimateTotalGasCost

▸ **estimateTotalGasCost**(`tx`): `Promise`<`BigNumber`\>

Estimates the total gas cost for a transaction in wei by adding the estimated the L1 gas cost
and the estimated L2 gas cost.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `tx` | `TransactionRequest` | Transaction to estimate total gas cost for. |

#### Returns

`Promise`<`BigNumber`\>

Estimated total gas cost.

#### Defined in

[packages/sdk/src/interfaces/l2-provider.ts:50](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/interfaces/l2-provider.ts#L50)

___

### getBalance

▸ `Abstract` **getBalance**(`addressOrName`, `blockTag?`): `Promise`<`BigNumber`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `addressOrName` | `string` \| `Promise`<`string`\> |
| `blockTag?` | `BlockTag` \| `Promise`<`BlockTag`\> |

#### Returns

`Promise`<`BigNumber`\>

#### Inherited from

Provider.getBalance

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:126

___

### getBlock

▸ `Abstract` **getBlock**(`blockHashOrBlockTag`): `Promise`<`Block`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `blockHashOrBlockTag` | `BlockTag` \| `Promise`<`BlockTag`\> |

#### Returns

`Promise`<`Block`\>

#### Inherited from

Provider.getBlock

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:133

___

### getBlockNumber

▸ `Abstract` **getBlockNumber**(): `Promise`<`number`\>

#### Returns

`Promise`<`number`\>

#### Inherited from

Provider.getBlockNumber

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:123

___

### getBlockWithTransactions

▸ `Abstract` **getBlockWithTransactions**(`blockHashOrBlockTag`): `Promise`<`BlockWithTransactions`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `blockHashOrBlockTag` | `BlockTag` \| `Promise`<`BlockTag`\> |

#### Returns

`Promise`<`BlockWithTransactions`\>

#### Inherited from

Provider.getBlockWithTransactions

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:134

___

### getCode

▸ `Abstract` **getCode**(`addressOrName`, `blockTag?`): `Promise`<`string`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `addressOrName` | `string` \| `Promise`<`string`\> |
| `blockTag?` | `BlockTag` \| `Promise`<`BlockTag`\> |

#### Returns

`Promise`<`string`\>

#### Inherited from

Provider.getCode

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:128

___

### getFeeData

▸ **getFeeData**(): `Promise`<`FeeData`\>

#### Returns

`Promise`<`FeeData`\>

#### Inherited from

Provider.getFeeData

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:125

___

### getGasPrice

▸ `Abstract` **getGasPrice**(): `Promise`<`BigNumber`\>

#### Returns

`Promise`<`BigNumber`\>

#### Inherited from

Provider.getGasPrice

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:124

___

### getL1GasPrice

▸ **getL1GasPrice**(): `Promise`<`BigNumber`\>

Gets the current L1 (data) gas price.

#### Returns

`Promise`<`BigNumber`\>

Current L1 data gas price in wei.

#### Defined in

[packages/sdk/src/interfaces/l2-provider.ts:14](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/interfaces/l2-provider.ts#L14)

___

### getLogs

▸ `Abstract` **getLogs**(`filter`): `Promise`<`Log`[]\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `filter` | `Filter` |

#### Returns

`Promise`<`Log`[]\>

#### Inherited from

Provider.getLogs

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:137

___

### getNetwork

▸ `Abstract` **getNetwork**(): `Promise`<`Network`\>

#### Returns

`Promise`<`Network`\>

#### Inherited from

Provider.getNetwork

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:122

___

### getStorageAt

▸ `Abstract` **getStorageAt**(`addressOrName`, `position`, `blockTag?`): `Promise`<`string`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `addressOrName` | `string` \| `Promise`<`string`\> |
| `position` | `BigNumberish` \| `Promise`<`BigNumberish`\> |
| `blockTag?` | `BlockTag` \| `Promise`<`BlockTag`\> |

#### Returns

`Promise`<`string`\>

#### Inherited from

Provider.getStorageAt

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:129

___

### getTransaction

▸ `Abstract` **getTransaction**(`transactionHash`): `Promise`<`TransactionResponse`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `transactionHash` | `string` |

#### Returns

`Promise`<`TransactionResponse`\>

#### Inherited from

Provider.getTransaction

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:135

___

### getTransactionCount

▸ `Abstract` **getTransactionCount**(`addressOrName`, `blockTag?`): `Promise`<`number`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `addressOrName` | `string` \| `Promise`<`string`\> |
| `blockTag?` | `BlockTag` \| `Promise`<`BlockTag`\> |

#### Returns

`Promise`<`number`\>

#### Inherited from

Provider.getTransactionCount

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:127

___

### getTransactionReceipt

▸ `Abstract` **getTransactionReceipt**(`transactionHash`): `Promise`<`TransactionReceipt`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `transactionHash` | `string` |

#### Returns

`Promise`<`TransactionReceipt`\>

#### Inherited from

Provider.getTransactionReceipt

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:136

___

### listenerCount

▸ `Abstract` **listenerCount**(`eventName?`): `number`

#### Parameters

| Name | Type |
| :------ | :------ |
| `eventName?` | `EventType` |

#### Returns

`number`

#### Inherited from

Provider.listenerCount

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:143

___

### listeners

▸ `Abstract` **listeners**(`eventName?`): `Listener`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `eventName?` | `EventType` |

#### Returns

`Listener`[]

#### Inherited from

Provider.listeners

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:144

___

### lookupAddress

▸ `Abstract` **lookupAddress**(`address`): `Promise`<`string`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `address` | `string` \| `Promise`<`string`\> |

#### Returns

`Promise`<`string`\>

#### Inherited from

Provider.lookupAddress

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:139

___

### off

▸ `Abstract` **off**(`eventName`, `listener?`): `Provider`

#### Parameters

| Name | Type |
| :------ | :------ |
| `eventName` | `EventType` |
| `listener?` | `Listener` |

#### Returns

`Provider`

#### Inherited from

Provider.off

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:145

___

### on

▸ `Abstract` **on**(`eventName`, `listener`): `Provider`

#### Parameters

| Name | Type |
| :------ | :------ |
| `eventName` | `EventType` |
| `listener` | `Listener` |

#### Returns

`Provider`

#### Inherited from

Provider.on

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:140

___

### once

▸ `Abstract` **once**(`eventName`, `listener`): `Provider`

#### Parameters

| Name | Type |
| :------ | :------ |
| `eventName` | `EventType` |
| `listener` | `Listener` |

#### Returns

`Provider`

#### Inherited from

Provider.once

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:141

___

### removeAllListeners

▸ `Abstract` **removeAllListeners**(`eventName?`): `Provider`

#### Parameters

| Name | Type |
| :------ | :------ |
| `eventName?` | `EventType` |

#### Returns

`Provider`

#### Inherited from

Provider.removeAllListeners

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:146

___

### removeListener

▸ **removeListener**(`eventName`, `listener`): `Provider`

#### Parameters

| Name | Type |
| :------ | :------ |
| `eventName` | `EventType` |
| `listener` | `Listener` |

#### Returns

`Provider`

#### Inherited from

Provider.removeListener

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:148

___

### resolveName

▸ `Abstract` **resolveName**(`name`): `Promise`<`string`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `name` | `string` \| `Promise`<`string`\> |

#### Returns

`Promise`<`string`\>

#### Inherited from

Provider.resolveName

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:138

___

### sendTransaction

▸ `Abstract` **sendTransaction**(`signedTransaction`): `Promise`<`TransactionResponse`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `signedTransaction` | `string` \| `Promise`<`string`\> |

#### Returns

`Promise`<`TransactionResponse`\>

#### Inherited from

Provider.sendTransaction

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:130

___

### waitForTransaction

▸ `Abstract` **waitForTransaction**(`transactionHash`, `confirmations?`, `timeout?`): `Promise`<`TransactionReceipt`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `transactionHash` | `string` |
| `confirmations?` | `number` |
| `timeout?` | `number` |

#### Returns

`Promise`<`TransactionReceipt`\>

#### Inherited from

Provider.waitForTransaction

#### Defined in

node_modules/@ethersproject/abstract-provider/lib/index.d.ts:149
