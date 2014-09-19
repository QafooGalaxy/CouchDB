# BootstrapRole

**Note:** *Roles should be named to reflect what they are doing properly. Upper
and lowercase letters are supposed to be used where applicable. If multiple
parts/words are needed they are supposed to be written in
[CamelCase](http://en.wikipedia.org/wiki/CamelCase).*

**Note:** *Not needed folder inside the bootstrap filestructure should be
deleted inside the corresponding role repository*

## Description

This role is just an example. It is supposed to serve as a template for the
creation of new [Ansible](http://www.ansible.com/) roles in the context of
[QafooGalaxy](http://qafoogalaxy.github.io/).

**Note:** *The description of any role should be a short precise definition of what it is
intended to do*

## Usage

```yaml
- role: BootstrapRole
  versions:
      - "0.8"
      - "0.10"
      - "0.11"
  default: "0.10"
```

## Explicit Dependencies

- SomeOtherRole
    - optional: special options this role needs to be configured with
- EvenAnotherRole

**Note:** *Explicit dependencies are dependencies, which are needed to be
installed for this role to work, but can not be installed using
[meta/dependencies](http://docs.ansible.com/playbooks_roles.html#role-dependencies)
due to specialized configuration.*

*An example of such a dependency is the
[npm](https://github.com/QafooGalaxy/npm) role, which needs a configured nodejs
environment. Nodejs however can be installed using different approaches and/or
in different versions. (eg. using the [nvm] role, which can not properly be
required using
[meta/dependencies](http://docs.ansible.com/playbooks_roles.html#role-dependencies).*

*Most roles do not have explicit dependencies. In this case the whole section
should be deleted*

## Configuration

`a-configuration-option`: description of this configuration value.

`another-complex-configuration-option`: list of programming language names to
be installed

**Example**:
```yaml
names:
    - "JavaScript"
    - "C++"
    - "PHP"
```

*optional* `some-configuration-option`: description of this configuration value. (Default:
`some default value chosen, if not supplied`)


**Note:** *Each available configuration option needs to be documented. In case
an option is a little more complex an example may be given to describe its
usage even further. Optional options are supposed to be mentioned at the end of
the list. They need to be marked using the `optional` keyword. Furthermore each
optional value needs a specification of a default value*

## Implicit Dependencies

- ImplicitDependency
- AnotherImplicit Dependency

**Note:** *Implicit dependencies are dependencies, which are enforced using
[meta/dependencies](http://docs.ansible.com/playbooks_roles.html#role-dependencies).
If no implicit dependency exists this section should be deleted.*

## Further Remarks

Any further remarks about this role. Something like "Warning: takes a long time
to install" or "May interfere with $someService", are possible remarks.

**Note:** *If no further remarks are needed this section should be deleted.*

