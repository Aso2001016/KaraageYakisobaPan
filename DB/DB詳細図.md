# DB定義書
## ER図
[ER図はこちら]()

*****
<>

*****

# データベース設計図

## m_users

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|ユーザーID|user_id|int(8)|○|○||
|ユーザー名|user_name|varchar(20)||○||
|メールアドレス|user_mail|varchar(100)||○||
|パスワード|user_pass|varchar(20)||○||
|年代|age|int(3)||○||
|性別フラグ|sex_Flag|int(2)||○||
|登録日|reg_date|datetime||○||
|更新日|upd_date|datetime||||

## m_shop

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|店ID|shop_id|int(8)|○|○||
|店名|shop_name|varchar(100)||○||
|登録ユーザーID|user_id|int(8)||○||
|登録日|reg_date|datetime||○||
|更新日|upd_date|datetime||||

## m_shopAddress

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|店ID|shop_id|int(8)|○|○||
|店緯度|shop_latitude|int(6)||○||
|店経度|shop_longitude|int(6)||○||
|店住所|shop_address|varchar(200)||○|○|
|登録日|reg_date|datetime||○||
|更新日|upd_date|datetime||||

## m_tag

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|タグID|tag_id|int(8)|○|○||
|タグ名|tag_name|varchar(80)|||○|
|登録日|reg_date|datetime||○||
|更新日|upd_date|datetime||||

## t_shopExplanation

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|店ID|shop_id|int(8)|○|○||
|店説明|shop_explanation|varchar(200)||○||
|画像ID|shop_image_ID|varchar(80)||○|○|
|店画像|shop_image|varchar(80)||○||
|タグID|tag_id|varchar(80)||○|○|
|最終変更ユーザーID|user_id|int(8)||○||
|更新日|up_date|datetime||○||
|登録日|reg_date|datetime||○||

## t_shopImage

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|画像ID|shop_image_ID|varchar(80)|○|○|○|
|店画像|shop_image|varchar(80)||○||
|最終変更ユーザーID|user_id|int(8)||○||
|更新日|up_date|datetime||○||
|登録日|reg_date|datetime||○||
