# .bash_profile

```
#console colours and magic
parse_git_branch() {
     git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ [\1]/'
}
alias ll='ls -alF'
alias ls='ls -G'
alias cd..='cd ..'
alias f='open -a Finder .'

export PS1="\[$(tput bold)\]\[$(tput setaf 6)\] \w\[$(tput setaf 5)\]\$(parse_git_branch) \[$(tput setaf 1)\]$ \[$(tput sgr0)\]\[$(tput sgr0)\]"

export HISTSIZE=""
git config --global push.default current

# The next line updates PATH for the Google Cloud SDK.
if [ -f '/Users/harrybishop/.bin/google-cloud-sdk/path.bash.inc' ]; then . '/Users/harrybishop/.bin/google-cloud-sdk/path.bash.inc'; fi

# The next line enables shell command completion for gcloud.
if [ -f '/Users/harrybishop/.bin/google-cloud-sdk/completion.bash.inc' ]; then . '/Users/harrybishop/.bin/google-cloud-sdk/completion.bash.inc'; fi

```
