<sub>[READMEへ](../../README.md)</sub>

[日本語](./gpsr_ja.md) | [English](./gpsr_en.md)

# General Purpose Service Robot - GPSR

参考動画: https://www.youtube.com/watch?v=Ef1RzF9Wj9U

> [!WARNING]
> この動画は参考動画であり，RoboCup@Home JapanOpenのルールと異なる可能性がある．


## タスク説明 (Description)

ロボットは、幅広い能力が求められるコマンドを理解し，実行することを目標とする．


## フォーカス (Focus)

*タスクプラニング*，*物体・人検出と認識*，*物体の特徴認識*，*物体のマニピュレーション*


## セットアップ(Setup)

- **場所 (Locations)**:
  - **競技場所 (Task location)**: タスクは*Arena*内で行われるが，一部のコマンドではロボットが外に出ることがある．
  このタスクでは，*Arena*は通常の状態となる．
  - **開始位置 (Start Location)**: ロボットは*Setup Days*に発表される*事前定義された場所 (predefined location)*から開始する．
  `TC`から*開始合図 (start signal)*が出る際に，ロボットは*Instruction Location*に向かって移動する．
  - **指示位置 (Instruction Location)**: 競技の開始時，および1番目と2番目のコマンドの終了後，ロボットは*Instruction Location*に移動する．
  この*Instruction Location*は*Setup Days*に発表される．
- **人物 (People)**:
  - **ホスト (Host)**: ホストは`TC`から与えられたコマンドをロボットに指示する．
  ホストは競技チームから選ばれる．
  - **ゲスト (Guests)**: ゲストはジェスチャーや他の手段を通じてロボットとインタラクションする．
  最大で3人のゲストが*Arena*内にいる．


## 手順 (Procedure)

1. **開始フェーズ (Start Phase)**

    1. **競技時間 (Task Time)**: 制限時間は**10分**とする．

    1. **セットアップ (Setup)**: TCはチームにロボットを*Start Location*に移動するよう指示する．

    1. **カテゴリ選択 (Category Selection)**: チームは選択したカテゴリを`TC`に伝える．
    カテゴリによって，`TC`は任意のコマンドを選び，ホストに与える．
      - **DEMカテゴリ**: 事前に定義された文章構成による指示．
      - **通常カテゴリ**: [Command Generator](https://github.com/RoboCupAtHomeJP/CommandGenerator/tree/rcj24_for_opl)から生成された指示．

    1. **開始 (Start)**: TCが*開始合図(start signal)*を出し，タイマーを開始する．
    チームはセットアップを完了させ（スタートボタンを押すなど），エリアを離れる．
    2つ以上のボタンを押すなどの複雑なセットアップ手順は許可されない．

    1. **目的 (Goal)**: ロボットはコマンドフェーズとサービスフェーズを3回行う．

1. **コマンドフェーズ (Command Phase)**

    1. **ホストへの移動 (Navigation to Operator)**: ロボットは*Instruction Location*へ移動する．

    1. **ロボットへの指示 (Instruct the Robot)**: ホストは与えられたタスクをロボットに指示する．
    ロボットが名前や好きな飲み物を理解できない場合，ロボットはゲストに指示を繰り返すように要求することができ，ペナルティを付与しない．

1. **サービスフェーズ (Service Phase)**

    1. **コマンド確認 (Command Confirmation)**: コマンドを受け取った後，ロボットはタスクを実行する前にコマンドを確認する．

    1. **コマンド実行 (Command Execution)**: ロボットは指示に従ってタスクを実行する．


## その他のルールと注意事項 (Additional Rules and Remarks)

### コマンドのスキップ (Skipping Commands)

ロボットは`コマンドフェーズ`と`サービスフェーズ`を3回行う．
ただし，ロボットがホストから与えられたコマンドを誤認識した場合，競技チームは次のコマンドにスキップすることができる．
ロボットが誤認識したことを示すためには，ロボットは間違ったタスクを完了させ，ホストの位置に戻って，次のコマンドを要求する必要がある．

> [!WARNING]
> チームはこのルールを悪用して，希望のコマンドが与えられるまでコマンドをスキップすることはできない．

### コマンドジェネレータ (Command Generator)

コマンドは，[Command Generator](https://github.com/RoboCupAtHomeJP/CommandGenerator/tree/rcj24_for_opl)から生成される．
TCは環境に応じて事前にコマンドを任意に生成し，コマンドの正確さを確認する．

競技チームが*DEMカテゴリ*を選択した場合，公平性を保ちつつ，与えられるコマンドはあらかじめ準備され，[DEMカテゴリの文章構成]()に基づく．


## デウス・エクス・マキナ (Deus Ex Machina)

競技実行中に*デウス・エクス・マキナ*が*一般ルール*にリストされている項目から，ポイントが減点される．
その重複は最大で10倍までとする．

例えば: 
- 代替のHRIを使用して音声認識を飛ばす
- タスクを達成するために人間の支援を受ける

また，*DEMカテゴリ*を選択することで、*通常カテゴリ*の難易度を下げることができる．
ただし，[カテゴリごとの重み](#カテゴリごとの加重-weights-per-category)で定義された重みに基づき，与えられたスコアに減点される．


## リスタート (Restart)

リスタートは段階に応じて以下のように取り扱う．
なお，リスタートした場合，ロボットはスタート地点からタスクを再開する．
Step 1を完了している場合，リスタート後に直前のタスクを継続してもよい．
この場合，コマンドの理解やタスクの実行を繰り返してもよく，一度獲得した得点が減点されることはない
ただしペナルティとして，リスタート直後に獲得した点数は半減される．

先の条件に当てはまらない場合は，以下の手順が適応される．
- $n(\le 2)$回目のコマンドの理解の途中
  - 次のコマンドを$n$回目のコマンドとして再開する．
- $n$回目のStep 1の途中（目的地点への移動が完了していない場合，次のStepへ移る準備ができていない）
  - 次のコマンドを$n$回目のコマンドとして再開する．
- $n'(\le 3)$回目のStep 1完了後
  - $n'$回目のコマンドを$n'$回目のコマンドとして続きから再開して良い．

> [!NOTE]
> 物体を把持している場合，その取り扱いはチームに委ねる．


## コマンドカテゴリ (Command Category)

### DEMカテゴリの文章構成 (DEM Category Sentence Structure)

| タスク | 文章構成 |
| --- | --- |
| **Manipulation** <br>grasp, give\|place            | &bullet; Go to the `$ROOM`, grasp the `$OBJECT` on the `$PLACE` and place it on the `$PLACE`. <br>&bullet; Go to the `$ROOM`, grasp the `$OBJECT` on the `$PLACE` and give it to `$PERSON`. |
| **Vision (Enumeration)** <br>count (obj \| people) | &bullet; Tell me how many `$CATEGORY_OBJ` there are on the `$PLACE`. <br>&bullet; Tell me how many people in the `$ROOM` are `$POSE/GESTURE`. |
| **Vision (Description)** <br>find (obj \| person)  | &bullet; Tell me what is the `$OBJ_COMP` object on the `$PLACE`. <br>&bullet; Tell me the `$PERS_INFO` of the person at the `$PLACE` |
| **Navigation** <br>follow, guide                   | &bullet; Go to the `$ROOM`, find `$POSE/GESTURE` person and follow (him \| her). <br>&bullet; Go to the `$ROOM`, find `$POSE/GESTURE` person and guide (him\|her) to the `$ROOM`. |
| **Speech** <br>answer, tell                        | &bullet; Go to the `$ROOM`, find `$PERSON` at the `$PLACE` and answer (his \| her) question. <br>&bullet; Go to the `$ROOM`, find the person who is `$POSE/GESTURE` and tell (him \| her) `$TELL_LIST`. |
<!-- | **Speech** <br>answer, ask                         | &bullet; Go to the `$ROOM`, find `$PERSON` at the `$PLACE` and answer (his \| her) question. <br>&bullet; Go to the `$ROOM`, find `$PERSON` at the `$PLACE` and ask (him \| her) `$QUESTION`. | -->

> [!NOTE]
> `$POSE/GESTURE`, `$OBJ_COMP`, `PERS_INFO`, `QUESTION_LIST` と `$TELL_LIST` はTLMやDiscordを通して決定する．

> [!IMPORTANT]
> RCJ2024 OPL中では`greetNameInRm` と `greetClothDscInRm` というコマンドを抽選しない．

### タスクごとのStep一覧 (Steps per Task)

| タスク | Step 1 | Step 2 | Step 3 | Step 4 |
| --- | --- | --- | --- | --- |
| **Manipulation**         | 物体の前へ移動する | 物体を把持する               | (配置場所 \| 人の前)へ移動する | 物体を(配置 \| 手渡し)する |
| **Vision (Enumeration)** | 指定位置へ移動する | 対象の(物体 \| 人)を数える   | ホストの前へする               | 観測結果を報告する |
| **Vision (Description)** | 指定位置へ移動する | 対象の(物体 \| 人)を検出する | ホストの前へ移動する           | 観測結果を報告する |
| **Navigation**           | 人の前へ移動する   | 人を(追従 \| 誘導)する       | (追従 \| 誘導)先へ移動する     | (追従終了を認識 \| 誘導終了を報告)する |
| **Speech (Answer)**      | 人の前へ移動する   | 人に質問を要求する           | 人にその質問を答える           | ホストの前へ移動する |
| **Speech (Tell)**        | 指定位置へ移動する | 対象の人を検出する           | 情報をゲストに提供する         | ホストの前へ移動する |
<!-- | **Speech (Ask)**         | 人の前へ移動する   | 与えられた質問を人に質問する | ホストの前へ移動する           | 質問の答えを報告する | -->

### カテゴリごとの重み (Weights per Category)

| カテゴリ | $Weight$ |
| -------- | ------ |
| DEM | 0.5 |
| 通常 | 1 |


## スコアシート (Score Sheet)

ロボットが実行するタスクを4つのStepsに分け，1 Stepごとに採点する．
$Weight$ の変数は[カテゴリごとの重み](#カテゴリごとの重み-weights-per-category)に定義されている．

| アクション (Action) | スコア (Score) |
| --- | --- |
| **メインタスク (Main Task)**                            |  |
| &emsp; - 命令を理解する | $3 \times 20$                 | $3 \times 20$ |
| &emsp; - 1回目の命令タスクを実行する                    | $(15 \times 4) \times Weight$ |
| &emsp; - 2回目の命令タスクを実行する                    | $(30 \times 4) \times Weight$ |
| &emsp; - 3回目の命令タスクを実行する                    | $(60 \times 4) \times Weight$ |
| &emsp; - 全てのコマンドを実行した後*Arena*から退出する  | $20$ |
| ***デウス・エクス・マキナ (Deus Ex Machina)***                        |  |
| &emsp; - 代替手段を用いて命令を理解する                               | $3 \times -10$ |
| &emsp; - $h (\le 10)$ 回の人間の支援により1回目の命令タスクを実行する | $-6h \times Weight$ |
| &emsp; - $h$ 回の人間の支援により2回目の命令タスクを実行する          | $-12h \times Weight$ |
| &emsp; - $h$ 回の人間の支援により3回目の命令タスクを実行する          | $-24h \times Weight$ |
| **ペナルティ (Penalty)**                                |  |
| &emsp; - リスタート                                     | $直後に獲得した点数  \times 0.5$| 
| &emsp; - 不参加（無断）                                 | $-500$ |
| **合計**                                                | $500$ |

**得点係用のスコアシート**: [GPSR-score_sheet](./doc/RCJ2024_OPL_GPSR-score_sheet.pdf)


## 指示 (Instructions)

### ボランティアへ (To Volunteer)

ボランティアは競技チームによって自由に選ばれ，以下のタスクを行う． 

- `ゲスト`と`ホスト`の役するボランティアを選ぶ．
- 競技が始まる**30分前**に集まる．
- ゲストの情報についての指示を受ける．
- ゲストはロボットからの指示に従い，自分自身で行動しないでください．

> [!WARNING]
> ゲストに関する情報は競技チームと共有してはいけない．
そのような行為はペナルティの付加や競技の失格につながる可能性がある．

> [!NOTE]
> ボランティアできる人数が足りない場合，
他チームからの支援をお願いする場合がある．

### 得点係へ (To Scorer)

得点係は*General Rules*の[採点方法](./gr_ja.md#採点方法scoring-system)に定義されているように選ばれ，以下のタスクを行う．

- 競技が始まる**30分**前に集まる．
- スコアシートの情報についての指示を受ける．
- 競技チームの競技をスコアリングする．
- 他の得点係とTCとスコアを確認し合う．
- スコアシートをTCに提出する．

> [!WARNING]
> ゲストに関する情報は競技チームと共有してはいけない．
そのような行為はペナルティの付加や競技の失格につながる可能性がある．

### TCへ (To TC)

- *Setup Days*中:
   - *Start Location*を発表する．
   - *Instruction Location*を発表する．
   - 物体，カテゴリ，場所の位置を発表する．
   - 名前と飲み物のリストを発表する．
- 競技前:
   - 競技チームによって選ばれたゲスト役のボランティアを確認する．
   - ボランティアに名前を割り当てる．
   - 競技チームが使用する*Command Category*を確認する.
   - コマンドに応じて，*Arena*の工夫をする．
- 競技中:
   - ホストにコマンドを伝える．
