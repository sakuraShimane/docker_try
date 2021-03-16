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







