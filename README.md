Role Name
=========

This role installs a Jenkins server and configures it to be readily usable with
autoproj-jenkins. It assumes a Debian-based system (tested on Ubuntu 16.04),
and installs the packages required by autoproj and autoproj-jenkins.

Role Variables
--------------

In addition to [the variables that control the jenkins
installation](https://github.com/geerlingguy/ansible-role-jenkins), this role
adds the following variables:

- `jenkins_master_labels`: the labels of the master executor. This defaults to
  `autoproj-jenkins` which is the label the autoproj-created jobs are
  restricted to.

Dependencies
------------

This role depends on
[geerlingguy.jenkins](https://github.com/geerlingguy/ansible-role-jenkins). The role injects required plugins in the `jenkins_plugins` variable. You can freely set `jenkins_plugins` without disrupting this.

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
