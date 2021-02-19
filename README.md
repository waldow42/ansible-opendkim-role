# opendkim

Install and configure OpenDKIM to apply DKIM signatures to mail in large or
complex installations that require using Signing and Key Tables to define
signing instructions.

# Role Variables

opendkim_signing_table: Signing Table dataset

opendkim_key_table: Key Table dataset

Documentation on the allowed syntax of datasets is available here:
http://www.opendkim.org/opendkim.8.html#DATA%20SETS

## Options

* packages_focal_opendkim: Package name to install. Default: opendkim

* opendkim_socket: Socket where opendkim listens for milter connections from the
  MTA. Default: inet:10027@0.0.0.0

* opendkim_signature_algorithm: Algorithm used for all signing. Default:
  rsa-sha256

* opendkim_debug: Toggle verbose logging. Default: no

# Example Playbook
```yaml
  - hosts: mail_hostgroup
    roles:
      - role: opendkim
```

# Author Information

DreamHost
