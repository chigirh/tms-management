# TrainingManagementSystem - 管理プロジェクト

## このプロジェクトは？
TrainingManagementSystem の開発の管理を行うプロジェクト。  
フルリモートのアジャイルライクな開発を行うため、タスクはIssueをベースとして管理する。  
あくまでも業務ではないのでタスクの見える化とか管理の容易性を上げるため、[ZenHub](https://github.com/SE-Garden/tms-management/edit/master/README.md#workspaces/tms-management-5cc2c43736b4b64850a0b79b/board?repos=183573990) を利用する。

## 開発方針

### ドキュメンテーションの割愛
今回はドキュメンテーションを極限まで割愛する。  
あくまでも、コーディング関連の開発力を高めることを目的とする。  
ただし、ドキュメンテーションがなくて開発を行うということは、ドキュメンテーションを行って開発するよりも割と難しい。

### やり取りを残しておく
ドキュメンテーションは行わないけれど、なぜこうしたのか？といったような経緯は残すべき。  
その経緯を表す文章なり資料なりが設計的な内容を含んでいても問題ない。  
それは意識合わせに必要だったから作ったと考える。

残す方法は、[Architecture Decision Record](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions)を採用する。  
アーキテクチャに該当すること以外にも方法を統一的にする。（簡易化のため）

#### adr-toolsのインストール
ADRを残すための支援ツールとして、[adr-tools](https://github.com/npryce/adr-tools) が提供されている。  
[インストール手順](https://github.com/npryce/adr-tools/blob/master/INSTALL.md) を参考にしてインストールする。  
Mac / Windows10 / Linux に対応しているので普通の人は大丈夫だと思う。  

#### 流れのイメージ
1. タスクを持った人間が、ADRを作成する。コマンドは `adr new some title` 
1. 自分の考え等を書いて、どうよ？Slackで投げかける
1. 反応できる人間で一通り反応　→　決着
1. ADRを更新（タスクを持った人間が必須ではないが、基本そうなるはず）
