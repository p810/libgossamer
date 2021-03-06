# Libgossamer API Reference - DbInterface

* **Fully Qualified Interface Name**: `ParagonIE\Gossamer\DbInterface`

## Constants

| Constant | Value |
|----------|-------|
| `GOSSAMER_PROTOCOL_VERSION` | `1.0.0` |
| `TABLE_META` | `gossamer_meta` |
| `TABLE_PROVIDERS` | `gossamer_providers` |
| `TABLE_PUBLIC_KEYS` | `gossamer_provider_publickeys` |
| `TABLE_PACKAGES` | `gossamer_packages` |
| `TABLE_PACKAGE_RELEASES` | `gossamer_package_releases` |

## Interface Methods

### `getCheckpointHash()`

**Returns** a `string`

### `updateMeta()`

**Arguments**:

1. `string` - Checkpoint Hash

**Returns** a `bool`.

### `appendKey()`

**Arguments**:

1. `string` - Provider
2. `string` - Public Key
3. `array` - Metadata
4. `string` - Hash

**Returns** a `bool`.

### `revokeKey()`

**Arguments**:

1. `string` - Provider
2. `string` - Public Key
3. `array` - Metadata
4. `string` - Hash

**Returns** a `bool`.

### `appendUpdate()`

**Arguments**:

1. `string` - Provider
2. `string` - Package
3. `string` - Public Key
4. `string` - Release (version)
5. `string` - Signature (of the release file)
6. `array` - Metadata
7. `string` - Hash

**Returns** a `bool`.

### `revokeUpdate()`

**Arguments**:

1. `string` - Provider
2. `string` - Package
3. `string` - Public Key
4. `string` - Release (version)
5. `array` - Metadata
6. `string` - Hash

**Returns** a `bool`.

### `providerExists()`

**Arguments**:

1. `string` - Provider Name

**Returns** a `bool`.

### `getPublicKeysForProvider()`

**Arguments**:

1. `string` - Provider Name

**Returns** an `array` of `string`s. 

### `getPackageId()`

**Arguments**:

1. `string` - Package Name
2. `int` - Provider ID

**Returns** an `int`.

### `getProviderId()`

**Arguments**:

1. `string` - Provider Name

**Returns** an `int`.

### `getPublicKeyId()`

**Arguments**:

1. `string` - Public Key
2. `int` - Provier ID

**Returns** an `int`.
