k9s Ansible Role
=========

This Ansible role installs k9s, a terminal-based UI for managing Kubernetes clusters, on Ubuntu systems.
It downloads the specified version of k9s from GitHub, extracts the binary, and installs it to /usr/local/bin.

Requirements
------------

1- Ansible 2.9+ (or later).
2- Ubuntu-based hosts with internet access.
3- curl and tar are installed automatically by the role.
4- Sudo privileges are required to install binaries into /usr/local/bin.

Role Variables
--------------

k9s_version: "v0.32.5"    # Version of k9s to install
k9s_download_url: "https://github.com/derailed/k9s/releases/download/{{ k9s_version }}/k9s_Linux_amd64.tar.gz"
k9s_install_path: "/usr/local/bin/k9s"

Dependencies
------------

This role has no dependencies on other roles.

Example Playbook
----------------

    - hosts: localhosts
      roles:
         - install_k9s

License
-------

BSD

Author Information
------------------

Role created by Muhammad Essam.

