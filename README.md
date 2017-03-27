Supported tags and respective `Dockerfile` links
================================================

  * [`latest` (Dockerfile)](https://github.com/wernight/docker-squid/blob/master/Dockerfile) [![](https://images.microbadger.com/badges/image/wernight/squid.svg)](https://microbadger.com/images/wernight/squid "Get your own image badge on microbadger.com")


What is Squid
-------------

[**Squid**](http://www.squid-cache.org/) is a forward proxy with caching and authentication.
It support `http://`, `ftp://`, with limited support for `https://`, `wss://` and TLS/SSL in general (but not `ws://`, i.e. WebSocket `UPGRADE` without TLS encapsulation, and not SOCKS protocol).


Usage example
-------------

    $ docker run -d -p 3128:3128 wernight/squid
    
Then you may set to use the proxy, for example via:

    $ curl --proxy http://localhost:3128/ example.com

Customize settings in `/etc/squid/squid.conf`. For example on Kubernetes you
probably want to set `dns_defnames on`.


Feedbacks
---------

Suggestions are welcome on our [GitHub issue tracker](https://github.com/wernight/docker-squid/issues).
