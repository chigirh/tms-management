# 開発方法

## 概要
以下を定める

- プログラミングローカル開発環境
- 外部リソース（DBなど）のローカル開発環境
- ブランチ戦略

## 決定

### Java

|要素|利用するもの|バージョン|
|:---|:---|:---|
|IDE|IntelliJ|そのときの最新|
|JDK|java11を利用？|11|
|静的解析|Githubと連動できるSaaSを利用|-|
|ビルドシステム|Gradle|5系|

### Node.js 


|要素|利用するもの|バージョン|備考|
|:---|:---|:---|:---|
|IDE|VSCode|そのときの最新||
|Node|言語|12.X.X||
|静的解析|Githubと連動できるSaaSを利用|-||
|依存関係解決|npm|||
|バンドルツール|webpack||FWによるかも|
|トランスパイラ|babel||FWによるかも|


### 外部リソース

- Docker
- DockerCompose

### ブランチ戦略
シンプルなので [GitHub Flow](https://www.atmarkit.co.jp/ait/articles/1708/01/news015.html)

