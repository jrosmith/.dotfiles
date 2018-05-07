Amalgamated from [git-aware-prompt](https://github.com/johnbillion/dotfiles/tree/master/.bash/git-aware-prompt) && [milesszs dotfile](https://github.com/mileszs/dotfiles/blob/master/git-completion.bash)

# Usage
Edit your .bash_profile and append the following:

```
export GITDOTFILES=~/.dotfiles/git-dotfiles

# Inline git branches
source $GITDOTFILES/prompt.sh
export PS1="\W\[\e[0;31m\]\$git_branch\[\e[0;33m\]\$git_dirty\[\e[0m\]\$ "

# Autocomplete git commands/branches
source $GITDOTFILES/autocomplete.sh
```

Restart/reload your terminal
