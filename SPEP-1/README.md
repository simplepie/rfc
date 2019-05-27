---

"Status": APPROVED
"Date Approved": 2019-05-27
"Obsoleted by": None
"Updated by": None
"Obsoletes": None
"Author(s)": Ryan Parman (@skyzyx)

---

# SPEP-1: PHP Version Support Guidelines

## Copyright Notice

This document is made available under the terms of the [`LICENSE`](https://github.com/simplepie/rfc/blob/master/LICENSE) of this repository. The author wishes this document to be copyright-free and part of the public domain.

## Abstract

SimplePie (and its related first- and second-party software) is provided by its authors under the terms of a liberal software license. It is also the desire of the authors to remain "good citizens" of the internet and PHP communities, which includes discouraging the continued use of unmaintained, end-of-life (EOL) software platforms.

## Annual Cadence

Since 2011, [PHP releases are on an annual cadence](https://wiki.php.net/rfc/releaseprocess) where new major versions of PHP are released — and old versions achieve EOL status — every November/December. This means that every November we will be dropping support for the oldest-supported version of PHP and adopting support for the new version of PHP.

Any future changes to the standard PHP release schedule will be adopted by the SimplePie Core Team. This may include extended support for a particular version of PHP (like we saw with PHP 5.6).

## Code Support Schedule

Due to this rationale, the high-level PHP support guidelines for SimplePie (and its related first- and second-party software) are as follows:

* The [latest bugfix releases](https://www.php.net/downloads.php)
* …of [all non-EOL versions of PHP](https://www.php.net/supported-versions.php)
    * …whereas "active support" versions are expected to receive parity support
    * …and whereas "security support" versions are expected to not receive backwards-incompatible changes, but may not gain access to new features that require newer language features
* …not older than PHP 7.2

As an example of how the schedule is expected to work, the two most recent _major.minor_ versions of PHP receive full parity support for new features. The third most recent will see feature-parity on a _best effort_ basis.

### In November/December

In the following table, the _Year_ refers to November/December of that year. Based on [PHP Supported Versions](https://www.php.net/supported-versions.php):

| Year | Active Support | Security Support | EOL |
| ---- | -------------- | ---------------- | --- |
| 2018 | 7.3, 7.2 | _N/A_ | _N/A_ |
| 2019 | 7.4, 7.3 | 7.2 | _N/A_ |
| 2020 | 8.0, 7.4 | 7.3 | 7.2 |
| 2021 | 8.1, 8.0 | 7.4 | 7.3, 7.2 |
| 2022 | 8.2, 8.1 | 8.0 | 7.4, 7.3, 7.2 |
