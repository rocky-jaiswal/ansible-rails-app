# A small Rails server playbook for Ansible

**Bastardised from https://github.com/dodecaphonic/ansible-rails-app**

It installs:

- Ruby 2.1.1
- PostgreSQL
- nginx
- Puma (jungle)

1. Change the app name and deploy directory in <code>vars/defaults.yml</code>.
2. Rename `hosts.example` to `hosts` and change it to your hosts (you will get the IP once the VM is setup).

To run:

    $ vagrant up

There is an example Capistrano `deploy.rb` in this repository that you can use too.

