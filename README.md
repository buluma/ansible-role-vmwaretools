# [vmwaretools](#vmwaretools)

Installation of vmware-tools package and repostory.

|GitHub|GitLab|Quality|Downloads|Version|Issues|Pull Requests|
|------|------|-------|---------|-------|------|-------------|
|[![github](https://github.com/buluma/ansible-role-vmwaretools/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-vmwaretools/actions)|[![gitlab](https://gitlab.com/buluma/ansible-role-vmwaretools/badges/master/pipeline.svg)](https://gitlab.com/buluma/ansible-role-vmwaretools)|[![quality](https://img.shields.io/ansible/quality/)](https://galaxy.ansible.com/buluma/vmwaretools)|[![downloads](https://img.shields.io/ansible/role/d/)](https://galaxy.ansible.com/buluma/vmwaretools)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-vmwaretools.svg)](https://github.com/buluma/ansible-role-vmwaretools/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-vmwaretools.svg)](https://github.com/buluma/ansible-role-vmwaretools/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-vmwaretools.svg)](https://github.com/buluma/ansible-role-vmwaretools/pulls/)|

## [Example Playbook](#example-playbook)

This example is taken from `molecule/default/converge.yml` and is tested on each push, pull request and release.
```yaml
---
- name: Converge
  hosts: all
  become: true

  roles:
    - role: buluma.vmwaretools
```

The machine needs to be prepared. In CI this is done using `molecule/default/prepare.yml`:
```yaml
---
- name: prepare
  hosts: all
  become: yes
  gather_facts: no

  roles:
    - role: buluma.bootstrap
```


## [Role Variables](#role-variables)

The default values for the variables are set in `defaults/main.yml`:
```yaml
---
# defaults file for vmwaretools

#   The version of VMware Tools to install. Possible values can be found here:
#   http://packages.vmware.com/tools/esx/index.html
vmwaretools_tools_version: latest

#   The server which holds the YUM repository. Customize this if you mirror
#   public YUM repos to your internal network.
vmwaretools_yum_server: https://packages.vmware.com

#   The path on *yum_server* where the repository can be found. Customize
#   this if you mirror public YUM repos to your internal network.
vmwaretools_yum_path: /tools

#   Repository package version
#   For example: 9.4.10-1 version for http://packages.vmware.com/tools/esx/latest/repos/vmware-tools-repo-RHEL6-9.4.10-1.el6.x86_64.rpm
#   If it is not specified it's autodetected by "Get repository package version if vmwaretools_repo_version is undefined." task.
# vmwaretools_repo_version: 8.6.16-1
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-vmwaretools/blob/main/requirements.txt).

## [Status of used roles](#status-of-requirements)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | GitLab |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Build Status GitHub](https://github.com/buluma/ansible-role-bootstrap/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions)|[![Build Status GitLab ](https://gitlab.com/buluma/ansible-role-bootstrap/badges/master/pipeline.svg)](https://gitlab.com/buluma/ansible-role-bootstrap)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-vmwaretools/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|fedora|all|
|el|8|
|opensuse|all|
|ubuntu|all|
|debian|all|
|freebsd|all|

The minimum version of Ansible required is 2.3, tests have been done to:

- The previous version.
- The current version.
- The development version.



If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-vmwaretools/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-vmwaretools/blob/master/CHANGELOG.md)

## [License](#license)

Apache-2.0

## [Author Information](#author-information)

[Michael Buluma](https://buluma.github.io/)
