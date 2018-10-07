# 概要
GoのプログラムをDockerコンテナ上で実行する

# 目的
Dockerが何をしているか？をコマンドを通じて学ぶ

# アプリケーション概要
このコードはサーバーアプリケーションとして動作する。
挙動としては
- どんなHTTPリクエストに対しても「Hello Docker!」とレスポンスを返す。
- 8080ポートでサーバーアプリケーションとして動作する。
- クライアントからリクエストを受けた際は、receives requestのログを標準出力に表示する。

# 導入の仕方
## projectのclone
```
git clone 
cd ~/cloneしたディレクトリ
```

## Dockerのbuildとrun
```
docker image build -t example/echo:latest .
docker container run -d -p 9000:8080 example/echo:latest
```

## 動作の確認
```
curl http://localhost:9000/
もしくは
http://localhost:9000/
にアクセス
```

## 詳細・まとめ
個人wiki  
https://sugawiki.herokuapp.com/5bb9a99a8b095d00044a6f90
