---
date: 2026-05-28
course: system_design
topic: UML
lecture_no:
period: "3"
instructor: 土屋
source: 授業
status: 未着手
confidence: "1"
assignment_status:
due:
repo:
tags:
  - 
  - 基本情報技術者試験
  - qualification_test_
aliases:
---

## 授業メモ
### UML
オブジェクト指向によるシステムの分析・設計・実装・テストに使用する設計図

|                    |                                         |                                                        |     |
| ------------------ | --------------------------------------- | ------------------------------------------------------ | --- |
| 静的構造図<br><br>構成を表す | クラス図                                    | クラス間の関連とクラス内の構造を表す                                     |     |
| オブジェクト図            | クラスを実体化したインスタンスの構造を表す                   |                                                        |     |
| パッケージ図             | クラスなどをグループ化し整理された関係を表現する                |                                                        |     |
| コンポーネント図           | サブシステムやモジュール間の構造・依存関係を、視覚的に理解したいときに使用する |                                                        |     |
| 複合構造図              | コンポーネントの内部構造ならびにコンポーネント間の依存関係を表す        |                                                        |     |
| 配置図                | コンポーネント間のインターフェイスを理解したいときに使用する          |                                                        |     |
| 動的振る舞い図            | アクティビティ図                                | 処理や制御を表す                                               |     |
| 動きを表す              | シーケンス図                                  | オブジェクト間のメッセージのやり取りを時系列で表す                              |     |
| 状態、時間の流れ           | 状態(ステート)マシン図                            | イベントにより引き起こされる 状態遷移を表す                                 |     |
|                    | ユースケース図                                 | システムの機能(振る舞い)をユーザの視点から表す                               |     |
|                    | タイミング図                                  | クラスやオブジェクトの状態遷移を時系列で表す                                 |     |
|                    | コミュニケーション図                              | オブジェクト間のメッセージやり取りを表す                                   |     |
|                    | 相互作用概要図                                 | ユースケース図やシーケンス図などが構成要素となっていて、各々がシステムからどのように、連携しているのかを表す |     |
#### 構成図
##### クラス図
クラス間の静的な相互関係を表現する構造図
![](data:image/emf;base64,R0lGODlhiwJ3AHcAMSH+GlNvZnR3YXJlOiBNaWNyb3NvZnQgT2ZmaWNlACH5BAEAAAAALAAAAABzAnYAhwAAAAAAAB0AAAAAHQAdHR0AHRwcHAEAAB4AHgEAHQEBAB4AAAEBHQEAHgAAMwAdMh0AMh0AMwEAMx0dNAAAMgEAMgAAMQEBMwAcSB0dSAAdSAEcRwEdSAAcRgAcRwEdRx0dSQAAqgAA/wAyMh00NAAzWh0zWgIzWQAzWwAyWgAyWAIzWgA0SAAwWB1JSQBVVR1GbB1GaB1Iah9Gah1EaB1GagCqqgD//zMAADIdADMAHTIAHTIAADQdHTIAMjMAMzQdNDQeRjQ0NDNdXTNbWzNZWzNZfzVbbjVZbDFZfTFXdzFZeTNbgEgdAEgcAEkdAEcdAEkdHUgdHVszAFozAEg0AFkzAFkzAkg0AVoyAEYzRkg1SElJHUhIHVtIHV1dM1tZM0REM11dXVtbW0hIW11dSFlZf0hZf0ZGblVVe11dbkhuW0ZsWVl/WVtuSFV7VVlsRl13d0huf0Rqe11/f1V7all/blVmZlVmd1V3d1Vqe1VublVud1luf0Rmd2xGHW5IHWpIHWxIHWpGH39dM39ZNXtZNW5bNW5GRn9uSH9/XXd3XXtqRG5uRG5uWX9uWX9zXXtqTGp3XWpqamZ3d3d3ZmZmZnd3d25ubn9mZm5ugG6AbmaIiIBbM4BdM4BzSIBuboiIZgECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwECAwj/AAMIHEiwoMGDCBMqXMiwocOHBgFInEixosWLGDNq3Mixo8ePEiGKHEmypEmRIFOqXMmypcuXMGPKZBlgps2bODMKzMmz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)

##### オブジェクト図
ある特定の時点でのオブジェクトのインスタンス間の静的な構造を記述する図

#### 振舞い図
##### ユースケース図
システムが提供する機能（システム）と利用者（アクタ）の関係を表現した図
要求分析でユーザの要件を特定し、ユーザと一緒に評価することができる
##### アクティビティ図
業務フローやプログラムのロジックをわかりやすく図にしたもの
作業の流れを整理、オブジェクトの振舞いの記述を行う
条件分岐や並行処理も表現可能
##### 




## 授業で出た単語
- 

## 授業中ミニ用語カード（1語30秒）
- [ ] #termcard 用語:  | 一言定義:  | 例:  | 重要: 試験/実務 | 転記先: [[ ]]

## 試験頻出・要復習
- 

## 実務での使いどころ
- 

## 授業後10分チェック
- [ ] #postclass E: 試験頻出を3つ以内に絞った
- [ ] #postclass Q: 疑問点を次回確認用に残した
- [ ] #postclass P: 実務で使える観点を1つ書いた
- [ ] #postclass T: 重要語だけ単語ノートへ転記した

