# SPEP-1: PHP Version Support Guidelines

| State | Value |
| ------------ | ------ |
| Obsoleted by | _None_ |
| Updated by | _None_ |
| Obsoletes | _None_ |

## Copyright Notice



## Abstract

   The Hypertext Transfer Protocol (HTTP) is an application-level
   protocol for distributed, collaborative, hypermedia information
   systems. It is a generic, stateless, protocol which can be used for
   many tasks beyond its use for hypertext, such as name servers and
   distributed object management systems, through extension of its
   request methods, error codes and headers [47]. A feature of HTTP is
   the typing and negotiation of data representation, allowing systems
   to be built independently of the data being transferred.

   HTTP has been in use by the World-Wide Web global information
   initiative since 1990. This specification defines the protocol
   referred to as "HTTP/1.1", and is an update to RFC 2068 [33].









We support:

* The latest bugfix releases
* …of [all non-EOL versions of PHP](https://www.php.net/supported-versions.php)
* …not older than PHP 7.2

## Annual Cadence

Since 2011, [PHP releases are on an annual cadence](https://wiki.php.net/rfc/releaseprocess) where new major versions of PHP are released every November/December. This means that every November we will be dropping support for the oldest-supported version of PHP.
