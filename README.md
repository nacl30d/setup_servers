Server setup utilities
===

Install and configure following services.  

* DNS: `dnsmasq` as local dns server

Configures
---

### Basic

* Create your inventory file like `inventory/hosts.sample`

### DNS

* Set local domain at `domain: "<YOUR_DOMAIN_HERE>"` in `roles/dns/vars/dns.yml`
* Set hosts file as `hosts-dnsmasq` in `roles/dns/files`
  * For exsample, this repo contains `hosts-dnsmasq.sample`

Usage
---

### Dry-Run

To check diff of configure files, run this.  

``` sh
$ ansible-playbook -i inventory/hosts --diff --check
```

### Install

``` sh
$ ansible-playbook -i inventory/hosts main.yml
```
