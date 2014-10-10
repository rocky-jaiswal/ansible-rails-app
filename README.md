# A small Rails server playbook for Ansible

**Bastardised from https://github.com/dodecaphonic/ansible-rails-app**

It installs:

- Ruby 2.1.2
- PostgreSQL
- nginx
- Puma (jungle)

1. Change the app name and deploy directory in <code>vars/defaults.yml</code>.

To run:

    $ vagrant up

There is an example Capistrano `deploy.rb` in this repository that you can use too.

