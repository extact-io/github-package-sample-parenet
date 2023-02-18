# github-package-sample-parent
> 豆蔵デベロッパーサイトのブログ記事で利用しているサンプルアプリ

## 利用している記事
- [GitHub Packages - MavenとActionsを使ったオレオレ依存ライブラリの管理](https://developer.mamezou-tech.com/blogs/2023/02/19/github-packages-with-maven/)


## contents

|リポジトリ名|用途|
|-----------|---|
|[sample-parent-pom](extact-io/github-packages-sample-parent-pom)|プロジェクトの親pomを格納するリポジトリ|
|[sample-console](extact-io/github-packages-sample-console)|sample-console.jarのコードを格納するリポジトリ|
|[sample-service](extact-io/github-packages-sample-service)|sample-service.jarのコードを格納するリポジトリ|
|[sample-registry](extact-io/github-packages-sample-registry)|パッケージレジストリとして利用するリポジトリ|


## ビルドと実行
サンプルアプリのビルドにはDocker環境とMavenが必要です

### リポジトリのclone
``` shell
# Clone this repository
git clone https://github.com/extact-io/docker-with-maven.git
```

### コンテナイメージのビルド
``` shell
cd hello-server
mvn clean package docker:build
```

### コンテナを起動したテストの実行
``` shell
cd app-client
mvn clean verify
```

