# [《MHS 学习笔记》] > [《Homebrew 学习》] (mhs2019.5.6)

- [安装]

## <span id="install">安装</span>
```
$ cd ~
$ curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install >> brew_install
$ vi brew_install
> # BREW_REPO = "https://github.com/Homebrew/brew".freeze
> BREW_REPO = "git://mirrors.ustc.edu.cn/brew.git".freeze
$ /usr/bin/ruby brew_install
$ cd "$(brew --repo)"
$ git config -l
$ git remote set-url origin https://mirrors.ustc.edu.cn/brew.git
$ cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
$ git config -l
$ git remote set-url origin https://mirrors.ustc.edu.cn/homebrew-core.git
$ brew update
$ echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles' >> ~/.bash_profile
$ source ~/.bash_profile
```


##
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"
[《Homebrew 学习》]: https://mhsnet.github.io/mhsstudynotes/tools/pkg-adm/brew/index.html "《Homebrew 学习》"

[安装]: https://mhsnet.github.io/mhsstudynotes/tools/pkg-adm/brew/index.html#install "安装"