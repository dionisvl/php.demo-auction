# oauth2

https://oauth2.thephpleague.com/installation/

### Generating public and private keys for JWT
- Сформируем приватный ключ
```
openssl genrsa -out private.key 2048
```
- Сформировать по этому приватному ключу новый публичный ключ:
```
openssl rsa -in private.key -pubout -out public.key
```
- Generating encryption key
```
php -r 'echo base64_encode(random_bytes(32)), PHP_EOL;'
```
