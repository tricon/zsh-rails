Fancy completion for working with Rails via Zsh.

### Commands

    mvd version # Migrate version down

    mvu version # Migrate version up


### Tab Completion

Versions are tab completed and return the migration's filename, but not the full path. This allows one to "fuzzy search":

    mvd create_admin<TAB> # => mvd 20110303232752_create_admins.rb

The commands will then keep only the timestamp, passing it to Rake as an argument. This makes migrating things by version much easier. Currently this only works from the root directory of your Rails project.


### Installing

Move _migration_version to /usr/share/zsh/<version>/functions (or into the function directory wherever your zsh is installed).
Add to your ~/.zshrc (presuming you put alias and config into ~/.dotfiles):

    # .zshrc
    . ~/.dotfiles/alias
    . ~/.dotfiles/config


Please leave comments, suggestions, and issues in the issue tracker. Pull requests are more than welcome!