---
layout: page
title: soc.ialis.me hosting
---

The [tech team](/about/collective/#tech) is responsible of managing the infrastructure, you can read the team's updates
at [@tech](https://soc.ialis.me/@tech), [the blog](/blog/tech/), and by e-mail at
[tech@soc.ialis.me](mailto:tech@soc.ialis.me).


The instance itself is hosted on servers at [Online.net](https://online.net) and
[Scaleway.com](http://scaleway.com), in Paris, France. The database and files are frequently
replicated on a couple of servers, and externally backuped.

The servers are run by an organization (which is mostly @href alone, with no legal grounds; entierly privately owned) called
[random.sh](https://random.sh) / [random labs](https://randomlabs.co); which hosts other services
such as irc.random.sh, a ChatSpike.net IRC Server, [Etherpad.fr](http://etherpad.fr), and much more.
I also intend to one day make it my own company for some products, but I'll then separate the business
with theses community services (the business will just be a sponsor, and without any advertisement, tracking,
or anything else evil).

### Detailed specs

Most of it is hosted on four hosts physical servers with:

* Intel Xeon E3-1231 v3 @ 3.40Ghz (1 socket, 8 cores)
* 32GB of RAM
* 1Tb of HDD storage

They are located at [Online.net][online]'s DC3 located in Ivry, France.

On top of theses server, we use:

* 4 Mastodon VMs
* 1 Redis VM (to be improved soon)
* 1 Minio VM (to be improved soon, with distributed minio)
* 2 PostgreSQL VMs (to be improved soon, shared with [random.sh][random])
* 4 Web-Frontends VMs (shared with [random.sh][random])

We also use other shared VMs with [random.sh][random], hosted at [Scaleway.com][scaleway] :

* e-mail services
* management (ssl, ansible, ...)
* monitoring (located at Scaleway Amsterdam)

### Software and credits

* [Proxmox](https://proxmox.com) for the phsyical servers,
* [FreeBSD](https://freebsd.org) for the VMs,
* [nginx](https://nginx.org) on the web-frontends,
* [varnish](https://varnish-cache.org) on the web frontends for static caching,
* [ansible]() to manage all of that,
* [prometheus]() with [grafana]() for monitoring,
* [elasticsearch]() with [logstash]() and [kibana]() for logging,
* ...

And many many other open-source software. Thanks to all their authors!

[online]: https://online.net
[scaleway]: https://scaleway.com
[random]: https://random.sh

