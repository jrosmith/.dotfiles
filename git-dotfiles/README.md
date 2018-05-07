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

# Configuring your PS1
Prompt String 1 is by default configured to output the basename of the current working directory followed by the branch. For example, if you were working on the master branch of a project with located at ~/Documents/project, the PS1 would output `project(master)$`

To configure your PS1, change the PS1 variable in your `bash_profile`. A list of control commands are available [here](https://www.linuxnix.com/linuxunix-shell-ps1-prompt-explained-in-detail/)

This dotfile to outputs red (e[0;31m]) branches with a yellow (e[0;33m] asterisk if a pending commit is detected. Other color codes can be found [here](https://en.wikipedia.org/wiki/ANSI_escape_code#Colors)

