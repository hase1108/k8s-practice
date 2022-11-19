# gcp設定

## プロジェクト作成

適当なIDでプロジェクト作成
``お支払い→予算とアラート``から予算に関するアラートを設定しておく

## gcloud SDKのインストール
参考: https://cloud.google.com/sdk/docs/install?hl=JA#deb

gcloud SDKはpython3.5-3.9だが、ubuntuにデフォルトで入っているのは3.10のため別途pythonをinstallする

```
$ sudo apt update
$ sudo apt install software-properties-common
$ sudo add-apt-repository ppa:deadsnakes/ppa
$ sudo apt install python3.9

.bashrcに追記
export CLOUDSDK_PYTHON=/usr/bin/python3.9
https://cloud.google.com/sdk/docs/install?hl=ja
DISPLAY=":0" gcloud auth login
```