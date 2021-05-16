
# Specifications

.*The functions stated below are arranged serially*

## GenerateKeyPair

    ```text
    > produces client's public & private key (ECDH algorithm - P-256 elliptic curve)
    > returns the keys in JWK format
    ```

.*Key exchange phase*

## DeriveKey

    ```text
    > after public key exchange, imports keys from JWK format
    > combines own private key with another's public key (AES-GCM algorithm)
    > returns the derivedKey
    ```

## Encrypt

    ```text
    > converts text & algorithm to bytes
    > encrypts the bytes
    > converts encrypted bytes to Uint8Array to string to base64
    > returns encrypted base64 data
    ```

.*Message exchange phase*

## Decrypt

    ```text
    > initializes text to Uint8Array
    > initializes algorithm
    > decrypts Uint8Array with algorithm
    > decodes decrypted Uint8Array data to base64
    > returns decrypted base64 data
    ```
