# Configuration snippets may be placed in this directory as well
includedir /etc/krb5.conf.d/

[logging]
 default = FILE:/var/log/krb5libs.log
 kdc = FILE:/var/log/krb5kdc.log
 admin_server = FILE:/var/log/kadmind.log

[libdefaults]
 dns_lookup_realm = false
 ticket_lifetime = 24h
 renew_lifetime = 7d
 forwardable = true
 rdns = false
 default_realm = AMAZONAWS.COM
 default_ccache_name = KEYRING:persistent:%{uid}

[realms]
 AMAZONAWS.COM = {
  kdc = ip-172-31-17-69.us-west-2.compute.internal
  admin_server = ip-172-31-17-69.us-west-2.compute.internal
 }

[domain_realm]
 .amazonaws.com = AMAZONAWS.COM
 amazonaws.com = AMAZONAWS.COM