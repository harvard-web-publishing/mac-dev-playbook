# Mac Development Ansible Playbook

This repository is a fork of Jeff Geerling's
[Mac Development Ansible Playbook](https://github.com/geerlingguy/mac-dev-playbook).
See [README-upstream.md](./README-upstream.md) for a copy of the original README
(at the time the fork was created).

## Quick start

If you are setting up a brand-new macOS computer, then follow the
[Setting up a new Mac](https://github.com/harvard-web-publishing/mac-dev-playbook/wiki)
instructions (the home page of the wiki for this project).

## Objectives

The purpose of this project is to

1. Give new members of the team a quick, reliable way to set up their new
   computers.
1. Provide a way for the team to share tools and configuration.

## Configuration

You can customize what gets installed by editing
[default.config.yml](./default.config.yml). You can

- Change what packages get installed and configured.
- Specify a personal dotfiles repository.
- Lots more ...

If you do make changes to the defaults, then you might want to create a personal
branch and commit your changes there. Then you can pull updates to the `main`
branch and merge them into your personal branch.

## Updating

Ansible is designed to be idempotent. If you do not make any changes, then
running a playbook twice should have the same effect as running it once.

1. Change to the root directory of this repository.
1. (Optional) Edit `default.config.yml` to install more or less.
1. Run the playbook:
   - `ansible-playbook main.yml --ask-become-pass`
   - Enter your password at the prompt.

## Major features

- Install [Homebrew](http://brew.sh/) to manage packages.
- Install [Colima](https://github.com/abiosoft/colima) and [DDEV](https://ddev.com/)
  to run Drupal sites (and others) locally.
- Install our preferred text editors/IDEs and configure them (including Xdebug
  support):
  - [Visual Studio Code](https://code.visualstudio.com/) (todo)
  - [Vim](https://www.vim.org/)
