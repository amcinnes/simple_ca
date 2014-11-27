# Simple certificate authority for local testing

I didn't want to look up the openssl commands to create a CA and sign
certificates again, so I've created this very simple script to make it easier.

## Usage:

### `./ca init 'Angus McInnes Local CA'`

Creates a certificate authority. The private key is stored **unencrypted** in
`ca.key.pem`. The certificate you need to import into your browser is in
`ca.cert.pem`.

### `./ca cert '*.example.com'`

Creates and signs a certificate for `*.example.com`. The certificate and private
key, which you need to give to your web server, are stored in
`_.example.com.cert.pem` and `_.example.com.key.pem` respectively.