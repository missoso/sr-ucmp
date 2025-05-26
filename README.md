# SR-UCMP

## Introduction

EOS lab to play with segment routing and UnEqual Cost Multi-Path (UCMP), created using Containerlab.
The configurations are just for the purpose of lab testing, they are not hardened/etc...

2.0.0.0/8 route received via two different eBGP peering points over two different interfaces wiht different speeds (1G and 10G), usage of extended communities and IS-IS SR will allow routers to load balance using different weights that reflect the different interface speeds.

## Setup environment

Setup was created using containerlab, to install it:

```bash
bash -c "$(curl -sL https://get.containerlab.dev)"
```

> [!WARNING]
> For MacOS installation, please refer to containerlab [website](https://containerlab.dev/install/)

Also ensure Docker is installed and running on your system.

## Containerlab commands

Containerlab is used to deploy and manage the network topology for this project. To start the lab, run:
```sh
containerlab deploy -t topology.clab.yaml
```
To destroy the lab:
```sh
containerlab destroy -t topology.clab.yaml
```

## Network Topology

The following diagram shows the network topology used in this project:

[![Network Topology](img/topology.clab.drawio.png)](img/topology.clab.drawio.png)
