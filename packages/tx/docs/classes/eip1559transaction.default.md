[@ethereumjs/tx](../README.md) / [eip1559Transaction](../modules/eip1559transaction.md) / default

# Class: default

[eip1559Transaction](../modules/eip1559transaction.md).default

Typed transaction with a new gas fee market mechanism

- TransactionType: 2
- EIP: [EIP-1559](https://eips.ethereum.org/EIPS/eip-1559)

## Hierarchy

- [*BaseTransaction*](basetransaction.basetransaction-1.md)<[*default*](eip1559transaction.default.md)\>

  ↳ **default**

## Table of contents

### Constructors

- [constructor](eip1559transaction.default.md#constructor)

### Properties

- [AccessListJSON](eip1559transaction.default.md#accesslistjson)
- [accessList](eip1559transaction.default.md#accesslist)
- [chainId](eip1559transaction.default.md#chainid)
- [common](eip1559transaction.default.md#common)
- [data](eip1559transaction.default.md#data)
- [gasLimit](eip1559transaction.default.md#gaslimit)
- [maxFeePerGas](eip1559transaction.default.md#maxfeepergas)
- [maxPriorityFeePerGas](eip1559transaction.default.md#maxpriorityfeepergas)
- [nonce](eip1559transaction.default.md#nonce)
- [r](eip1559transaction.default.md#r)
- [s](eip1559transaction.default.md#s)
- [to](eip1559transaction.default.md#to)
- [v](eip1559transaction.default.md#v)
- [value](eip1559transaction.default.md#value)

### Accessors

- [senderR](eip1559transaction.default.md#senderr)
- [senderS](eip1559transaction.default.md#senders)
- [transactionType](eip1559transaction.default.md#transactiontype)
- [type](eip1559transaction.default.md#type)
- [yParity](eip1559transaction.default.md#yparity)

### Methods

- [\_processSignature](eip1559transaction.default.md#_processsignature)
- [getBaseFee](eip1559transaction.default.md#getbasefee)
- [getDataFee](eip1559transaction.default.md#getdatafee)
- [getMessageToSign](eip1559transaction.default.md#getmessagetosign)
- [getMessageToVerifySignature](eip1559transaction.default.md#getmessagetoverifysignature)
- [getSenderAddress](eip1559transaction.default.md#getsenderaddress)
- [getSenderPublicKey](eip1559transaction.default.md#getsenderpublickey)
- [getUpfrontCost](eip1559transaction.default.md#getupfrontcost)
- [hash](eip1559transaction.default.md#hash)
- [isSigned](eip1559transaction.default.md#issigned)
- [raw](eip1559transaction.default.md#raw)
- [serialize](eip1559transaction.default.md#serialize)
- [sign](eip1559transaction.default.md#sign)
- [toCreationAddress](eip1559transaction.default.md#tocreationaddress)
- [toJSON](eip1559transaction.default.md#tojson)
- [validate](eip1559transaction.default.md#validate)
- [verifySignature](eip1559transaction.default.md#verifysignature)
- [fromRlpSerializedTx](eip1559transaction.default.md#fromrlpserializedtx)
- [fromSerializedTx](eip1559transaction.default.md#fromserializedtx)
- [fromTxData](eip1559transaction.default.md#fromtxdata)
- [fromValuesArray](eip1559transaction.default.md#fromvaluesarray)

## Constructors

### constructor

\+ **new default**(`txData`: [*FeeMarketEIP1559TxData*](../interfaces/types.feemarketeip1559txdata.md), `opts?`: [*TxOptions*](../interfaces/types.txoptions.md)): [*default*](eip1559transaction.default.md)

This constructor takes the values, validates them, assigns them and freezes the object.

It is not recommended to use this constructor directly. Instead use
the static factory methods to assist in creating a Transaction object from
varying data types.

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `txData` | [*FeeMarketEIP1559TxData*](../interfaces/types.feemarketeip1559txdata.md) | - |
| `opts` | [*TxOptions*](../interfaces/types.txoptions.md) | {} |

**Returns:** [*default*](eip1559transaction.default.md)

Overrides: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [eip1559Transaction.ts:164](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L164)

## Properties

### AccessListJSON

• `Readonly` **AccessListJSON**: [*AccessList*](../modules/types.md#accesslist)

Defined in: [eip1559Transaction.ts:27](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L27)

___

### accessList

• `Readonly` **accessList**: [*AccessListBuffer*](../modules/types.md#accesslistbuffer)

Defined in: [eip1559Transaction.ts:26](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L26)

___

### chainId

• `Readonly` **chainId**: *BN*

Defined in: [eip1559Transaction.ts:25](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L25)

___

### common

• `Readonly` **common**: *default*

Overrides: [BaseTransaction](basetransaction.basetransaction-1.md).[common](basetransaction.basetransaction-1.md#common)

Defined in: [eip1559Transaction.ts:31](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L31)

___

### data

• `Readonly` **data**: *Buffer*

Inherited from: [BaseTransaction](basetransaction.basetransaction-1.md).[data](basetransaction.basetransaction-1.md#data)

Defined in: [baseTransaction.ts:37](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L37)

___

### gasLimit

• `Readonly` **gasLimit**: *BN*

Inherited from: [BaseTransaction](basetransaction.basetransaction-1.md).[gasLimit](basetransaction.basetransaction-1.md#gaslimit)

Defined in: [baseTransaction.ts:34](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L34)

___

### maxFeePerGas

• `Readonly` **maxFeePerGas**: *BN*

Defined in: [eip1559Transaction.ts:29](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L29)

___

### maxPriorityFeePerGas

• `Readonly` **maxPriorityFeePerGas**: *BN*

Defined in: [eip1559Transaction.ts:28](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L28)

___

### nonce

• `Readonly` **nonce**: *BN*

Inherited from: [BaseTransaction](basetransaction.basetransaction-1.md).[nonce](basetransaction.basetransaction-1.md#nonce)

Defined in: [baseTransaction.ts:33](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L33)

___

### r

• `Optional` `Readonly` **r**: *BN*

Inherited from: [BaseTransaction](basetransaction.basetransaction-1.md).[r](basetransaction.basetransaction-1.md#r)

Defined in: [baseTransaction.ts:40](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L40)

___

### s

• `Optional` `Readonly` **s**: *BN*

Inherited from: [BaseTransaction](basetransaction.basetransaction-1.md).[s](basetransaction.basetransaction-1.md#s)

Defined in: [baseTransaction.ts:41](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L41)

___

### to

• `Optional` `Readonly` **to**: *Address*

Inherited from: [BaseTransaction](basetransaction.basetransaction-1.md).[to](basetransaction.basetransaction-1.md#to)

Defined in: [baseTransaction.ts:35](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L35)

___

### v

• `Optional` `Readonly` **v**: *BN*

Inherited from: [BaseTransaction](basetransaction.basetransaction-1.md).[v](basetransaction.basetransaction-1.md#v)

Defined in: [baseTransaction.ts:39](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L39)

___

### value

• `Readonly` **value**: *BN*

Inherited from: [BaseTransaction](basetransaction.basetransaction-1.md).[value](basetransaction.basetransaction-1.md#value)

Defined in: [baseTransaction.ts:36](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L36)

## Accessors

### senderR

• get **senderR**(): *undefined* \| *BN*

EIP-2930 alias for `r`

**`deprecated`** use `r` instead

**Returns:** *undefined* \| *BN*

Defined in: [eip1559Transaction.ts:46](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L46)

___

### senderS

• get **senderS**(): *undefined* \| *BN*

EIP-2930 alias for `s`

**`deprecated`** use `s` instead

**Returns:** *undefined* \| *BN*

Defined in: [eip1559Transaction.ts:55](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L55)

___

### transactionType

• get **transactionType**(): *number*

Alias for `type`

**`deprecated`** Use `type` instead

**Returns:** *number*

Defined in: [baseTransaction.ts:96](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L96)

___

### type

• get **type**(): *number*

Returns the transaction type.

Note: legacy txs will return tx type `0`.

**Returns:** *number*

Defined in: [baseTransaction.ts:105](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L105)

___

### yParity

• get **yParity**(): *undefined* \| *BN*

EIP-2930 alias for `v`

**`deprecated`** use `v` instead

**Returns:** *undefined* \| *BN*

Defined in: [eip1559Transaction.ts:64](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L64)

## Methods

### \_processSignature

▸ **_processSignature**(`v`: *number*, `r`: *Buffer*, `s`: *Buffer*): [*default*](eip1559transaction.default.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `v` | *number* |
| `r` | *Buffer* |
| `s` | *Buffer* |

**Returns:** [*default*](eip1559transaction.default.md)

Overrides: BaseTransaction.\_processSignature

Defined in: [eip1559Transaction.ts:362](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L362)

___

### getBaseFee

▸ **getBaseFee**(): *BN*

The minimum amount of gas the tx must have (DataFee + TxFee + Creation Fee)

**Returns:** *BN*

Inherited from: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [baseTransaction.ts:133](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L133)

___

### getDataFee

▸ **getDataFee**(): *BN*

The amount of gas paid for the data in this tx

**Returns:** *BN*

Overrides: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [eip1559Transaction.ts:229](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L229)

___

### getMessageToSign

▸ **getMessageToSign**(`hashMessage`: ``false``): *Buffer*[]

Returns the serialized unsigned tx (hashed or raw), which can be used
to sign the transaction (e.g. for sending to a hardware wallet).

Note: in contrast to the legacy tx the raw message format is already
serialized and doesn't need to be RLP encoded any more.

```javascript
const serializedMessage = tx.getMessageToSign(false) // use this for the HW wallet input
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `hashMessage` | ``false`` | Return hashed message if set to true (default: true) |

**Returns:** *Buffer*[]

Overrides: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [eip1559Transaction.ts:298](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L298)

▸ **getMessageToSign**(`hashMessage?`: ``true``): *Buffer*

#### Parameters

| Name | Type |
| :------ | :------ |
| `hashMessage?` | ``true`` |

**Returns:** *Buffer*

Overrides: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [eip1559Transaction.ts:299](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L299)

___

### getMessageToVerifySignature

▸ **getMessageToVerifySignature**(): *Buffer*

Computes a sha3-256 hash which can be used to verify the signature

**Returns:** *Buffer*

Overrides: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [eip1559Transaction.ts:327](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L327)

___

### getSenderAddress

▸ **getSenderAddress**(): *Address*

Returns the sender's address

**Returns:** *Address*

Inherited from: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [baseTransaction.ts:221](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L221)

___

### getSenderPublicKey

▸ **getSenderPublicKey**(): *Buffer*

Returns the public key of the sender

**Returns:** *Buffer*

Overrides: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [eip1559Transaction.ts:334](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L334)

___

### getUpfrontCost

▸ **getUpfrontCost**(`baseFee?`: *BN*): *BN*

The up front amount that an account must have for this transaction to be valid

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `baseFee` | *BN* | The base fee of the block (will be set to 0 if not provided) |

**Returns:** *BN*

Overrides: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [eip1559Transaction.ts:239](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L239)

___

### hash

▸ **hash**(): *Buffer*

Computes a sha3-256 hash of the serialized tx.

This method can only be used for signed txs (it throws otherwise).
Use `getMessageToSign()` to get a tx hash for the purpose of signing.

**Returns:** *Buffer*

Overrides: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [eip1559Transaction.ts:316](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L316)

___

### isSigned

▸ **isSigned**(): *boolean*

**Returns:** *boolean*

Inherited from: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [baseTransaction.ts:188](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L188)

___

### raw

▸ **raw**(): [*FeeMarketEIP1559ValuesArray*](../modules/types.md#feemarketeip1559valuesarray)

Returns a Buffer Array of the raw Buffers of the EIP-1559 transaction, in order.

Format: `[chainId, nonce, maxPriorityFeePerGas, maxFeePerGas, gasLimit, to, value, data,
accessList, signatureYParity, signatureR, signatureS]`

Use `serialize()` to add to block data for `Block.fromValuesArray()`.

**Returns:** [*FeeMarketEIP1559ValuesArray*](../modules/types.md#feemarketeip1559valuesarray)

Overrides: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [eip1559Transaction.ts:253](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L253)

___

### serialize

▸ **serialize**(): *Buffer*

Returns the serialized encoding of the EIP-1559 transaction.

Format: `0x02 || rlp([chainId, nonce, maxPriorityFeePerGas, maxFeePerGas, gasLimit, to, value, data,
accessList, signatureYParity, signatureR, signatureS])`

Note that in contrast to the legacy tx serialization format this is not
valid RLP any more due to the raw tx type preceeding and concatenated to
the RLP encoding of the values.

**Returns:** *Buffer*

Overrides: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [eip1559Transaction.ts:280](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L280)

___

### sign

▸ **sign**(`privateKey`: *Buffer*): [*default*](eip1559transaction.default.md)

Signs a transaction.

Note that the signed tx is returned as a new object,
use as follows:
```javascript
const signedTx = tx.sign(privateKey)
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `privateKey` | *Buffer* |

**Returns:** [*default*](eip1559transaction.default.md)

Inherited from: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [baseTransaction.ts:239](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L239)

___

### toCreationAddress

▸ **toCreationAddress**(): *boolean*

If the tx's `to` is to the creation address

**Returns:** *boolean*

Inherited from: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [baseTransaction.ts:163](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L163)

___

### toJSON

▸ **toJSON**(): [*JsonTx*](../interfaces/types.jsontx.md)

Returns an object with the JSON representation of the transaction

**Returns:** [*JsonTx*](../interfaces/types.jsontx.md)

Overrides: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [eip1559Transaction.ts:389](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L389)

___

### validate

▸ **validate**(): *boolean*

Checks if the transaction has the minimum amount of gas required
(DataFee + TxFee + Creation Fee).

**Returns:** *boolean*

Inherited from: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [baseTransaction.ts:113](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L113)

▸ **validate**(`stringError`: ``false``): *boolean*

#### Parameters

| Name | Type |
| :------ | :------ |
| `stringError` | ``false`` |

**Returns:** *boolean*

Inherited from: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [baseTransaction.ts:114](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L114)

▸ **validate**(`stringError`: ``true``): *string*[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `stringError` | ``true`` |

**Returns:** *string*[]

Inherited from: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [baseTransaction.ts:115](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L115)

___

### verifySignature

▸ **verifySignature**(): *boolean*

Determines if the signature is valid

**Returns:** *boolean*

Inherited from: [BaseTransaction](basetransaction.basetransaction-1.md)

Defined in: [baseTransaction.ts:208](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L208)

___

### fromRlpSerializedTx

▸ `Static` **fromRlpSerializedTx**(`serialized`: *Buffer*, `opts?`: [*TxOptions*](../interfaces/types.txoptions.md)): [*default*](eip1559transaction.default.md)

Instantiate a transaction from the serialized tx.
(alias of `fromSerializedTx()`)

Note: This means that the Buffer should start with 0x01.

**`deprecated`** this constructor alias is deprecated and will be removed
in favor of the `fromSerializedTx()` constructor

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `serialized` | *Buffer* | - |
| `opts` | [*TxOptions*](../interfaces/types.txoptions.md) | {} |

**Returns:** [*default*](eip1559transaction.default.md)

Defined in: [eip1559Transaction.ts:115](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L115)

___

### fromSerializedTx

▸ `Static` **fromSerializedTx**(`serialized`: *Buffer*, `opts?`: [*TxOptions*](../interfaces/types.txoptions.md)): [*default*](eip1559transaction.default.md)

Instantiate a transaction from the serialized tx.

Format: `0x02 || rlp([chainId, nonce, maxPriorityFeePerGas, maxFeePerGas, gasLimit, to, value, data,
accessList, signatureYParity, signatureR, signatureS])`

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `serialized` | *Buffer* | - |
| `opts` | [*TxOptions*](../interfaces/types.txoptions.md) | {} |

**Returns:** [*default*](eip1559transaction.default.md)

Defined in: [eip1559Transaction.ts:88](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L88)

___

### fromTxData

▸ `Static` **fromTxData**(`txData`: [*FeeMarketEIP1559TxData*](../interfaces/types.feemarketeip1559txdata.md), `opts?`: [*TxOptions*](../interfaces/types.txoptions.md)): [*default*](eip1559transaction.default.md)

Instantiate a transaction from a data dictionary.

Format: { chainId, nonce, maxPriorityFeePerGas, maxFeePerGas, gasLimit, to, value, data,
accessList, v, r, s }

Notes:
- `chainId` will be set automatically if not provided
- All parameters are optional and have some basic default values

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `txData` | [*FeeMarketEIP1559TxData*](../interfaces/types.feemarketeip1559txdata.md) | - |
| `opts` | [*TxOptions*](../interfaces/types.txoptions.md) | {} |

**Returns:** [*default*](eip1559transaction.default.md)

Defined in: [eip1559Transaction.ts:78](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L78)

___

### fromValuesArray

▸ `Static` **fromValuesArray**(`values`: [*FeeMarketEIP1559ValuesArray*](../modules/types.md#feemarketeip1559valuesarray), `opts?`: [*TxOptions*](../interfaces/types.txoptions.md)): [*default*](eip1559transaction.default.md)

Create a transaction from a values array.

Format: `[chainId, nonce, maxPriorityFeePerGas, maxFeePerGas, gasLimit, to, value, data,
accessList, signatureYParity, signatureR, signatureS]`

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `values` | [*FeeMarketEIP1559ValuesArray*](../modules/types.md#feemarketeip1559valuesarray) | - |
| `opts` | [*TxOptions*](../interfaces/types.txoptions.md) | {} |

**Returns:** [*default*](eip1559transaction.default.md)

Defined in: [eip1559Transaction.ts:125](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip1559Transaction.ts#L125)
