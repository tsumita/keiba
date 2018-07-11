# keiba
競馬予測（取り組み中）


## DBテーブル情報
table               | description
:------------------ | :-------------
horse_info_per_race | 各レースにおける各出走馬の情報、及び結果
races               | 各レース情報


## horse_info_per_raceテーブル情報
column         | type   | example        | description
:------------- | :----- | :------------- |:----------
race_id        | INT    | 21201          |レースID（racesテーブルと紐づく）
a_num          | INT    | 2              |着番
f_num          | INT    | 8              |枠番
h_num          | INT    | 16             |馬番
h_name         | STRING | キッスアフィニティ|馬名
sex            | STRING | 牡             |性別
age            | INT    | 2              |年齢
b_weight       | INT    | 55             |斤量
jockey         | STRING | 柴山雄一        |騎手
time           | STRING | 1:49.0         |タイム
diff_a         | STRING | 1/2            |着差
passing        | STRING | 8-9-7-5        |通過
uphill         | FLOAT  | 35.1           |上り
1win           | FLOAT  | 7.3            |単勝オッズ
popularity     | INT    | 4              |人気
h_weight       | INT    | 508            |馬体重
weight_increase| STRING | +8             |前回との増減量
trainer        | STRING | 久保田貴        |調教師
owner          | STRING | シルクレーシング  |馬主
prize          | FLOAT  | 200            |賞金[万円]

![horse_infoTABLE](./image/horse_info_per_race.png)

## racesテーブル情報
column         | type   | example        | description
:------------- | :----- | :------------- |:----------
race_id        | INT    | 21201          |レースID（horse_info_per_raceテーブルと紐づく）
race_name      | STRING | 2歳未勝利       |レース名
race_page_num  | STRING | 201403030502   |スクレイピング用ページ番号
place          | STRING | 福島            |競馬場の所在
year           | INT    | 2014           |年
month          | INT    | 11             |月
day            | INT    | 1              |日にち
date           | INT    | 20141101       |日付（年/月/日）
direction      | STRING | 右             |周回方向（右・左）
distance       | INT    | 1800           |競走距離[メートル]
climate        | STRING | 小雨            |天候（晴・曇・小雨・雨・小雪・雪）
course         | STRING | 芝              |コース（芝・ダート）
condition      | STRING | 良              |コース状態（良・稍重・重・不良）
the_start      | STGING | 10:20          |発走時間
prize          | FLOAT  | 500            |このレースの最高賞金[万円]
entry          | INT    | 16             |出走馬数

![race_infoTABLE](./image/race_info.png)
