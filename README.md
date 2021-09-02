# Docker Introduction
["docker_try"](https://github.com/jin237/docker_try) is the repository for Docker Introduction.
<br>


## Refereces
- [x] [Docker超入門①〜Dockerってなに？〜【初心者向け】<br>https://datawokagaku.com/whatisdocker/](https://datawokagaku.com/whatisdocker/)
- [x] [Docker超入門②〜Dockerってなに？〜【初心者向け】<br>https://datawokagaku.com/startdocker/](https://datawokagaku.com/startdocker/)
- [x] [Docker超入門③〜Dockerってなに？〜【初心者向け】<br>https://datawokagaku.com/howtouse_container/](https://datawokagaku.com/howtouse_container/)
- [ ] [Docker超入門④〜Dockerってなに？〜【初心者向け】<br>https://datawokagaku.com/container_commit_upload/](https://datawokagaku.com/container_commit_upload/)
- [ ] [Docker超入門⑤〜Dockerってなに？〜【初心者向け】<br>https://datawokagaku.com/howtousedockerfile/](https://datawokagaku.com/howtousedockerfile/)
- [ ] [Docker超入門⑥〜Dockerってなに？〜【初心者向け】<br>https://datawokagaku.com/dockerbasicflow/](https://datawokagaku.com/dockerbasicflow/)
- [ ] [Docker超入門⑦〜Dockerってなに？〜【初心者向け】<br>https://datawokagaku.com/dockerfile_commands/](https://datawokagaku.com/dockerfile_commands/)
<br>


## Memo & Note

Each terminal command charts

### ログイン
```
$ docker login
```

### Pullする
```
$ docker pull {IMAGE_NAME:TAG_NAME}
```

### Docker imageのリストの確認
```
$ docker images 
```

### コンテナに入る 
```
// すでにあるコンテナに入る
$ docker exec {CONTAINER_NAME}

// 動いているコンテナに入る
$docker exec -it {CONTAINER_NAME} bash
```

### Runの一覧
```
// imageからコンテナを作る
$ docker run {IMAGE_NAME}

// imageからコンテナを作ってから入る 
$ docker run -it {IMAGE_NAME:TAG_NAME} bash

// すでにあるコンテナを指定してrun
$ docker run --name {CONTAINER_NAME} -it {IMAGE_NAME:TAG_NAME} bash
```

### コンテナの確認
```
$ docker ps -a
```

### ファイルの作成
```
touch {FILE_NAME}
```

### コンテナから出る
```
// 完全に出る
$ exit

// 「コンテナを動かしたままにしたい」「止めたくない」という場合
command + p + q
(コマンドでなく、ショートカット)
```

### リスタート
```
$ docker restart {CONTAINER_NAME or ID}
```

### コミット
```
$ docker commit {CONTAINER_NAME or ID} {NEW_Docker_image_NAME}
```



## windowsでのdocker環境構築


https://hub.docker.com/signup
でIDというかアカウントを作成orサインイン

https://docs.docker.com/desktop/windows/install/
で，Docker Desktop for Windowsをインストール

ダウンロードしたパッケージ：Docker Desktop Installer.exeで実行

configurationは２つともチェックした状態で，Okを押す．
ダウンロードが始まる（Docker Desktop 4.0.0）

終わったらclose and log outを押す．再起動する．

Our Service Agreement has Changedっていうものが出てくるので，acceptする．

この状態でDockerが立ち上がると，WSL2のインストールができてないので，エラーが起こる．
（WLS 2 installation is incomplete.）

この状態で一度docker desktopは閉じる
cmdを開いて，

docker -v
Docker version 20.10.8, build 3967b7d

みたいなのが出てくる．

docker-compose -v
docker-compose version 1.20.1, build 5d8c71b2

再度，docker desktopを開く．
そこでサインインを行う．

そこでおそらく，fail to start になる．

上のsettingsを開き，use the WSL 2 based eigine
のチェックを外す．
そのまま，右下のApply & Restartを押す．
そのままチュートリアルを行う．

この時，clone build run shareの順を覚えておくとよい

docker run するときにアクセス許可はしてね

完了したらdone

https://hub.docker.com/repositories
ここにアクセスしてみるとそこでできたリポジトリが反映される．

WSLの環境設定
＝wsl --installをコマンドで使えるようにする
[Windows Insider Program](https://docs.microsoft.com/ja-jp/windows/wsl/install-win10#:~:text=%E3%81%8C%E3%81%82%E3%82%8A%E3%81%BE%E3%81%99%E3%80%82-,Windows%20Insider%20Program,-%E3%81%AB%E5%8F%82%E5%8A%A0%E3%81%99%E3%82%8B)にアクセス
1. resister
2. flight
3. give feedbackをそれぞれしっかりと行う

2.flightから

install on your indivisual deviceのpreparationについて

To install Windows Insider Preview Builds, you must be running a licensed version of Windows on your device. You can install Windows here if your device is currently running an older version or if you need to buy Windows. If you're having issues installing Windows, you can also download a Windows Insider Preview ISO to get started.
->windows 10であればいらない

The process of setting up flighting restarts your device during program setup and updating. Make sure you're ready for this, so you don't lose open documents or unsaved work. You might also want to take a picture of these directions or bookmark this page on your browser to get back to it easily.
-> 作業中のものは保存して閉じておく


Installation

[Settings > Update & Security > Windows Insider Program](ms-settings:windowsinsider)を開く．そしたら，スタートして，アカウントリンクを行う．＝自分のmicrosoft accountを選ぶ．

Insider previewを選択：Dev channel















