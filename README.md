# silpion/ansible-httpd

## Synopsis

```
- hosts: all
  vars:
    httpd_listen_on:
      - 127.0.0.1:2000
    httpd_extra_modules:
      - mod_ldap
```
## Description

A role to configure a basic httpd


## Role Variables

* ``httpd_listen_on``: A list of sockets to listen on (default: ``['0.0.0.0:80']``)
* ``httpd_extra_modules``: A list of extra packages to install (default: ``[]``)

## Example Playbook

```yaml
- name: Test ansible-httpd
  hosts: all
  roles:
    - ansible-httpd
```

## Contributing

If you want to contribute to this repository please be aware that this
project uses a [gitflow](http://nvie.com/posts/a-successful-git-branching-model/)
workflow with the next release branch called ``next``.

Please fork this repository and create a local branch split off of the ``next``
branch and create pull requests back to the origin ``next`` branch.

## License

Apache Version 2.0

## Integration testing

This role provides integration tests using the Ruby RSpec/serverspec framework
with a few drawbacks at the time of writing this documentation.

Running integration tests requires a number of dependencies being
installed. As this role uses Ruby RSpec there is the need to have
Ruby with rake and bundler available.

```shell
# install role specific dependencies with bundler
bundle install
```

<!-- -->

```shell
rake suite
```


## Author information

Alvaro Aleman


<!-- vim: set nofen ts=4 sw=4 et: -->
