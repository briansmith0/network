Changelog
=========

[1.4.0] - 2021-08-10
--------------------

### Changes

- Drop the support for Ansible 2.8
- Display the `stderr_lines` only by default
  - All the config parameters can still be displayed as previous using
    `ansible-playbook -v`

### New features

- Support Simultaneous Authentication of Equals(SAE) authentication
- Support Opportunistic Wireless Encryption (OWE)
- Support Ethtool ring settings
- Support `auto_gateway` option

### Bug fixes

- Fix static IPv6 support for initscripts provider
- Fix `dns_search` and `dns_options` support for all address family
- Fix deprecation warning on Ethtool setting
- Fix the idempotence when applying the same network connection twice

[1.3.0] - 2021-04-08
--------------------

### Changes

- Use inclusive language
  - `slave` is deprecated in favor of `port`
  - `master` is deprecated in favor of `controller`

### New features

- Support disabling IPv6
- Support `dns_options` when using one or more IPv4 nameservers
- Support Ethtool coalesce settings
- Support dummy interfaces

### Bug fixes

- Fix static IPv6 support for initscripts provider

[1.2.0] - 2020-08-26
--------------------

### Changes

- Rename ethtool features to use underscores instead of dashes to support
  Jinja2 dot notation. Accept old notation for compatibility with existing
  playbooks.

### New features

- Initial 802.1x authentication support (only EAP-TLS)
- Wireless support
- Handle OracleLinux as a RHEL clone
- Remove dependency on ethtool command line tool
- initscripts: Support creating and activating bond profiles in one run
- Ignore up/down states if a profile is not defined and not present on the
  managed host
- Document bond profiles

### Bug fixes

- NetworkManager: Always rollback checkpoint on failure
- NetworkManager: Try to reapply changes to reduce network interruptions
- initscripts: Fix dependencies for Fedora 32
- Only log actual warnings as Ansible warnings
