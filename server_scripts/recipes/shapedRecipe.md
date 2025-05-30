# 定型レシピ

特定の配置でアイテムを置くことでアイテムを作るレシピを追加します。

`shaped(output, recipeShape, shapeItemID)`

| 引数の名前 | クラス | 説明 |
| ---- | :---: | ---- |
| output | Item | 出力されるアイテム |
| recipeShape | Array<Item> | レシピの形を模した配列 |
| shapeItemID | Item \|\| Tag | shapeに対応するID | 

```js
//SAMPLECODE IS HERE!
//石を土で囲むことで3個のダイヤモンドが作られるレシピ
event.shaped("3x diamond",[
  "DDD",
  "DSD",
  "DDD"
], {
    D: "dirt",
    S: "#minecraft:stones"
  })
```

