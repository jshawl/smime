

### Install `smimesign`

```
brew install smimesign
```

### Generate x509 cert

https://www.linkedin.com/pulse/create-self-signed-x509-certificate-using-openssl-windows-bhosale/

```
openssl req -x509 -days 365 -newkey rsa:2048 –keyout my-key.pem -out my-cert.pem 
openssl pkcs12 -export -in my-cert.pem -inkey my-key.pem -out test-cert.pfx 
```

### Import test-cert.pfx to keychain


### Configure Git

```
git config --global gpg.x509.program smimesign
git config --global gpg.format x509
smimesign --list-keys
git config --local user.signingkey 0ff455a2708394633e4bb2f88002e3cd80cbd76f
```
