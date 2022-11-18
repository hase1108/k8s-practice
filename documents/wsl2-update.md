# wsl2で稼働するubuntuのverアップ

## なにが変わる

wsl2で稼働するUbuntuのバージョンをLTSの新しいバージョンに上げた

20.04(lts) → 22.04(lts)

## 参考

https://zenn.dev/ryuu/articles/upgrade-ubuntu2204-wsl

## 実作業

```bash
# windows powershell起動

wsl #wsl起動

# 以降wsl内で実施

cat /etc/os-release #現在のバージョン確認
sudo apt update && sudo apt upgrade #パッケージのバージョン確認
sudo apt dist-upgrade && sudo apt install update-manager-core #アップグレード準備
sudo do-release-upgrade -d #アップグレード実施
```

### 気づいたこと

wslを再起動する場合は以下のコマンドを実行するといい

```bash
wsl.exe --shutdown
```
