# docker-rpi-jenkins
RaspberryPi(64bit)にDockerでJenkinsを構築

## 環境
- kernel：Linux ホスト名 5.15.32-v8+ #1538 SMP PREEMPT Thu Mar 31 19:40:39 BST 2022 aarch64 GNU/Linux
- OS：Debian GNU/Linux 11 (bullseye)

## Dockerコマンド
```bash
# Docker-compose実行
$ docker-compose up -d

# Docker コンテナ確認
$ docker ps

# Docker イメージ確認
$ docker images

# Docker コンテナの中に入る
$ docker exec -it [コンテナID] /bin/sh

# dokcer-composeのリビルド
$ docker-compose up -d --build  --force-recreate

# dokcer-composeの一括削除（滅びの呪文）
$ docker-compose down --rmi all --volumes --remove-orphans
```

## ブラウザからアクセスして起動確認
下記URLからJenkinsに接続する
```js
http://localhost/jenkins/
```
下記コマンドでJenkinsの初回パスワードを確認する
```bash
$ docker exec -it [コンテナid]  cat /var/jenkins_home/secrets/initialAdminPassword
```

## 参考
- [weseek/docker-jenkinss](https://github.com/weseek/docker-jenkins/blob/master/README.md)
