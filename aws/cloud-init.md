# cloud-init

## How to remove cloud-init from host

```bash
$ echo 'datasource_list: [ None ]' | sudo -s tee /etc/cloud/cloud.cfg.d/90_dpkg.cfg
$ apt-get remove --purge cloud-init
$ rm -rf /etc/cloud/; sudo rm -rf /var/lib/cloud/
```
