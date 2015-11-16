# Ansible Role: EPEL Repository

Installs the EPEL repository (Extra Packages for Enterprise Linux) for RHEL/CentOS.

## Requirements

This role only is needed/runs on RHEL and its derivatives.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

epel_repo_url: "https://dl.fedoraproject.org/pub/epel/epel-release-latest-{{ ansible_distribution_major_version }}.noarch.rpm"
epel_repo_gpg_key_url: "/etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-{{ ansible_distribution_major_version }}"

The EPEL repo URL and GPG key URL. Generally, these should not be changed, but if this role is out of date, or if you need a very specific version, these can both be overridden.

## Dependencies

None.

## Example Playbook

    - hosts: servers
      roles:
        - { role: jgeusebroek.epel }

## License

MIT / BSD

## Author Information

Forked from [Jeff Geerling](http://jeffgeerling.com/).