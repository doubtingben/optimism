[@eth-optimism/sdk](README.md) / Exports

# @eth-optimism/sdk

## Table of contents

### Enumerations

- [MessageDirection](enums/MessageDirection.md)
- [MessageReceiptStatus](enums/MessageReceiptStatus.md)
- [MessageStatus](enums/MessageStatus.md)

### Classes

- [CrossChainMessenger](classes/CrossChainMessenger.md)
- [DAIBridgeAdapter](classes/DAIBridgeAdapter.md)
- [ETHBridgeAdapter](classes/ETHBridgeAdapter.md)
- [StandardBridgeAdapter](classes/StandardBridgeAdapter.md)

### Interfaces

- [BridgeAdapterData](interfaces/BridgeAdapterData.md)
- [BridgeAdapters](interfaces/BridgeAdapters.md)
- [CoreCrossChainMessage](interfaces/CoreCrossChainMessage.md)
- [CrossChainMessage](interfaces/CrossChainMessage.md)
- [CrossChainMessageProof](interfaces/CrossChainMessageProof.md)
- [CrossChainMessageRequest](interfaces/CrossChainMessageRequest.md)
- [IBridgeAdapter](interfaces/IBridgeAdapter.md)
- [ICrossChainMessenger](interfaces/ICrossChainMessenger.md)
- [L2Provider](interfaces/L2Provider.md)
- [MessageReceipt](interfaces/MessageReceipt.md)
- [OEContracts](interfaces/OEContracts.md)
- [OEContractsLike](interfaces/OEContractsLike.md)
- [OEL1Contracts](interfaces/OEL1Contracts.md)
- [OEL2Contracts](interfaces/OEL2Contracts.md)
- [StateRoot](interfaces/StateRoot.md)
- [StateRootBatch](interfaces/StateRootBatch.md)
- [StateRootBatchHeader](interfaces/StateRootBatchHeader.md)
- [TokenBridgeMessage](interfaces/TokenBridgeMessage.md)

### Type aliases

- [AddressLike](modules.md#addresslike)
- [DeepPartial](modules.md#deeppartial)
- [MessageLike](modules.md#messagelike)
- [MessageRequestLike](modules.md#messagerequestlike)
- [NumberLike](modules.md#numberlike)
- [OEL1ContractsLike](modules.md#oel1contractslike)
- [OEL2ContractsLike](modules.md#oel2contractslike)
- [ProviderLike](modules.md#providerlike)
- [SignerLike](modules.md#signerlike)
- [SignerOrProviderLike](modules.md#signerorproviderlike)
- [TransactionLike](modules.md#transactionlike)

### Variables

- [BRIDGE\_ADAPTER\_DATA](modules.md#bridge_adapter_data)
- [CHAIN\_BLOCK\_TIMES](modules.md#chain_block_times)
- [CONTRACT\_ADDRESSES](modules.md#contract_addresses)
- [DEFAULT\_L2\_CONTRACT\_ADDRESSES](modules.md#default_l2_contract_addresses)
- [DEPOSIT\_CONFIRMATION\_BLOCKS](modules.md#deposit_confirmation_blocks)

### Functions

- [encodeCrossChainMessage](modules.md#encodecrosschainmessage)
- [getAllOEContracts](modules.md#getalloecontracts)
- [getBridgeAdapters](modules.md#getbridgeadapters)
- [getOEContract](modules.md#getoecontract)
- [hashCrossChainMessage](modules.md#hashcrosschainmessage)
- [makeMerkleTreeProof](modules.md#makemerkletreeproof)
- [makeStateTrieProof](modules.md#makestatetrieproof)
- [omit](modules.md#omit)
- [toAddress](modules.md#toaddress)
- [toBigNumber](modules.md#tobignumber)
- [toNumber](modules.md#tonumber)
- [toSignerOrProvider](modules.md#tosignerorprovider)
- [toTransactionHash](modules.md#totransactionhash)

## Type aliases

### AddressLike

Ƭ **AddressLike**: `string` \| `Contract`

Stuff that can be coerced into an address.

#### Defined in

[packages/sdk/src/interfaces/types.ts:287](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/interfaces/types.ts#L287)

___

### DeepPartial

Ƭ **DeepPartial**<`T`\>: { [P in keyof T]?: DeepPartial<T[P]\> }

Utility type for deep partials.

#### Type parameters

| Name |
| :------ |
| `T` |

#### Defined in

[packages/sdk/src/utils/type-utils.ts:4](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/type-utils.ts#L4)

___

### MessageLike

Ƭ **MessageLike**: [`CrossChainMessage`](interfaces/CrossChainMessage.md) \| [`TransactionLike`](modules.md#transactionlike) \| [`TokenBridgeMessage`](interfaces/TokenBridgeMessage.md)

Stuff that can be coerced into a CrossChainMessage.

#### Defined in

[packages/sdk/src/interfaces/types.ts:255](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/interfaces/types.ts#L255)

___

### MessageRequestLike

Ƭ **MessageRequestLike**: [`CrossChainMessageRequest`](interfaces/CrossChainMessageRequest.md) \| [`CrossChainMessage`](interfaces/CrossChainMessage.md) \| [`TransactionLike`](modules.md#transactionlike) \| [`TokenBridgeMessage`](interfaces/TokenBridgeMessage.md)

Stuff that can be coerced into a CrossChainMessageRequest.

#### Defined in

[packages/sdk/src/interfaces/types.ts:263](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/interfaces/types.ts#L263)

___

### NumberLike

Ƭ **NumberLike**: `string` \| `number` \| `BigNumber`

Stuff that can be coerced into a number.

#### Defined in

[packages/sdk/src/interfaces/types.ts:292](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/interfaces/types.ts#L292)

___

### OEL1ContractsLike

Ƭ **OEL1ContractsLike**: { [K in keyof OEL1Contracts]: AddressLike }

Convenience type for something that looks like the L1 OE contract interface but could be
addresses instead of actual contract objects.

#### Defined in

[packages/sdk/src/interfaces/types.ts:52](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/interfaces/types.ts#L52)

___

### OEL2ContractsLike

Ƭ **OEL2ContractsLike**: { [K in keyof OEL2Contracts]: AddressLike }

Convenience type for something that looks like the L2 OE contract interface but could be
addresses instead of actual contract objects.

#### Defined in

[packages/sdk/src/interfaces/types.ts:60](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/interfaces/types.ts#L60)

___

### ProviderLike

Ƭ **ProviderLike**: `string` \| `Provider` \| `any`

Stuff that can be coerced into a provider.

#### Defined in

[packages/sdk/src/interfaces/types.ts:272](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/interfaces/types.ts#L272)

___

### SignerLike

Ƭ **SignerLike**: `string` \| `Signer`

Stuff that can be coerced into a signer.

#### Defined in

[packages/sdk/src/interfaces/types.ts:277](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/interfaces/types.ts#L277)

___

### SignerOrProviderLike

Ƭ **SignerOrProviderLike**: [`SignerLike`](modules.md#signerlike) \| [`ProviderLike`](modules.md#providerlike)

Stuff that can be coerced into a signer or provider.

#### Defined in

[packages/sdk/src/interfaces/types.ts:282](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/interfaces/types.ts#L282)

___

### TransactionLike

Ƭ **TransactionLike**: `string` \| `TransactionReceipt` \| `TransactionResponse`

Stuff that can be coerced into a transaction.

#### Defined in

[packages/sdk/src/interfaces/types.ts:250](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/interfaces/types.ts#L250)

## Variables

### BRIDGE\_ADAPTER\_DATA

• **BRIDGE\_ADAPTER\_DATA**: `Object`

Mapping of L1 chain IDs to the list of custom bridge addresses for each chain.

#### Index signature

▪ [l1ChainId: `number`]: [`BridgeAdapterData`](interfaces/BridgeAdapterData.md)

#### Defined in

[packages/sdk/src/utils/contracts.ts:109](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/contracts.ts#L109)

___

### CHAIN\_BLOCK\_TIMES

• **CHAIN\_BLOCK\_TIMES**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `1` | `number` |
| `31337` | `number` |
| `42` | `number` |
| `5` | `number` |

#### Defined in

[packages/sdk/src/utils/chain-constants.ts:13](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/chain-constants.ts#L13)

___

### CONTRACT\_ADDRESSES

• **CONTRACT\_ADDRESSES**: `Object`

Mapping of L1 chain IDs to the appropriate contract addresses for the OE deployments to the
given network. Simplifies the process of getting the correct contract addresses for a given
contract name.

#### Index signature

▪ [l1ChainId: `number`]: [`OEContractsLike`](interfaces/OEContractsLike.md)

#### Defined in

[packages/sdk/src/utils/contracts.ts:53](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/contracts.ts#L53)

___

### DEFAULT\_L2\_CONTRACT\_ADDRESSES

• **DEFAULT\_L2\_CONTRACT\_ADDRESSES**: [`OEL2ContractsLike`](modules.md#oel2contractslike)

Full list of default L2 contract addresses.

#### Defined in

[packages/sdk/src/utils/contracts.ts:26](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/contracts.ts#L26)

___

### DEPOSIT\_CONFIRMATION\_BLOCKS

• **DEPOSIT\_CONFIRMATION\_BLOCKS**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `1` | `number` |
| `31337` | `number` |
| `42` | `number` |
| `5` | `number` |

#### Defined in

[packages/sdk/src/utils/chain-constants.ts:1](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/chain-constants.ts#L1)

## Functions

### encodeCrossChainMessage

▸ `Const` **encodeCrossChainMessage**(`message`): `string`

Returns the canonical encoding of a cross chain message. This encoding is used in various
locations within the Optimism smart contracts.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `message` | [`CoreCrossChainMessage`](interfaces/CoreCrossChainMessage.md) | Cross chain message to encode. |

#### Returns

`string`

Canonical encoding of the message.

#### Defined in

[packages/sdk/src/utils/message-encoding.ts:13](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/message-encoding.ts#L13)

___

### getAllOEContracts

▸ `Const` **getAllOEContracts**(`l1ChainId`, `opts?`): [`OEContracts`](interfaces/OEContracts.md)

Automatically connects to all contract addresses, both L1 and L2, for the given L1 chain ID. The
user can provide custom contract address overrides for L1 or L2 contracts. If the given chain ID
is not known then the user MUST provide custom contract addresses for ALL L1 contracts or this
function will throw an error.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `l1ChainId` | `number` | Chain ID for the L1 network where the OE contracts are deployed. |
| `opts` | `Object` | Additional options for connecting to the contracts. |
| `opts.l1SignerOrProvider?` | `Signer` \| `Provider` | - |
| `opts.l2SignerOrProvider?` | `Signer` \| `Provider` | - |
| `opts.overrides?` | [`DeepPartial`](modules.md#deeppartial)<[`OEContractsLike`](interfaces/OEContractsLike.md)\> | Custom contract address overrides for L1 or L2 contracts. |

#### Returns

[`OEContracts`](interfaces/OEContracts.md)

An object containing ethers.Contract objects connected to the appropriate addresses on
both L1 and L2.

#### Defined in

[packages/sdk/src/utils/contracts.ts:256](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/contracts.ts#L256)

___

### getBridgeAdapters

▸ `Const` **getBridgeAdapters**(`l1ChainId`, `messenger`, `opts?`): [`BridgeAdapters`](interfaces/BridgeAdapters.md)

Gets a series of bridge adapters for the given L1 chain ID.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `l1ChainId` | `number` | L1 chain ID for the L1 network where the custom bridges are deployed. |
| `messenger` | [`ICrossChainMessenger`](interfaces/ICrossChainMessenger.md) | Cross chain messenger to connect to the bridge adapters |
| `opts?` | `Object` | Additional options for connecting to the custom bridges. |
| `opts.overrides?` | [`BridgeAdapterData`](interfaces/BridgeAdapterData.md) | Custom bridge adapters. |

#### Returns

[`BridgeAdapters`](interfaces/BridgeAdapters.md)

An object containing all bridge adapters

#### Defined in

[packages/sdk/src/utils/contracts.ts:309](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/contracts.ts#L309)

___

### getOEContract

▸ `Const` **getOEContract**(`contractName`, `l1ChainId`, `opts?`): `Contract`

Returns an ethers.Contract object for the given name, connected to the appropriate address for
the given L1 chain ID. Users can also provide a custom address to connect the contract to
instead. If the chain ID is not known then the user MUST provide a custom address or this
function will throw an error.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `contractName` | keyof [`OEL1Contracts`](interfaces/OEL1Contracts.md) \| keyof [`OEL2Contracts`](interfaces/OEL2Contracts.md) | Name of the contract to connect to. |
| `l1ChainId` | `number` | Chain ID for the L1 network where the OE contracts are deployed. |
| `opts` | `Object` | Additional options for connecting to the contract. |
| `opts.address?` | [`AddressLike`](modules.md#addresslike) | Custom address to connect to the contract. |
| `opts.signerOrProvider?` | `Signer` \| `Provider` | Signer or provider to connect to the contract. |

#### Returns

`Contract`

An ethers.Contract object connected to the appropriate address and interface.

#### Defined in

[packages/sdk/src/utils/contracts.ts:218](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/contracts.ts#L218)

___

### hashCrossChainMessage

▸ `Const` **hashCrossChainMessage**(`message`): `string`

Returns the canonical hash of a cross chain message. This hash is used in various locations
within the Optimism smart contracts and is the keccak256 hash of the result of
encodeCrossChainMessage.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `message` | [`CoreCrossChainMessage`](interfaces/CoreCrossChainMessage.md) | Cross chain message to hash. |

#### Returns

`string`

Canonical hash of the message.

#### Defined in

[packages/sdk/src/utils/message-encoding.ts:30](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/message-encoding.ts#L30)

___

### makeMerkleTreeProof

▸ `Const` **makeMerkleTreeProof**(`leaves`, `index`): `string`[]

Generates a Merkle proof (using the particular scheme we use within Lib_MerkleTree).

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `leaves` | `string`[] | Leaves of the merkle tree. |
| `index` | `number` | Index to generate a proof for. |

#### Returns

`string`[]

Merkle proof sibling leaves, as hex strings.

#### Defined in

[packages/sdk/src/utils/merkle-utils.ts:18](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/merkle-utils.ts#L18)

___

### makeStateTrieProof

▸ `Const` **makeStateTrieProof**(`provider`, `blockNumber`, `address`, `slot`): `Promise`<{ `accountProof`: `string` ; `storageProof`: `string`  }\>

Generates a Merkle-Patricia trie proof for a given account and storage slot.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `provider` | `JsonRpcProvider` | RPC provider attached to an EVM-compatible chain. |
| `blockNumber` | `number` | Block number to generate the proof at. |
| `address` | `string` | Address to generate the proof for. |
| `slot` | `string` | Storage slot to generate the proof for. |

#### Returns

`Promise`<{ `accountProof`: `string` ; `storageProof`: `string`  }\>

Account proof and storage proof.

#### Defined in

[packages/sdk/src/utils/merkle-utils.ts:57](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/merkle-utils.ts#L57)

___

### omit

▸ `Const` **omit**(`obj`, ...`keys`): `any`

Returns a copy of the given object ({ ...obj }) with the given keys omitted.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `obj` | `any` | Object to return with the keys omitted. |
| `...keys` | `string`[] | Keys to omit from the returned object. |

#### Returns

`any`

A copy of the given object with the given keys omitted.

#### Defined in

[packages/sdk/src/utils/misc-utils.ts:11](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/misc-utils.ts#L11)

___

### toAddress

▸ `Const` **toAddress**(`addr`): `string`

Converts an address-like into a 0x-prefixed address string.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `addr` | [`AddressLike`](modules.md#addresslike) | Address-like to convert into an address. |

#### Returns

`string`

Address-like as an address.

#### Defined in

[packages/sdk/src/utils/coercion.ts:88](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/coercion.ts#L88)

___

### toBigNumber

▸ `Const` **toBigNumber**(`num`): `BigNumber`

Converts a number-like into an ethers BigNumber.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `num` | [`NumberLike`](modules.md#numberlike) | Number-like to convert into a BigNumber. |

#### Returns

`BigNumber`

Number-like as a BigNumber.

#### Defined in

[packages/sdk/src/utils/coercion.ts:68](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/coercion.ts#L68)

___

### toNumber

▸ `Const` **toNumber**(`num`): `number`

Converts a number-like into a number.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `num` | [`NumberLike`](modules.md#numberlike) | Number-like to convert into a number. |

#### Returns

`number`

Number-like as a number.

#### Defined in

[packages/sdk/src/utils/coercion.ts:78](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/coercion.ts#L78)

___

### toSignerOrProvider

▸ `Const` **toSignerOrProvider**(`signerOrProvider`): `Signer` \| `Provider`

Converts a SignerOrProviderLike into a Signer or a Provider. Assumes that if the input is a
string then it is a JSON-RPC url.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `signerOrProvider` | `any` | SignerOrProviderLike to turn into a Signer or Provider. |

#### Returns

`Signer` \| `Provider`

Input as a Signer or Provider.

#### Defined in

[packages/sdk/src/utils/coercion.ts:25](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/coercion.ts#L25)

___

### toTransactionHash

▸ `Const` **toTransactionHash**(`transaction`): `string`

Pulls a transaction hash out of a TransactionLike object.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `transaction` | [`TransactionLike`](modules.md#transactionlike) | TransactionLike to convert into a transaction hash. |

#### Returns

`string`

Transaction hash corresponding to the TransactionLike input.

#### Defined in

[packages/sdk/src/utils/coercion.ts:45](https://github.com/ethereum-optimism/optimism/blob/e5a9fd56/packages/sdk/src/utils/coercion.ts#L45)
