

<!-- MarkdownTOC -->

- [0 - Overview][0---overview]
  - [0.1 - Goal][01---goal]
    - [Setup][setup]
    - [Usage][usage]
  - [0.2 - Resources][02---resources]
    - [Docker images][docker-images]

<!-- /MarkdownTOC -->



# 0 - Overview

## 0.1 - Goal

### Setup

Have a local Development environment with:

* 3 Consul-servers (1 cluster)
* 1 Consul-Agent client (to test usage)

* 1 **Shell** with ```consul-template```
* 1 **Shell** with ```consul``` Binary and CLI
* 1 **Shell** with ```consul-cli``` and other tools to test and interact with Consul KV / Catalog


### Usage

Be able to define automate / usage in other projects with:

* To **load Data** into KV store
* To test Agent registering configuration
* Test utilities to interact and usge Consul KV / Catalog from User point of view




## 0.2 - Resources

### Docker images

#### Consul

* https://hub.docker.com/u/gliderlabs/
* https://github.com/gliderlabs/docker-consul
  - consul
  - consul-agent
  - consult-server

> Need:
>  * Build or volume 
>  * ```config.d``` and config files ...



#### Consul-template

* https://github.com/avthart/docker-consul-template/
  - Base Alpine
  - Install Consul-template
  - **Link** to Docker HOST Unix socket (For integration with **Registrator**)
  - **ENTRYPOINT** on ```consul-template```
  => Binary usage


* https://github.com/CiscoCloud/docker-consul-template/
  - Base Alpine
  - Install Consul-template
  - Set as **CMD**
  => Can be overwritten to Shell into :D
  => But ... can not pass argument as BINARY

> **To use as a base** for another image:



#### docker-compose environment

* https://github.com/micahhausler/consul-demo/blob/master/docker-compose.yml

> WARNING ...
> * This does not seems to work with ```gliderlabs/consul``` images








