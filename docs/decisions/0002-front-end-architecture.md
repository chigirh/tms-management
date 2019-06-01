# ソフトウェアアーキテクチャ（フロントエンド）

## 目的

フロントエンド側で使用されている技術要素を調査し、本開発で使用する技術を選定する。

## 調査事項

### JavaScript言語

フロントエンドのプログラミング言語としては、JavaScriptが有名であるが、  
独特な文法や動的型付けといった部分をカバーするAltJSと呼ばれるプログラミング言語がある。  
AltJSで実装したコードをコンパイルすることで、JavaScriptコードが生成される。

1. JavaScript(ECMAScript2018)
- AltJSではない、純粋なJavaScript。

2. TypeScript
- AltJSの一種。JavaScript技術者が回答したアンケート「[The State of JavaScript 2018](https://2018.stateofjs.com/javascript-flavors/overview/)」によると、
  AltJSの中で一番使用されている言語。
- 型の概念やクラス定義を使った処理を実装しやすい。
  型やクラスを使う他言語からだと、JavaScriptよりハードルは低そう。
- AltJSは、JavaScriptの記法とは異なるため、JavaScript習得者からすると、学習コストは増える。

### CSS

1. Sass
- AltCSSの一種。AltCSSの中では古参であり、[Googleトレンド検索](https://trends.google.co.jp/trends/explore?cat=31&date=today%205-y&q=CSS%20Sass,CSS%20Scss,CSS%20Less)でも、Scss/Lessと比べ人気。
- コンパイルにはRubyが必要で、記述もRubyライク。
- 条件分岐や繰り返しの制御も記述できるらしい。

2. Scss
- AltCSSの一種。Sassの派生。
- コンパイルにはRubyが必要だが、記述は従来のCSSライク。
- Sass同様、条件分岐や繰り返しの制御も記述できるらしい。

3. Less
- AltCSSの一種。Sass/Scssよりもシンプルな記述。
- Sass/Scssと違ってRubyも必要なく準備が簡単だが、
  人気や各種サポートツールの豊富さでは、Sass/Scssに劣る。

### パッケージマネージャ

1. npm
- Node.jsにデフォルトで入っているパッケージ管理ツール。
- JavaScriptのパッケージ管理ツールとしては古参であり、
  [Googleトレンド検索](https://trends.google.co.jp/trends/explore?cat=31&date=today%205-y&q=npm,yarn)では、Yarnと比べ人気度が高い。

2. Yarn
- 2016年にFacebook等から発表されたパッケージ管理ツール。
- ローカルキャッシュの使用など、npmと比べインストール速度が速いことが売り。

### ビルドツール

JavaScriptの世界では、実装したコードにブラウザが対応していないことがままあるようで、
ブラウザに対応した形式への変換を行うために、以下のツールが存在する。

- モジュール分割して実装したコードを結合する「モジュールバンドラ」
- 実装したコードをブラウザが対応するコードに変換する「トランスパイラ」

#### モジュールバンドラ

1. webpack
- モジュールバンドラの代表的な存在。
- 多機能で、[The State of JavaScript 2018](https://2018.stateofjs.com/other-tools/)によると、使用率もダントツ1位。

2. Parcel
- 2017年に発表されたモジュールバンドラ。
- webpackと比較し、設定ファイルを必要とせず、利用するハードルが低そう。
- 簡単に使える反面、機能面ではwebpackに劣る。

#### トランスパイラ

1. Babel
- トランスパイラの代表的な存在。
- 他のトランスパイラも検索したが見つからず、
  Babelがデファクトスタンダードのように思う。

### Webフロントエンドフレームワーク

1. React+Redux
- Facebook製のフレームワーク。
- [The State of JavaScript 2018](https://2018.stateofjs.com/front-end-frameworks/overview/)によると、使用率1位。
- ユーザーインタフェースの実装に特化している。
- 状態管理としては、Reduxを使うのがデファクトスタンダードらしい。
- 主な開発規模は、中～中大。
- 公式ページが日本語に対応。

2. Vue.js+Vuex
- 企業ではなくコミュニティ発のフレームワーク。
- [The State of JavaScript 2018](https://2018.stateofjs.com/front-end-frameworks/overview/)によると、使用率3位で他に劣るが、もう使いたくないという回答が少なく満足度は非常に高い。
- ユーザーインタフェースの実装に特化している。
- 状態管理としては、Vuexを使うのがデファクトスタンダードらしい。
- 主な開発規模は、小～中。
- 公式ページが日本語に対応。

3. Angular+ngrx
- Google製のフレームワーク。
- [The State of JavaScript 2018](https://2018.stateofjs.com/front-end-frameworks/overview/)によると、使用率2位だが、もう使いたくないという回答が多い。
- ルーティングを含め、Webアプリケーションを実装する機能がフルスタックで揃っている。
- 状態管理としては、ngrxを使うのがデファクトスタンダードらしい。
- 主な開発規模は、大。
- 公式ページが日本語に対応。

### コーディング規約

1. Google JavaScript Style Guide
- Googleによるコーディングスタイル。
- Closure LinterというGoogle製の文法チェッカーがある。

2. jQuery JavaScript Style Guide
- jQueryによるコーディングスタイル。

3. Airbnb JavaScript Style Guide
- AirBnBによるコーディングスタイル。
- Github上では人気らしい。

### 静的解析

1. ESLint
- [Googleトレンド検索](https://trends.google.co.jp/trends/explore?cat=31&date=today%205-y&q=ESLint,JSHint,JSLint)では、近年他２つと比べて人気度が高い。
- 設定ファイルはJSONかYAML形式で記載する。

2. JSHint
- 4、5年ほど前はJavaScriptの静的解析ツールとして、2強の片翼を担っていたツール。
- 設定ファイルはJSON形式で記載する。

3. JSLint
- 4、5年ほど前はJavaScriptの静的解析ツールとして、2強の片翼を担っていたツール。

### テストフレームワーク

1. Jest
- Facebook製のテストフレームワーク
- 急速な普及により、[The State of JavaScript 2018](https://2018.stateofjs.com/testing/overview/)では、Mocha、Jasmineを抜いて一番人気となっている。
- zero configや、テストに必要な機能が揃っている点が売り。
- 公式ページが一部日本語対応

2. Mocha+chai
- Jestに次いで人気のあるテストフレームワーク。
- Mochaはテストコードの実装規則、chaiはアサーションライブラリ。

3. Jasmine
- Mochaと違いアサーションからMockまで機能が揃っている、上記2つと比べると人気は落ちる。

## 結果

本開発のフロントエンド側で使用する、技術要素・アーキテクチャは、以下とする。

### JavaScript言語

- TypeScript
  - Java経験者であれば、JavaScriptよりも、オブジェクト指向の考え方で実装しやすいTypeScriptのほうが扱いやすい。
  - AltJSの中で今最も人気があるため、新鮮な情報を多く入手でき、問題解決もしやすい。

### CSS

- Sass
  - AltCSSの中で今最も人気があり、新鮮な情報を多く入手でき、問題解決しやすい。

### パッケージマネージャ

- npm
  - Yarnと比べても普及率が高く、学習時に情報を集めやすい。
  - 最近のアップデートで、速度面においてもYarnと互角の性能になりつつある。

### ビルドツール

#### モジュールバンドラ

- webpack
  - 普及率が高く情報も多いため、学習しやすい。
  - Parcelはwebpackと比べ登場から日が浅く、今後の伸び率もわからない。

#### トランスパイラ

- Babel
  - 代替のツールが見つからないが、フロントエンド業界でもデファクトスタンダードである。

### Webフロントエンドフレームワーク

- React+Redux
  - Vue.jsと比べ登場から時間が経っており、情報量やライブラリの数で優る。
  - 現在の使用率は最も高く、満足度も低くないため、今後も使われ続けそうである。
  - 開発規模も本開発とマッチしている。

### コーディング規約

- Google JavaScript Style Guide
  - 公式でチェックツールも用意されており、綺麗なコーディングが期待できる。

### 静的解析

- ESLint
  - 静的解析ツールの中で今最も人気があるため、設定方法などの情報を多く入手しやすい。

### テストフレームワーク

- Jest
  - アサーション、Mock、カバレッジと、テストに必要な機能を1つで賄えるため学習しやすい。
  - Facebook製のため、同じくFacebook製のReactとは相性が良いと思われる。
