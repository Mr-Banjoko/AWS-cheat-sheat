## How to encrypt a file using a symetric KMS key via CLI

```
aws kms encrypt \
    --key-id <key_ID_number> \
    --plaintext fileb://<Name of file> \     #provide the full path if the file is not in your working directory 
    --output text \
    --query CiphertextBlob | base64 \
    --decode > <Name-of-the-desired-encrypted-version-of-the-file>
```

## How to decrypt a file using a symetric KMS key via CLI

```
aws kms decrypt \
    --ciphertext-blob fileb://<Name-of-Encrypted-file>  \
    --key-id <key_ID_number> \
    --output text \
    --query Plaintext | base64 \
    --decode > <Name-of-the-desired-decrypted-version-of-the-file>

```
