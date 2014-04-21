# timdev-lockdown

## Overview

An ansible role for locking down a newly bootstraped Debian server.

Currently it:

* Disables root login via ssh
* Disables password authentication for SSH
* Installs and configures fail2ban

The role is meant to be easily composable into more complex playbooks.  It expects to be run against a system you can
SSH into as a mortal user, and sudo without a password.  See timdev-bootstrap for a role that will bring a bare server
(just a root account with password) up to spec for this and other timdev- roles.

## Configuration

See defaults/main.yml for a few default variables you can override pretty much anywhere it makes sense for you
(group_vars, host_vars, inventory variables, command-line, etc).
