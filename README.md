# でんでんモジメイト <small>(mojimate.js)</small>

![](mojimate_logo.png)

## これは何？

HTMLファイルの中で使われている表外漢字（常用漢字表に含まれない漢字）と人名用漢字をハイライトするだけのJavaScriptです。文章の校正用に使ってください。

### 常用漢字

> 常用漢字（じょうようかんじ）は、文部科学省文化審議会国語分科会の答申に基づき、「法令、公用文書、新聞、雑誌、放送など、一般の社会生活において、現代の国語を書き表す場合の漢字使用の目安」として内閣告示「常用漢字表」で示された現代日本語の漢字。現行の常用漢字表は、2010年（平成22年）11月30日に平成22年内閣告示第2号として告示され、2136字／4388音訓［2352音・2036訓］から成る。
>
> ――<small>[常用漢字 - Wikipedia](http://ja.wikipedia.org/wiki/%E5%B8%B8%E7%94%A8%E6%BC%A2%E5%AD%97)</small>

### 人名用漢字

> 人名用漢字（じんめいようかんじ）は、日本における戸籍に子の名として記載できる漢字のうち、常用漢字に含まれないものを言う。法務省により戸籍法施行規則別表第二（「漢字の表」）として指定されている。
>
> ――<small>[人名用漢字 - Wikipedia](http://ja.wikipedia.org/wiki/%E4%BA%BA%E5%90%8D%E7%94%A8%E6%BC%A2%E5%AD%97)</small>

### その他

表外漢字であっても、共同通信社記者ハンドブック(第12版)で使うとされた漢字を専用の色でハイライトします。

## 使い方

HTMLファイルの `<head>` の中に次のように記述します。

    <script type="text/javascript" src="path/to/mojimate.js"></script>

または、Githubページにホストされたスクリプトを読み込んでもいける。

     <script type="text/javascript" src="http://denshoch.github.io/mojimate.js/mojimate.js"></script>

テキストに含まれる漢字が次のようにハイライトされます。

* <span style="background-color:#00FFFF;">表外漢字</span>（水色）
* <span style="background-color:#FF99CC;">人名用漢字</span>（ピンク）
* <span style="background-color:#FFFF00;">記者ハンドブックで使うとされた表外漢字</span>（黄色）

## ハイライトされた漢字があったらどうする？

常用漢字と人名用漢字は、あくまでも漢字使用の目安に過ぎません。各自の事情に応じて判断してください。ここで示す対応例についても同様です。

### 表外漢字への対応例

* 表外漢字を使わずひらがなで表記する

        炙る →　あぶる

* 表外漢字を常用漢字を用いた表記に改める

        嚢 → 袋

* 表外漢字に読み仮名をふる。

        茫然 → 茫然（ぼうぜん）

### 人名用漢字への対応例

* 人名に使われている場合を除き、表外漢字と同様の対応を行う
* 人名用漢字はそのまま使う（共同通信社記者ハンドブックはこちらの方針）

## 制限事項

現時点では Unicode における次の漢字を対象としています。

* Unified Repertoire and Ordering (CJK統合漢字)
* 拡張漢字A集合

次の集合に含まれる漢字を検出できません。

* 拡張漢字B集合
* 拡張漢字C集合
* 拡張漢字D集合  

## LICENSE

This library is distribuetd under the term of the MIT License. See MIT-LICENSE file for more info.
