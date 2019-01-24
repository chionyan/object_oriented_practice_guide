## アプリケーション例：自転車旅行会社

### 会社内容

- 会社名：株式会社FastFeet社
- 事業内容：ロードバイクとマウンテンバイクの自転車旅行の提供

### 旅行内容

- 開催頻度：年に数回程度
- 旅行にはそれぞれ参加者の上限が決まっている
- 同行するガイドも一定数必要
  - ガイドは整備士を兼ねている
- 各旅行に必要な体力に応じた難易度がつけられる
  - マウンテンバイク旅行は技術の難易度も追加
- 自転車は借りることも持ち込むこともできる
- 会社は貸出用の自転車を自社で数台保有
  - 貸出自転車の在庫を地域の自転車店と共有
  - 貸出用自転車はロードバイクもマウンテンバイクも保持
  - 客が自転車を借りれるかはわからない

### 要件

「参加者が適切な難易度の、特定の日付の、自転車を借りられる旅行の一覧を見たい」


### モデル

- Customer: 参加者クラス
  - date: 希望する日付
  - difficulty: 体力レベル
  - need_bike: 自転車レンタル希望可否
  - マウンテンバイクの技術スキルレベル

- Trip(旅行)
  - 日付
  - 参加者上限
  - 同行するガイド達
  - 体力難易度
  - マウンテンバイク技術レベル
  - 行程

- Route(行程)
  - 行き先
  - 自転車種類

- Bike(自転車)
  - 種類

- Mechanic(整備士)