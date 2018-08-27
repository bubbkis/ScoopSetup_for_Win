# Scoop によるWindows環境セットアップ

## Scoop buckets 一覧

- https://github.com/lukesampson/scoop/tree/master/bucket
- https://github.com/lukesampson/scoop-extras
- https://github.com/tapanchandra/awesome-scoop
- https://github.com/Ash258/scoop-Ash258
- https://github.com/oltolm/scoop-nonportable

## Scoop のインストール
PowerShellを起動し、以下を実行

```
Set-ExecutionPolicy RemoteSigned -scope CurrentUser
iex (new-object net.webclient).downloadstring('https://get.scoop.sh')
```

### インストール先の指定方法
環境変数 SCOOPとSCOOP_GLOBAL (AllUsers用)を設定してください。
デフォルトでは以下になります。

```
SCOOP = C:\Users\<ユーザー名>\scoop
SCOOP_GLOBAL = C:\ProgramData\scoop
```

変更する場合は、
管理者権限でプロンプトを起動し、以下を実行
以下、例です。

```
setx SCOOP d:\scoop\%USERNAME%
setx SCOOP_GLOBAL d:\scoop\global /m
```

環境変数を設定したら、上記Scoopのインストールを実行してください。


## アプリの一括インストールスクリプトを実行
setup.ps1内の
sudo scoop install ***** -g
は全ユーザー共通用のグローバルインストールになります。

コマンドプロンプトを起動し、以下を実行

```
powershell -ExecutionPolicy RemoteSigned -File C:\Users\<ユーザー名>\ScoopSetup_for_Win\setup.ps1
```

