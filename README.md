# InterPlanetary File System for Business (IPFSfB)

[![Build Status](https://api.travis-ci.org/IBM/IPFSfB.svg?branch=master)](https://travis-ci.org/IBM/IPFSfB)

This repository contains instructions to build a private, unstructured data storage network for any blockchain on distributed file system, InterPlanetary File System for Business (IPFSfB), using crypto tools and Docker images with Docker and Docker Compose to provision the enterprise blockchain storage network.

## Overview

InterPlanetary File System for Business (IPFSfB) is based on InterPlanetary File System, which aim to provide an enterprise form, unstructured data storage network for any blockchain.

## Prerequisites

- [Docker](https://www.docker.com/)
- [Go](https://golang.org/)
- [Git](https://git-scm.com/)

## Building from source

Building from source with IPFSfB repository:

``` bash
go get -u github.com/IBM/IPFSfB
```

Building from souce with IPFSfB tools, Once the repository is downloaded, run:

``` bash
make swarmkeygen
```

or build all utilities:

``` bash
make all
```

## Steps

### Running a private network

Currently, we are offering simple network as one of the samples, it contains three senarios including peer-to-peer, peer-to-server, and peer to peer and to server. You can follow the [tutorial](https://github.com/IBM/IPFSfB/blob/master/samples/simple-network/TUTORIAL.md) to envision and run a private network.


## Runtime instructions

If you are running a private network, [config.sh](https://github.com/IBM/IPFSfB/blob/master/samples/simple-network/config.sh) file will help containers to check runtime health. Regularly inspect docker containers log in the runtime environment may be helpful.

## Scenarios

One of the samples, simple network is avaliable in three scenarios ([p2p](https://en.wikipedia.org/wiki/Peer-to-peer), [p2s](https://zh.wikipedia.org/wiki/P2S), and [p2sp](https://zh.wikipedia.org/wiki/P2SP)).

The scenario guidelines are available at [samples/simple-network](https://github.com/IBM/IPFSfB/tree/master/samples/simple-network).

### Accessing and running

You can access and download network specific binaries and images through [bootstrap.sh](https://github.com/IBM/IPFSfB/blob/master/samples/simple-network/scripts/bootstrap.sh). Once downloaded, you can run these network scenarios by [pnet.sh](https://github.com/IBM/IPFSfB/blob/master/samples/simple-network/pnet.sh).

### End-to-end testing

Each scenarios have end-to-end testing, located in [samples/simple-network/e2e](https://github.com/IBM/IPFSfB/tree/master/samples/simple-network/e2e).

## Troubleshooting

If you encountered a problem for running IPFSfB, raise an issue and mention one of the maintainers in the [maintainers board](https://github.com/IBM/IPFSfB/blob/master/MAINTAINERS.md#maintainers-board).

## Considerations

There are several considerations for the roadmap of IPFSfB.

### Performance and production

For the private or enterprise network performance, such as uploading a file, downloading a file, hosting a web, and even collaborating a documentation from the network, we need more network connection cases and speed performance to test the network.

IPFSfB production will not only include simple network scenarios for private network, but also give a vision for clustering, consensus enabled enterprise network.

### Extension

- General data interface for any blockchain
- VS Code extension
- Hyperledger Fabric extension

## Architecture
