# 不定形レシピ

どこに配置しても大丈夫なレシピ(きのこシチュー等)を追加する関数

`shapeless(output, inputs)`

| 引数の名前 | クラス | 説明 |
| ---- | :---: | ---- |
| output | Item | 出力されるアイテム(64個まで) |
| inputs | Array<Item> | 入力アイテムのリスト(合計して9個まで) |

```js
//SAMPLECODE IS HERE!!!

//3個の火薬と1本の骨で3個のTNTを作るレシピ
event.shapeless("3x tnt", [
    "bone",
    "3x gunpowder"
  ]
)
```
