<sub>[READMEへ](../../README.md)</sub>

[日本語](./gpsr_ja.md) | [English](./gpsr_en.md)

# General Purpose Service Robot - GPSR

参考動画: https://www.youtube.com/watch?v=Ef1RzF9Wj9U

> [!WARNING]
> これは参考用のサンプル動画です。
> その年のルールとはタスク内容が異なる場合があります。


## タスク説明 (Description)

ロボットは、幅広い能力が求められるコマンドを理解し，実行することを目標とする．

- **主な目標**: オペレーターから要求された3つのコマンドを実行する。

- **任意の目標**: デフォルトオペレーターからのコマンドを理解する。

## フォーカス (Focus)

タスクプラニング，物体・人検出と認識，物体の特徴認識，物体のマニピュレーション


## セットアップ(Setup)

- **場所 (Locations)**:
  - **競技場所 (Task location)**: タスクは*Arena*内で行われるが，コマンドによってはロボットが*Arena*外に出ることがある．
  このタスクでは，*Arena*は通常の状態となる．
  - **開始位置 (Start Location)**: ロボットは*Setup Days*に発表される事前定義された場所 (*predefined location*)から開始する．
  `TC`から開始合図 (*start signal*)が出る際に，ロボットは*Instruction Point*に向かって移動する．
  - **指示位置 (Instruction Point)**: 競技の開始時，および1番目と2番目のコマンドの終了後，ロボットは*Instruction Location*に移動する．
  この*Instruction Point*は*Setup Days*に発表される．
- **人物 (People)**:
  - **ホスト (Host)**: ホストは`TC`から与えられたコマンドをロボットに指示する．
  デフォルトホスト(*default host*)は`TC`のメンバとなる．
  しかし，内部ホスト(*internal host*)として，競技チーム内からメンバを選定することが可能である．
  その際，DEMスコアリングが適応される．
  - **ゲスト (Guests)**: ゲストはジェスチャーや他の手段を通じてロボットとインタラクションする．
  また，コマンドによって，*Arena*内のゲスト人数(1-5名)が変動する可能性がある．
  <!-- 最大で3人のゲストが*Arena*内にいる． -->


## 手順 (Procedure)

1. **開始フェーズ (Start Phase)**

    1. **競技時間 (Task Time)**: 制限時間は**10分**とする．

    1. **セットアップ (Setup)**: `TC`はチームにロボットを*Start Location*に移動するよう指示する．

    1. **カテゴリ選択 (Category Selection)**: チームは選択したカテゴリを`TC`に伝える．
    カテゴリによって，`TC`は任意のコマンドを選び，ホストに与える．
      - **DEMカテゴリ**: 事前に定義された文章構成による指示．
      - **通常カテゴリ**: [Command Generator - Branch: rcj25_for_opl](https://github.com/RoboCupAtHomeJP/CommandGenerator/tree/rcj25_for_opl)から生成された指示．

    1. **開始 (Start)**: TCが*開始合図(start signal)*を出し，タイマーを開始する．
    チームはセットアップを完了させ（スタートボタンを押すなど），エリアを離れる．
    2つ以上のボタンを押すなどの複雑なセットアップ手順は許可されない．

    1. **タイマーの一時停止(Pausing the Timer)**: ロボットが*Instruction Point*に到達すると、`TC`は次のコマンドのために*Arena*を準備する時間を確保するためタイマを一時停止する。ホストが次のコマンドのためにロボットの前に戻るとタイマーが再開される。

    1. **目的 (Goal)**: ロボットはコマンドフェーズとサービスフェーズを**3回**行う．

1. **コマンドフェーズ (Command Phase)**

    1. **ホストへの移動 (Navigation to Operator)**: ロボットは*Instruction Point*へ移動する．

    1. **ロボットへの指示 (Instruct the Robot)**: `TC`が次のコマンドのために*Arena*の準備を終えた後、ホストは`TC`から与えられたタスクをロボットに指示する．
    ロボットがコマンドを理解できない場合，ロボットはホストにそのコマンドを繰り返すように要求することができ，ペナルティが課されない．

1. **サービスフェーズ (Service Phase)**

    1. **コマンド確認 (Command Confirmation)**: コマンドを受け取った後，ロボットはタスクを実行する前にコマンドを確認する必要がある．

    1. **コマンド実行 (Command Execution)**: ロボットは指示に従ってタスクを実行する．


## その他のルールと注意事項 (Additional Rules and Remarks)

### コマンドジェネレータ (Command Generator)

コマンドは，[Command Generator - Branch: rcj25_for_opl](https://github.com/RoboCupAtHomeJP/CommandGenerator/tree/rcj25_for_opl)から生成される．
`TC`は環境のセットアップに応じて事前にコマンドを任意に生成し，コマンドの正確さを確認する．

競技チームが*DEMカテゴリ*を選択した場合，公平性を保ちつつ，与えられるコマンドはあらかじめ準備され，[DEMカテゴリの文章構成](#demカテゴリの文章構成-dem-category-sentence-structure)に基づく．

### コマンドのスキップ - 1.5ルール (Skipping Commands - 1.5 Rule)

ロボットは`コマンドフェーズ`と`サービスフェーズ`を3回行う．
ただし，ロボットがホストから与えられたコマンドを誤認識した場合，競技チームは次のコマンドにスキップすることができる．
ロボットが誤認識したことを示すためには，ロボットは間違ったタスクを完了させ，ホストの位置に戻って，次のコマンドを要求する必要がある．

> [!WARNING]
> チームはこのルールを悪用して，希望のコマンドが与えられるまでコマンドをスキップすることはできない．


## デウス・エクス・マキナ (Deus Ex Machina)

競技チームは、ロボットがホストから与えられたコマンドを誤解した場合、次のコマンドにスキップできます。

ただし，コマンドをスキップするには、**1.5ルール**が適用されます。
このルールは、競技チームがスキップルールを悪用しないようにするためのものです。

**1.5ルール**は次のように適用されます:
- ロボットが*コマンド確認*中に誤ったコマンドを正しいだと判断し、
- ロボットが*誤ったコマンド実行*に進む、
- ロボットが[カテゴリーごとのステップ](#タスクごとのstep一覧-steps-per-task)で定義された*Step 1*を完了する、
- ロボットが*Step 2*を完了するか完了しようとし（例: 物体を掴もうとして，失敗することや、人物を追従できないなど）、
- その後初めて、ロボットは*Instruction Point*に戻り、次のタスクを要求することができます。


## リスタート (Restart)

リスタートは段階に応じて以下のように取り扱う．
なお，リスタートした場合，ロボットはスタート地点からタスクを再開する．
[カテゴリーごとのステップ](#タスクごとのstep一覧-steps-per-task)のStep 1を完了している場合，リスタート後にスタート地点から再開せずに，直前のタスクを継続してもよい．
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
| **Manipulation** <br>grasp, give \| place            | &bullet; Go to the `$ROOM`, grasp the `$OBJECT` on the `$PLACE` and place it on the `$PLACE`. <br>&bullet; Go to the `$ROOM`, grasp the `$OBJECT` on the `$PLACE` and give it to `$PERSON`. |
| **Vision (Enumeration)** <br>count (obj \| people) | &bullet; Tell me how many `$CATEGORY_OBJ` there are on the `$PLACE`. <br>&bullet; Tell me how many people in the `$ROOM` are `$POSE/GESTURE`. |
| **Vision (Description)** <br>find (obj \| person)  | &bullet; Tell me what is the `$OBJ_COMP` object on the `$PLACE`. <br>&bullet; Tell me the `$PERS_INFO` of the person at the `$PLACE` |
| **Navigation** <br>follow, guide                   | &bullet; Go to the `$ROOM`, find `$POSE/GESTURE` person and follow (him \| her). <br>&bullet; Go to the `$ROOM`, find `$POSE/GESTURE` person and guide (him \| her) to the `$ROOM`. |
| **Speech** <br>answer, tell                        | &bullet; Go to the `$ROOM`, find `$PERSON` at the `$PLACE` and answer (his \| her) question. <br>&bullet; Go to the `$ROOM`, find the person who is `$POSE/GESTURE` and tell (him \| her) `$TELL_LIST`. |
<!-- | **Speech** <br>answer, ask                         | &bullet; Go to the `$ROOM`, find `$PERSON` at the `$PLACE` and answer (his \| her) question. <br>&bullet; Go to the `$ROOM`, find `$PERSON` at the `$PLACE` and ask (him \| her) `$QUESTION`. | -->

> [!NOTE]
> `$POSE/GESTURE`, `$OBJ_COMP`, `PERS_INFO`, `QUESTION_LIST` と `$TELL_LIST` はTLMやDiscordを通して決定する．

> [!IMPORTANT]
> スコアリングのため，CmdGenから生成される`greeting`関連のコマンドを使用しない．

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

| 行動 (Action) | スコア (Score) |
| --- | --- |
| **メインタスク (Main Task)**                            |  |
| &emsp; - 命令を理解する | $3 \times 20$                 | $3 \times 20$ |
| &emsp; - 1回目のコマンドを実行する                    | $(15 \times 4) \times Weight$ |
| &emsp; - 2回目のコマンドを実行する                    | $(30 \times 4) \times Weight$ |
| &emsp; - 3回目のコマンドを実行する                    | $(60 \times 4) \times Weight$ |
| &emsp; - 全てのコマンドを実行した後*Arena*から退出する  | $20$ |
| ***デウス・エクス・マキナ (Deus Ex Machina)***                        |  |
| &emsp; - 内部オペレータを通してコマンドを理解する                               | $3 \times -2$ |
| &emsp; - QRコードを用いて命令を理解する                               | $3 \times -10$ |
| &emsp; - $h (\le 10)$ 回の人間の支援により1回目のコマンドを実行する | $-6h \times Weight$ |
| &emsp; - $h$ 回の人間の支援により2回目のコマンドを実行する          | $-12h \times Weight$ |
| &emsp; - $h$ 回の人間の支援により3回目のコマンドを実行する          | $-24h \times Weight$ |
| **ペナルティ (Penalty)**                                |  |
| &emsp; - リスタート                                     | $直後に獲得した点数  \times 0.5$| 
| &emsp; - 不参加（無断）                                 | $-500$ |
| **合計**                                                | $500$ |

**得点係用のスコアシート**: GPSR-score_sheet (TBD)
**得点係用のスコアシート**: [GPSR-score_sheet](./doc/RCJ2025_OPL_GPSR-score_sheet.pdf)


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
   - *Instruction Point*を発表する．
   - 物体，カテゴリ，場所の位置を発表する．
   - 名前と飲み物のリストを発表する．
- 競技前:
   - 競技チームによって選ばれたゲスト役のボランティアを確認する．
   - ボランティアに名前を割り当てる．
   - 競技チームが使用する*Command Category*を確認する.
   - コマンドに応じて，*Arena*の工夫をする．
- 競技中:
   - ホストにコマンドを伝える．
