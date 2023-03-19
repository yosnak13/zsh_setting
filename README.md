# ----------------------------
# Added automatically by Powerlevel10k
# config can be reset: 'p10k configure'
# ----------------------------
# Enable Powerlevel10k instant prompt. Should stay close to the top of ~/.zshrc.
# Initialization code that may require console input (password prompts, [y/n]
# confirmations, etc.) must go above this block; everything else may go below.
if [[ -r "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh" ]]; then
  source "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh"
fi

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
alias gp='git pull'
alias gpsh='git push'

# ruby
alias rspec=‘bundle exec rspec’
alias lint=‘bundle exec rubocop -A’

# rbenv
export PATH="$HOME/.rbenv/bin:$PATH"
eval "$(rbenv init -)"


# ----------------------------
# Added by Zinit's installer
# ----------------------------
if [[ ! -f $HOME/.local/share/zinit/zinit.git/zinit.zsh ]]; then
    print -P "%F{33} %F{220}Installing %F{33}ZDHARMA-CONTINUUM%F{220} Initiative Plugin Manager (%F{33}zdharma-continuum/zinit%F{220})…%f"
    command mkdir -p "$HOME/.local/share/zinit" && command chmod g-rwX "$HOME/.local/share/zinit"
    command git clone https://github.com/zdharma-continuum/zinit "$HOME/.local/share/zinit/zinit.git" && \
        print -P "%F{33} %F{34}Installation successful.%f%b" || \
        print -P "%F{160} The clone has failed.%f%b"
fi

source "$HOME/.local/share/zinit/zinit.git/zinit.zsh"
autoload -Uz _zinit
(( ${+_comps} )) && _comps[zinit]=_zinit


# ----------------------------
# Zinit plugins
# ----------------------------
# シンタックスハイライト
zinit light zsh-users/zsh-syntax-highlighting

# 入力補完
zinit light zsh-users/zsh-autosuggestions


# ----------------------------
# Powerlevel10k
# ----------------------------
zinit ice depth=1
zinit light romkatv/powerlevel10k

# To customize prompt, run `p10k configure` or edit ~/.p10k.zsh.
[[ ! -f ~/.p10k.zsh ]] || source ~/.p10k.zsh
