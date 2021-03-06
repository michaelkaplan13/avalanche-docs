[avalanche](../README.md) › [AVMAPI-Transactions](../modules/avmapi_transactions.md) › [Tx](avmapi_transactions.tx.md)

# Class: Tx

Class representing a signed transaction.

## Hierarchy

* **Tx**

## Index

### Constructors

* [constructor](avmapi_transactions.tx.md#constructor)

### Properties

* [credentials](avmapi_transactions.tx.md#protected-credentials)
* [unsignedTx](avmapi_transactions.tx.md#protected-unsignedtx)

### Methods

* [fromBuffer](avmapi_transactions.tx.md#frombuffer)
* [fromString](avmapi_transactions.tx.md#fromstring)
* [toBuffer](avmapi_transactions.tx.md#tobuffer)
* [toString](avmapi_transactions.tx.md#tostring)

## Constructors

###  constructor

\+ **new Tx**(`unsignedTx`: [UnsignedTx](avmapi_transactions.unsignedtx.md), `credentials`: Array‹[Credential](avmapi_credentials.credential.md)›): *[Tx](avmapi_transactions.tx.md)*

*Defined in [src/apis/avm/tx.ts:530](https://github.com/ava-labs/avalanche.js/blob/eabcc2f/src/apis/avm/tx.ts#L530)*

Class representing a signed transaction.

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`unsignedTx` | [UnsignedTx](avmapi_transactions.unsignedtx.md) | undefined | Optional [UnsignedTx](avmapi_transactions.unsignedtx.md) |
`credentials` | Array‹[Credential](avmapi_credentials.credential.md)› | undefined | - |

**Returns:** *[Tx](avmapi_transactions.tx.md)*

## Properties

### `Protected` credentials

• **credentials**: *Array‹[Credential](avmapi_credentials.credential.md)›* = []

*Defined in [src/apis/avm/tx.ts:459](https://github.com/ava-labs/avalanche.js/blob/eabcc2f/src/apis/avm/tx.ts#L459)*

___

### `Protected` unsignedTx

• **unsignedTx**: *[UnsignedTx](avmapi_transactions.unsignedtx.md)* = new UnsignedTx()

*Defined in [src/apis/avm/tx.ts:457](https://github.com/ava-labs/avalanche.js/blob/eabcc2f/src/apis/avm/tx.ts#L457)*

## Methods

###  fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): *number*

*Defined in [src/apis/avm/tx.ts:469](https://github.com/ava-labs/avalanche.js/blob/eabcc2f/src/apis/avm/tx.ts#L469)*

Takes a [Buffer](https://github.com/feross/buffer) containing an [Tx](avmapi_transactions.tx.md), parses it, populates the class, and returns the length of the Tx in bytes.

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`bytes` | Buffer | - | A [Buffer](https://github.com/feross/buffer) containing a raw [Tx](avmapi_transactions.tx.md) |
`offset` | number | 0 | A number representing the starting point of the bytes to begin parsing  |

**Returns:** *number*

The length of the raw [Tx](avmapi_transactions.tx.md)

___

###  fromString

▸ **fromString**(`serialized`: string): *number*

*Defined in [src/apis/avm/tx.ts:518](https://github.com/ava-labs/avalanche.js/blob/eabcc2f/src/apis/avm/tx.ts#L518)*

Takes a base-58 string containing an [Tx](avmapi_transactions.tx.md), parses it, populates the class, and returns the length of the Tx in bytes.

**`remarks`** 
unlike most fromStrings, it expects the string to be serialized in AVA format

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`serialized` | string | A base-58 string containing a raw [Tx](avmapi_transactions.tx.md)  |

**Returns:** *number*

The length of the raw [Tx](avmapi_transactions.tx.md)

___

###  toBuffer

▸ **toBuffer**(): *Buffer*

*Defined in [src/apis/avm/tx.ts:488](https://github.com/ava-labs/avalanche.js/blob/eabcc2f/src/apis/avm/tx.ts#L488)*

Returns a [Buffer](https://github.com/feross/buffer) representation of the [Tx](avmapi_transactions.tx.md).

**Returns:** *Buffer*

___

###  toString

▸ **toString**(): *string*

*Defined in [src/apis/avm/tx.ts:528](https://github.com/ava-labs/avalanche.js/blob/eabcc2f/src/apis/avm/tx.ts#L528)*

Returns a base-58 AVA-serialized representation of the [Tx](avmapi_transactions.tx.md).

**`remarks`** 
unlike most toStrings, this returns in AVA serialization format

**Returns:** *string*
