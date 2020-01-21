### Set credentials
VALUE
```shell script
credhub set --type value 
            --name '/example-value' 
            --password 'sample'
```
PASSWORD
```aidl
credhub set --type password 
            --name '/example-password' 
            --password '3t6Y2OFP0jQIcLnki1h7p3NtSfDx4l9bamr1ja6R'
```
USER
```shell script
user$ credhub set --type user 
            --name '/example-user' 
            --username 'FQnwWoxgSrDuqDLmeLpU' 
            --password '6mRPZB3bAfb8lRpacnXsHfDhlPqFcjH2h9YDvLpL'
```
CERTIFICATE
```shell script
credhub set --type certificate 
            --name '/example-certificate' 
            --root ./root.pem 
            --certificate ./cert.pem 
            --private ./private.pem
```
RSA
```shell script
credhub set --type rsa 
            --name '/example-rsa' 
            --public ./public.pem 
            --private ./private.pem
```

SSH
```shell script
credhub set --type ssh 
            --name '/example-ssh' 
            --public ./public.pem 
            --private ./private.pem
```

### Search credentials
```shell script
credhub find --name 'password'
```
### Get credentials
```shell script
credhub get --name '/key-name'

```
### Delete credentials
```shell script
credhub delete --name '/example-password'
```

### Generate credentials
```shell script
credhub generate --type password --name '/example-password'
credhub generate --type user --name '/example-user'
credhub generate --type certificate --name '/example-certificate' --common-name 'example.com' --ca '/example-ca'
credhub generate --type rsa --name '/example-rsa'
credhub generate --type ssh --name '/example-ssh'
```