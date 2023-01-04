# Ansible config

This ansible repo is mainly for Ubuntu based system (Ubuntu, Pop_OS!, etc...)

We avoid to automate specific configuration like:
- DisplayLink => for docking station which support displaylink
- Logiops => an unofficial driver for Logitech mice and keyboard

## TODO:

- [ ] Create productivity tasks
- [ ] Install personal dotfiles
- [ ] Refactor: use `import_tasks` only instead of `include_tasks`
- [ ] Refactor: standardize output
- [ ] Refactor: gather tasks by tags
- [ ] Refactor: use `ansible_env` instead of `lookup`
- [ ] Refactor: format yml
- [ ] Create branches for different linux distro
