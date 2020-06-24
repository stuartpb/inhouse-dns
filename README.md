# inhouse-dns

This Chart sets up an in-cluster server that serves records for `.internal` domain names as well as (by default) encrypting all DNS lookups.

## Usage

See the usage of external-dns for how to annotate LoadBalancer Service and Ingress records with domain names.

To expose the DNS server to the network, set `coredns.serviceType=LoadBalancer`, as well as `coredns.service.loadBalancerIP` (if you don't want to just go with whatever the LB gives you).
