# vrnetlab Docker Images

This repository contains Github Actions workflow that builds and publishes [vrnetlab](https://github.com/hellt/vrnetlab) Ubuntu images. The resulting images can be used with [containerlab](https://containerlab.dev/).

## How to use with containerlab

Below is an example containerlab topology file:

```yaml
name: example-lab
topology:
  nodes:
    example01:
      kind: generic_vm
      image: ghcr.io/dteslya/vrnetlab-images/ubuntu-vrnetlab:jammy
  links:
    - type: dummy
      endpoint:
        node: example01
        interface: eth1
```
