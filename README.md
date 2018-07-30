# node_https_server
利用node express 创建https server


### mac OS 自带openssl工具， 可以生成SSL协议所需的证书文件，
- private.pem: 私钥
- csr.pem: CSR证书签名
- file.crt: 证书文件

mac Terminal:
```
desktop> openssl
OpenSSL> genrsa -out private.pem 1024
OpenSSL> req -new -key private.pem -out csr.pem
OpenSSL> x509 -req -days 365 -in csr.pem -signkey private.pem -out file.crt
```
