# Use_docker

## Windows10環境でLinux(Ubuntu)環境を構築する

参考サイト

https://www.4peace.co.jp/tech/569/

こちらの内容を抜粋＆一部内容追加。

## 1. コマンドプロンプトの起動

管理者として実行をすると2-2でエラーを吐くことはない。スタート -> コマンドプロンプト -> 右クリックで「管理者として実行」

Macは知りません。

## 2. WSL（Windows Subsystem for Linux）のインストール

### 2-1 以下3つのコマンドを実行

#### (1) Linux用のWindowsサブシステムを有効にする

```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

#### (2) 仮想マシン機能を有効にする

```
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

#### (3) Linuxカーネル更新プログラムパッケージのインストール

https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msiをインストール

WSL2を規定バージョンとして設定

```
wsl --set-default-version 2
```

## 3 Microsoft StoreからUbuntuをインストール

内容省略

初回起動時、ユーザー名とパスワードを設定する必要がある。

## 4 軽い動作確認

### (1) LinuxからWindowsのファイルにアクセス

```
$ cd /mnt/c
```

### (2) pingでも打ってみる？

```
$ ping 8.8.8.8
```

```linux
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=116 time=10.5 ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=116 time=7.32 ms
64 bytes from 8.8.8.8: icmp_seq=3 ttl=116 time=6.92 ms
```

## Windows11環境でLinux(Ubuntu)環境を構築する

参考サイト

https://www.kagoya.jp/howto/cloud/container/wsl2_docker/

## 1. コマンドプロンプトの起動

内容省略

## 2. 以下コマンドを実行

```
wsl --install
```

おわり！(すご…)

## 3. Ubuntuのインストール

内容省略

<br\>

<br\>

## Docker Desktop for Windowsのインストール

Docker公式サイトにアクセスし、右上のGet Startedをクリック

https://www.docker.com/

Downloads for Windowsをクリックし、インストールを進める。



