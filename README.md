# dokku-ssl-client
A dokku plugin allowing SSL client authentication

## Requirements
* dokku v0.5.x+

## Installation
```
dokku plugin:install https://github.com/dokku/dokku-ssl-client.git ssl-client
```
## commands
```
ssl-client <app> <ca.cert                         Install CA and enable SSL client authentication
ssl-client:remove                                 Remove CA and disable SSL client authentication
ssl-client:add-crl <app> <crl.pem                 Adds a CRL file and configure nginx accordingly
ssl-client:remove-crl <app>                       Removes an existing CRL file if any
```

## usage

```bash
# Install the ca.cert CA and enable ssl client verification on nginx
dokku ssl-client hello-world <ca.cert

# Disable ssl client verification on nginx and remove the CA
dokku ssl-client:remove hello-world

# Add a CRL file for client certificate verification
dokku ssl-client:add-crl hello-world <crl.pem

# Remove the CRL file hello-word <crl.pem
dokku ssl-client:remove-crl hello-world

# Reload nginx
dokku nginx:build-config hello-word
```

