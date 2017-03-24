# docker-squid

Dockerized [Squid](http://www.squid-cache.org/) forward proxy with caching.

This is an *experimental* version not fully tested.

## Usage

    $ docker run -d -p 3128:3128 wernight/squid
    
Then you may set to use the proxy, for example via:

    $ curl --proxy http://localhost:3128/ example.com

Customize settings in `/etc/squid/squid.conf`. For example on Kubernetes you
probably want to set `dns_defnames on`.
