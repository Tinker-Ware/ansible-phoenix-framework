Phoenix Framework Ansible Role
===

This role will is to provide a ready-to-use [Phoenix Framework](http://www.phoenixframework.org/) 
for [Elixir](http://elixir-lang.org/).

Requirements
---

- NodeJS. V.4x [This role recommended](https://github.com/Oefenweb/ansible-nodejs.git)

Quick usage
---

- hosts: my_host
  roles:
      - { role: nodejs, sudo: yes }
      - { role: phoenix, sudo: yes }

Variables
---
`phoenix_user`: Defines the user that will run Phoenix. Default: `phoenix`
`phoenix_group`: Sets the user's primary group. Default: `phoenix`
`phoenix_groups`: Additional groups for the User. Default: `''`

After provision
---

Everything is setup! You can now run:

```
  mix phoenix.new hello_phoenix --no-ecto
  cd hello_phoenix
  mix phoenix.server
```

The `--no-ecto` flag will create a Phoenix project without Database.

If you want to use the Graphical interface you need to run:
```
  cd hello_phoenix
  npm install babel-preset-es2015 --save
  mix phoenix.server
```

Platforms
---

Debian Jessie.
