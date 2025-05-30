# 鍛冶レシピ

鍛冶レシピの追加が行えます

`smithing(output, template, input, upgradeItem)`

| 引数の名前 | クラス | 説明 |
| ---- | :---: | ---- |
| output | Item | 出力されるアイテム |
| template | Item \|\| Tag | テンプレートのスロットに置くアイテム |
| input | Item \|\| Tag | アップグレードされるアイテム |
| upgradeItem | Item \|\| Tag| アップグレードに必要なアイテム |

```js
//鉄インゴットを黒色と組み合わせてネザライトにしてしまうレシピ
event.smithing("netherite_ingot",
  "netherite_upgrade_smithing_template",
  "#forge:ingots/iron",
  "#forge:dyes/black"
)
```
