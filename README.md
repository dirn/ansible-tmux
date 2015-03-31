Role Name
=========

[![Build Status](https://travis-ci.org/dirn/ansible-tmux.svg?branch=master)](https://travis-ci.org/dirn/ansible-tmux)

An Ansible role to install [tmux](http://tmux.sourceforge.net/).

Requirements
------------

This role works on OS X and Debian-based OSes. If using OS X, make sure you have
[Homebrew](http://brew.sh/) installed before running the role. If you're looking
for a role to handle it for you, check out
[dirn.homebrew](https://github.com/dirn/ansible-homebrew).

Role Variables
--------------

Several variables are available to configure the role.

To control if [tmuxinator](https://github.com/tmuxinator/tmuxinator) is
installed:

    tmux_install_tmuxinator: false

To use a specific version of Ruby to install tmuxinator:

    tmux_tmuxinator_executable: ~

> See the [gem module documentation](http://docs.ansible.com/gem_module.html)
> for more details.

To control if [tmuxp](http://tmuxp.readthedocs.org/en/latest/) is installed:

    tmux_install_tmuxp: false

To use a specific version of Python to install tmuxp:

    tmux_tmuxp_executable: ~

If you want to install tmuxp into a virtual environment:

    tmux_tmuxp_virtualenv: ~
    tmux_tmuxp_virtualenv_command: ~

> See the [pip module documentation](http://docs.ansible.com/pip_module.html)
> for more details.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: dirn.tmux
          tmux_install_tmuxp: true
          tmux_tmuxp_virtualenv: ~/.local/bin/tmuxp
          tmux_tmuxp_virtualenv_command: pyvenv

License
-------

MIT

Author Information
------------------

This role was created by [Andy Dirnberger](https://github.com/dirn).
