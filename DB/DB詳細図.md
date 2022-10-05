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

## m_pre_users

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|ユーザーID|pre_user_id|int(8)|○|○||
|ユーザー名|pre_user_name|varchar(20)||○||
|メールアドレス|pre_user_mail|varchar(100)||○||
|パスワード|pre_user_pass|varchar(255)||○||
|年代|pre_age|int(3)||○||
|性別フラグ|pre_sex_flag|int(2)||○||
|トークン|pre_user_token|varchar(255)||○||
|登録日|reg_date|datetime||○||
|更新日|upd_date|datetime||||
|フラグ|flag|int(1)||○||
|変更先ユーザーID|change_user_id|int(8)||||

## m_shop

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|店ID|shop_id|int(8)|○|○||
|店緯度|shop_latitude|int(6)||○||
|店経度|shop_longitude|int(6)||○||
|店住所|shop_address|varchar(200)||○|○|
|登録ユーザーID|user_id|int(8)||○||
|登録日|reg_date|datetime||○||
|更新日|upd_date|datetime||||

## m_Tag

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|タグID|Tag_id|int(8)|○|○||
|タグ名|Tag_name|varchar(80)|||○|
|登録日|reg_date|datetime||○||
|更新日|upd_date|datetime||||

## t_shopExplanation

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|店ID|shop_id|int(8)|○|○||
|店名|shop_name|varchar(100)||○||
|店説明|shop_explanation|varchar(200)||○||
|店画像|shop_image|varchar(80)||○||
|タグID|shop_tag|varchar(80)||○|○|
|最終変更ユーザーID|user_id|int(8)||○||
|更新日|up_date|datetime||○||
|登録日|reg_date|datetime||○||
