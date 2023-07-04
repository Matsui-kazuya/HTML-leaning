# テスト用に作成しました

おそらくトップ画面を作るようだから、それを作ってみる
ついでに色々やってみる

## 改修しやすくするには？

### １　classを使う
　個別にインラインで書く内容はできるだけ少なくし、共通のスタイルをまとめて記載して、これを使用する

#### メリット
複数の要素を一括で修正、編集できる
機能ごとに分けると修正もしやすそう？(大きさ・枠線・背景色とか？)

#### デメリット
書き換えたいもの、書き換えたくないものが混在していた時のことを考えると面倒な気もする
　→今後のことを考えた設計にすることでできる？
　　→それをやろうとすると結局１つ１つわかれたりしない？
機能別に要素が多すぎてごちゃごちゃしそう


### 2　名前のフォーマットを決める
共通のスタイルや名称は名前のフォーマットを作成する
例えば、`.[機能名]_[詳細な内容]`とか

```
　border_solid　　　→境界線が実線
　backglound_blue　→背景が青色
```

現状は上記のルールで記載している
container、box、枠線、背景色それぞれで分けている
boxなどはmargin→paddingの順でm〇p〇のように記載

#### メリット
内容を見なくてもわかる

#### デメリット
名前の形式をあいまいなままにしておくと複数のフォーマットが混在するような書き方になってしまう


## メモ
HTML上でもCSSやJavascriptは使用できる
できる限りClassで記載を行い、特定のものだけをCSSで行う
```
<body>
  HTMLの記載


<style>
  CSSの記載
</style>

<script>
  javascriptの記載
</script>

</body>
```