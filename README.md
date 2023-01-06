# DevSallSa's ansible config automation

This is my personal ansible automation process made with long night, tears, blood (yes) 
and some holidays sacrificed.
> :warning: This ansible repo is mainly for Ubuntu based system (Ubuntu, Pop_OS!, etc...)

> :warning: Don't try to run my ansible config blindly. It'll prompt an error. See GOAL section

We avoid to automate specific configuration like:
- DisplayLink => for docking station which support displaylink
- Logiops => an unofficial driver for Logitech mice and keyboard

## The goal

Well,

- I want to avoid the hassle of setting up a new UNIX\* dev environment
- Make this repo as a reference for those who want to use ansible for setup automation


If you really want to use my configs, then use the following command:
```bash
# options are not implemented yet
$ ./run --skip-tags=ssh,authorized-ssh-keys
```

## Things todo

- Essential:
    + [x] Make runner script
    + [x] Create productivity tasks
    + [ ] Install personal dotfiles
    + [ ] Refactor: use `import_tasks` only instead of `include_tasks`
    + [ ] Refactor: standardize output
    + [ ] Refactor: gather tasks by tags
    + [ ] Refactor: use `ansible_env` instead of `lookup`
    + [ ] Refactor: format yml

- Important:
    + [ ] Add option to run script
    + [ ] Make README.md more clear, more precise, more intuitive
    + [ ] Make this repo public
- Wishable:
    + [ ] Make runner script for removing all the configs
    + [ ] Create branches for different OS (this is veeeeerryyyy optional)
