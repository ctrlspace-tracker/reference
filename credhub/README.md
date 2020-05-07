### Set credentials
VALUE
```shell script
credhub set --type value 
            --name '/sample-value' 
            --password 'sample'
```
PASSWORD
```aidl
credhub set --type password 
            --name '<password-name>' 
            --password '<password>'
```
USER
```shell script
user$ credhub set --type user 
            --name '/sample-user' 
            --username '<username>' 
            --password '<password>'
```
CERTIFICATE
```shell script
credhub set --type certificate 
            --name '/sample-certificate' 
            --root <./locationofrootcert.pem> 
            --certificate <./locationofcert.pem> 
            --private <./locationofrootprivate.pem>
```
RSA
```shell script
credhub set --type rsa 
            --name '/sample-rsa' 
            --public <publickep.pem> 
            --private <privatekey.pem>
```

SSH
```shell script
credhub set --type ssh 
            --name '/samplessh' 
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
credhub delete --name '/sample-password'
```

### Generate credentials
```shell script
credhub generate --type password --name '/sample-password'
credhub generate --type user --name '/sample-user'
credhub generate --type certificate --name '/sample-certificate' --common-name 'sample.com' --ca '/sample-ca'
credhub generate --type rsa --name '/sample-rsa'
credhub generate --type ssh --name '/sample-ssh'
```
