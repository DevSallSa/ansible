# DevSallSa's ansible config automation

This is my personal ansible automation process made with long night, tears, blood (yes)
and some holidays sacrificed.

> :warning: Don't try to run my ansible config blindly. It'll prompt an error. See GOAL section

> :warning: This ansible repo is mainly for Ubuntu based system (Ubuntu, Pop_OS!, etc...).

> For now, It's a little Pop_OS! centric but I'll add more distro/OS later

We avoid to automate specific configuration like:

- DisplayLink => for docking station which support displaylink
- Logiops => an unofficial driver for Logitech mice and keyboard

## The goal

Well,

- I want to avoid the hassle of setting up a new UNIX\* dev environment
- Make this repo as a reference for those who want to use ansible for setup automation

## How to use ?

If you really want to use my configs, then use the run script with the
following command:

```bash
$ ./run --skip-tags=git,ssh
```

> You can use all `ansible-playbook` options with the runner

> Logs are in `/tmp/ansible-runner.log`

Available tags are:

- `ansible`: for installing ansible dependencies
- `brave`: for installing brave browser
- `core`: for installing core packages (essential for my workflow) like _ssh, git, stow, flatpak, etc..._
- `desktop`: configure the desktop environment. It works actually with Gnome 42.5
- `docker`: install Docker Desktop
- `dotfiles`: download and install my personal [dotfiles](https://github.com/DevSallSa/.dotfiles)
- `entertainment`: install all entertainment apps
- `flatpak`: install all flatpak apps that I use regardless of the category
- `fonts`: install fonts
- `git`: configure Git. For this you need to adapt the `local.yml` files with your infos
- `install`: install and configure every applications (flatpak, appimages, deb packages, etc...)
- `kitty`: install Kitty Terminal
- `neovim`: install Neovim
- `nodejs`: install Node.js
- `npm`: install _npm_ packages that I use the most
- `productivity`: install all productivity apps
- `starship`: install starship prompt
- `sdkman`: install SDKMAN!
- `ssh`: configure SSH
- `utils`: install all utility apps
- `zsh`: install and configure Z-Shell

Some needs to be run as super user.

## Things todo

- Essential:

  - [x] Make runner script
  - [x] Create productivity tasks
  - [x] Install personal dotfiles
  - [x] Refactor: use `import_tasks` only instead of `include_tasks`
  - [x] Refactor: standardize output
  - [x] Refactor: gather tasks by tags
  - [x] Refactor: use `ansible_env` instead of `lookup`
  - [x] Refactor: format yml
  - [x] Delete temporary processing folder
  - [x] Ask user to reboot system
  - [x] Make this repo public
  - [x] Make final test on a real hardware

- Important:

  - [x] Add option to run script
  - [x] Save log files
  - [ ] Make README.md more clear, more precise, more intuitive

- Wishable:
  - [ ] create a full CLI tool. I can use [bashly](https://github.com/DannyBen/bashly)
  - [ ] Add --help to runner script
  - [ ] Make runner script for removing all the configs
  - [ ] Create branches for different OS (this is veeeeerryyyy optional)
