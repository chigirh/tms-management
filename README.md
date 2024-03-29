# TrainingManagementSystem - 管理プロジェクト

## このプロジェクトは？
TrainingManagementSystem の開発の管理を行うプロジェクト。  
フルリモートのアジャイルライクな開発を行うため、タスクはIssueをベースとして管理する。 

## 開発方針

### タスク管理
業務ではないのでタスクの見える化とか管理の容易性を上げるため、[ZenHub](https://github.com/SE-Garden/tms-management/edit/master/README.md#workspaces/tms-management-5cc2c43736b4b64850a0b79b/board?repos=183573990) を利用する。  
[こちらのリンク](https://www.zenhub.com/extension) からChromeもしくはFireFoxの拡張機能を入れると便利に利用可能になる。

### ブランチ戦略
ブランチ戦略は [GitHub Flow](https://gist.github.com/Gab-km/3705015) を採用する。  
初期開発は変に難しいブランチ戦略にする必要性がない。  
結合試験以降はまた変更すると思う。

|ブランチ名|例|用途|
|:---|:---|:---|
|master|-|最新版、いつでもリリース可能なもの|
|topic|topic/name|作業ブランチ。IssueおよびZenHubのタスクと紐付くことが望ましい|

### ドキュメンテーションの割愛
今回はドキュメンテーションを極限まで割愛する。  
あくまでも、コーディング関連の開発力を高めることを目的とする。  
ただし、ドキュメンテーションがなくて開発を行うということは、ドキュメンテーションを行って開発するよりも割と難しい。

### 決定事項を残す
ドキュメンテーションは行わないけれど、なぜこうしたのか？といったような経緯は残すべき。  
その経緯を表す文章なり資料なりが設計的な内容を含んでいても問題ない。  
それは意識合わせに必要だったから作ったと考える。

残す方法は、[Architecture Decision Record](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions) を採用する。  Wikiは使わない。
アーキテクチャに該当すること以外にも方法を統一的にする。（簡易化のため）

#### adr-toolsのインストール
ADRを残すための支援ツールとして、[adr-tools](https://github.com/npryce/adr-tools) が提供されている。  
[インストール手順](https://github.com/npryce/adr-tools/blob/master/INSTALL.md) を参考にしてインストールする。  
Mac / Windows10 / Linux に対応しているので普通の人は大丈夫だと思う。  

#### 流れのイメージ
1. タスクを持った人間が、ADRを作成する。コマンドは「`adr new some title` 」 で####_some_titme.mdとかが作成される
1. 自分の考え等を書いて、どうよ？Slackで投げかける
1. 反応できる人間で一通り反応
1. 議論の後、決定
1. ADRを更新（タスクを持った人間が必須ではないが、基本そうなるはず）

## プロジェクト
現在Organizationには古いプロジェクトも残っている状態。  
紛らわしいので、一覧として分類しておく。

|リポジトリ名|新旧|用途|GitHubPages|
|:---|:--|:--|:--|
|tms|旧|開発リポジトリ。全部入りになってる|http://SE-Garden.github.io/tms|
|devlog|旧|開発ブログ。なんとなくやってた|http://SE-Garden.github.io/devlog|
|tms-management|新|開発管理プロジェクト。このリポジトリ。|-|

