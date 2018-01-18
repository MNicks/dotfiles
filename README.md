# dotfiles

This is a companion repo to [thoughtbot/dotfiles][1] including an install script for oh-my-zsh and for thoughtbot's dotfiles. It is heavily inspired by [Evie's dotfiles](https://github.com/webel/dotfiles)

## Includes

- Install script for `thoughtbot/dotfiles`
- config for zshrc (see `thoughtbot/dotfiles` for description on how they treat local dotfiles)

  - this config is basically the default created by `oh-my-zsh`, although with these plugins: `git` `docker` `brew` `docker-compose` `docker` `httpie` `node` `npm` `osx` `sudo` `zsh-autosuggestions` `history` `history-substring-search`

## Remark


Instead invocing directly it is highly recommended to run the  [mac-dev-playbook](https://github.com/MNicks/mac-dev-playbook) as it will install this dotfiles automatically. When installing this dotfiles seperatly as post install step you should one time run `~/.osx.local`.
   
## Install
- clone the repo

      > git clone --recurse-submodules https://github.com/MNicks/dotfiles.git ~/dotfiles-local

- run `INSTALL/install.sh`

      > . ~/dotfiles-local/INSTALL/install.sh

  + sets default shell to `zsh`
  + installs `oh-my-zsh`
  + installs brew if not present
  + clones Github repo [`thoughtbot/dotfiles`][1] into `~/dotfiles`
  + install `rcrc` (for `thoughtbot/dotfiles`)
  + set `RCRC` env and runs `rcup` (for `thoughtbot/dotfiles` aswell as the linking of these local dotfiles)

## Links
- [thoughtbot/dotfiles][1]

#### ZSH
- [Powerline patched fonts][3]
- [Agnoster theme][4]
- [powerlevel9k theme][5]
- [Install latest ZSH with brew][6]

[1]:https://github.com/thoughtbot/dotfiles
[3]:https://github.com/powerline/fonts
[4]:https://github.com/agnoster/agnoster-zsh-theme
[5]:https://github.com/bhilburn/powerlevel9k
[6]:https://rick.cogley.info/post/use-homebrew-zsh-instead-of-the-osx-default/
