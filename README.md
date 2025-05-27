# SR-UCMP

## Introduction

EOS lab to play with segment routing and UnEqual Cost Multi-Path (UCMP), created using Containerlab.
The configurations are just for the purpose of lab testing, they are not hardened/etc...

2.0.0.0/8 route received via two different eBGP peering points over two different interfaces wiht different speeds (1G and 10G), usage of extended communities and IS-IS SR will allow routers to load balance using different weights that reflect the different interface speeds.
## Network Topology

![Network Topology](img/topology.clab.drawio.png)

## Setup environment

1 - Setup was created using containerlab, to install it:

```bash
bash -c "$(curl -sL https://get.containerlab.dev)"
```

> [!WARNING]
> For MacOS installation, please refer to containerlab [website](https://containerlab.dev/install/)

1. Ensure Docker is installed and running on your system.
2. CEOS image
 * a. use the [EOS downloader](https://github.com/titom73/eos-downloader)
 * b. if you already have the image in your host you can simply import it into docker

```sh
$ docker import cEOS-lab-$EOS_VERSION.tar ceos:$EOS_VERSION
```

## Containerlab commands

Containerlab is used to deploy and manage the network topology for this project. To start the lab, run:
```sh
containerlab deploy -t topology.clab.yaml
```

To destroy the lab:

```sh
containerlab destroy -t topology.clab.yaml
```

### Credentials

- User: `admin` (no password)

