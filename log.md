
# Specifications

.*The functions stated below are arranged serially*

## GenerateKeyPair

    ```
    > produces client's public & private key (ECDH algorithm - P-256 elliptic curve)
    > returns the keys in JWK format
    ```

.*Key exchange phase*

## DeriveKey

    ```
    > after public key exchange, imports keys from JWK format
    > combines own private key with another's public key (AES-GCM algorithm)
    > returns the derivedKey
    ```

## Encrypt

    ```
    > converts text & algorithm to bytes
    > encrypts the bytes
    > converts encrypted bytes to Uint8Array to string to base64
    > returns encrypted base64 data
    ```

.*Message exchange phase*

## Decrypt

    ```
    > initializes text to Uint8Array
    > initializes algorithm
    > decrypts Uint8Array with algorithm
    > decodes decrypted Uint8Array data to base64
    > returns decrypted base64 data
    ```
