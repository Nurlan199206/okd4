## Кластер OpenShift 4.5(OKD) на ноутбуке из 1 master All-in-One.

## Железо ноутбука: 

CPU: Core i7 8gen

RAM: 32GB

DISK: 1TB SSD

ОS: fedora-coreos-32.20200629.3.0-metal.x86_64.raw.xz

OKD release: https://github.com/openshift/okd/releases/tag/4.5.0-0.okd-2020-08-12-020541

![alt text](https://github.com/Nurlan199206/okd4/blob/master/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202020-08-27%20%D0%B2%2001.52.27.png?raw=true)

```openshift-install create manifests```

```openshift-install create ignition-configs```

====================================STATIC IP=============================================

```nmcli con mod "Wired connection 1" ipv4.addresses 10.160.1.x/24
nmcli con mod "Wired connection 1" ipv4.gateway 10.160.1.1
nmcli con mod "Wired connection 1" ipv4.dns "10.201.1.12,10.201.1.13"
nmcli con mod "Wired connection 1" ipv4.method manual - change from DHCP to static
nmcli conn show```

