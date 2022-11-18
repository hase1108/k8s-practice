# git環境構築

## git初期設定

gitは基本的に最初から入っている

以下の初期設定をする
```bash
# wsl
git config --global user.name "haseesah"
git config --global user.email "hase1108shoiti@yahoo.co.jp"
```

GCMのセットアップを行ってホストマシンのwindows側で設定されている認証情報を利用する
参考
https://learn.microsoft.com/ja-jp/windows/wsl/tutorials/wsl-git#git-credential-manager-setup
https://zenn.dev/ttani/articles/wsl2-git-credential-manager

windows側でGCMのセットアップ後以下実行
```bash
# wsl
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/libexec/git-core/git-credential-manager.exe"
```

## wslのbashにgitのbranch名を表示する

~/.bashrcに以下を追記

```bash
sudo vim ~/.bashrc

# 以下追記
PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]$(__git_ps1)\$ '
# 保存

source ~/.bashrc
```

ポイントは``$(__git_ps1)``
