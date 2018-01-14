



(Thoughtbot) dotfiles customization
====================================
[Thoughtbot dotfiles](https://github.com/thoughtbot/dotfiles) will used as basis and afterwards extended by this custom
dotfiles. For details see [Thoughtbot dotfiles](https://github.com/thoughtbot/dotfiles) Github repo.

Install
------------

### Set zsh as your login shell:

    chsh -s $(which zsh)
     
### Clone basis (Thoughbot)[dotfiles](https://github.com/thoughtbot/dotfiles) to your laptop

    git clone git://github.com/thoughtbot/dotfiles.git ~/dotfiles

### Install [Oh My Zsh](https://github.com/robbyrussell/oh-my-zsh)

    sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

### Install rcm:

     brew tap thoughtbot/formulae
     brew install rcm

### Clone custom dotfiles (this repo) to your laptop

    mkdir ~/dotfiles-local
    cd dotfiles-local
    git clone git://github.com/MNicks/dotfiles.git

### Install the dotfiles:

    env RCRC=$HOME/dotfiles/rcrc rcup

After the initial installation, you can run `rcup` without the one-time variable
`RCRC` being set (`rcup` will symlink the repo's `rcrc` to `~/.rcrc` for future
runs of `rcup`). [See
example](https://github.com/thoughtbot/dotfiles/blob/master/rcrc).

This command will create symlinks for config files in your home directory.
Setting the `RCRC` environment variable tells `rcup` to use standard
configuration options:

* Exclude the `README.md` and `LICENSE` files, which are part of
  the `dotfiles` repository but do not need to be symlinked in.
* Give precedence to personal overrides which by default are placed in
  `~/dotfiles-local`
* Please configure the `rcrc` file if you'd like to make personal
  overrides in a different directory
  
Update
------

From time to time you should pull down any updates to these dotfiles, and run

    rcup

to link any new files and install new vim plugins. **Note** You _must_ run
`rcup` after pulling to ensure that all files in plugins are properly installed,
but you can safely run `rcup` multiple times so update early and update often!
