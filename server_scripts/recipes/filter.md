# Filter
大体どこでも使えるフィルターの概念を解説する

レシピの消去やら置換のお供にどうぞ

> [!NOTE]
> input/outputフィルタだけはタグも使用できます。(IDに`#`を付けるのを忘れずに)

| フィルタ名 | フィルタの記法 | 説明 |
| --- | --- | --- |
| input | `{input: "<INPUT_ITEM_ID>"}` | このアイテムを必要とする全レシピ |
| output | `{output: "<OUTPUT_ITEM_ID>"}` | 出力されるアイテムのIDに適合する全レシピ |
| mod | `{mod : "<MOD_ID>"}` | MOD_IDに一致する全レシピ |
| id | `{id: "<RECIPE_ID>"}` | 単一のレシピIDに一致する単一のレシピ |
| type| `{type: "<RECIPE_TYPE_ID>"}` | このレシピタイプに合致する全レシピ |
| and| `{filterA: "<ID>", filterB: <ID>}` | filterAとfilterBのどちらにも合致する全レシピ |
| or| `[{filterA: "<ID>"}, {filterB: <ID>}]` | filterAとfilterBのどちらかに合致する全レシピ |
| not| `{not: {filterA: "<ID>"}}` | filterAに合致しない全レシピ |

念の為のサンプルコード君
```js
//SAMPLE_CODE_IS_HERE!!!

//鉄インゴットのタグが付いているレシピを全て消去する
event.remove({input: "#forge:ingots/iron"})

//石のツルハシのレシピが全て消去される
event.remove({ output: "stone_pickaxe" })

//色を作るレシピを消す
event.remove({ output: "#minecraft:dyes" }) 

//Mekanismから全レシピを消去
event.remove({ mod: "mekanism" })

//グロウストーンダストを固めてグロウストーンを作成するレシピを指定して消去
event.remove({ id: "glowstone" })

//かまどのレシピを全て消去
event.remove({ type: "smelting" })

//AND: かまどから鉄を得るレシピのみを消去する
event.remove({ output: "iron_ingot", type: "smelting" })

//OR: 板材を作る/使用するレシピ全てを削除
event.remove([{ input: "#minecraft:planks" }, { output: "#minecraft:planks" }])

//NOT: Minecraf"ではない"アイテム全てを削除
event.remove({ not: { mod: "minecraft" } })
```
