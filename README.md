# helpful-scripts
terminal scripts that help me

## Hosting
### Digital Ocean and Rancher
##### Create a new droplet that syncs up with rancher
```
curl -X POST -H "Content-Type: application/json" \
-H "Authorization: Bearer <DOAPI TOKEN>" \
-d '{"name":"test-curl","region":"nyc3","size":"1gb","image":"docker","ssh_keys":null,"backups":false,"ipv6":true,"user_data":"#!/bin/bash \n <CMD FROM RANCHER>","private_networking":null,"volumes": null}' "https://api.digitalocean.com/v2/droplets"
```
