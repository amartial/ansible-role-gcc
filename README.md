Ansible Role: GCC
=================

[//]: <> (Comment)
[//]: <> (A brief description of the role goes here.)

Install [GNU Compiler Collection (GCC)](https://gcc.gnu.org/) on Centos 7 from sources.

_Work in progress_
***

Requirements
------------

[//]: <> (Any pre-requisites that may not be covered by Ansible itself 
or the role should be mentioned here. For instance, if the role uses the EC2 module, 
it may be a good idea to mention in this section that the boto package is required.
)

None

Role Variables
--------------

[//]: <> (A description of the settable variables for this role should go here,
including any variables that are in defaults/main.yml, vars/main.yml, 
and any variables that can/should be set via parameters to the role. 
Any variables that are read from other roles and/or the global scope 
\(ie. hostvars, group vars, etc.\) should be mentioned here as well.
)

Available variables are listed below, along with default values (see [`defaults/main.yml`](defaults/main.yml)):

| Variable  |  	Default  | Comments  |
|---|---|---|
| `gcc_version`   | [9.3.0](https://gcc.gnu.org/releases.html) | Choose gcc version to install  |
| `gcc_install_dir`  | /opt/gcc/[gcc_version]-gcc[gcc_sys_version]     | Directory where to install gcc   |
| `gcc_configure_args`  |  \[--disable-multilib, \]  | Arguments to pass to `configure`  |
                         
Dependencies             
------------       
      
[//]: <> (A list of other roles hosted on Galaxy should go here, 
plus any details in regards to parameters that may need to be set for other roles, 
or variables that are used from other roles.
)

None

*Optional roles:*

- role: `korzeczl/gmp` *(Not yet available)*
- role: `korzeczl/mpfr` *(Not yet available)*
- role: `korzeczl/mpc` *(Not yet available)*
- role: `korzeczl/isl` *(Not yet available)*

Example Playbook
----------------

[//]: <> (Including an example of how to use your role \(for instance, with variables passed in as parameters\) is always nice for users too:)

    - hosts: servers
      roles:
        - role: korzeczl.gcc

License
-------

[//]: <> (Comment)

[MIT][link-license]

Author Information
------------------

[//]: <> (An optional section for the role authors to include contact information, 
or a website \(HTML is not allowed\).)

This role was created in 2020 by Laurent Korzeczek.

[link-license]: https://gitlab.com/ansible-roles-korzeczl/gcc/-/blob/master/LICENSE
[link-galaxy]: https://galaxy.ansible.com/korzeczl/gcc