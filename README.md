# zsh_setting

https://qiita.com/taijuf212/items/57fccf4550ac6a983b8d
#zshrc
alias vz='vim ~/.zshrc'
alias sz='source ~/.zshrc'

# git
alias g='git'
alias gst='git status'
alias gb='git branch'
alias gc='git checkout'
alias gsw='git switch'
alias gct='git commit'
alias gg='git grep'
alias ga='git add'
alias gd='git diff'
alias gl='git log'
alias gfo='git fetch origin'
alias gcm='git commit -m'
alias gpo='git push origin'



# ruby
alias rspec=‘bundle exec rspec’
alias lint=‘bundle exec rubocop -A’

# rbenv
export PATH="$HOME/.rbenv/bin:$PATH"
eval "$(rbenv init -)"


# コマンド補完
autoload -U compinit && compinit -u

# 日本語ファイル名を表示可能にする
setopt print_eight_bit
