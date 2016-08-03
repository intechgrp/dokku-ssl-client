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
```

## usage

```bash
# Install the ca.cert CA and enable ssl client verification on nginx
dokku ssl-client <ca.cert hello-world

# Disable ssl client verification on nginx and remove the CA
dokku ssl-client:remove hello-world

```

