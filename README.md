# SR-UCMP

## Introduction

EOS lab to play with segment routing and UnEqual Cost Multi-Path (UCMP), created using Containerlab.
The configurations are just for the purpose of lab testing, they are not hardened/etc...

2.0.0.0/8 route received via two different eBGP peering points over two different interfaces wiht different speeds (1G and 10G), usage of extended communities and IS-IS SR will allow router to load balance using different weights that reflect the different interface speeds.

## How to use

1. Configurations are provided, the setup itself was created using ContainerlabClone this repository:
2. Install [Containerlab](https://containerlab.dev/install/).
3. Ensure Docker is installed and running on your system.

## Containerlab

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
