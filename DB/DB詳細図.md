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
|削除日|del_date|datetime||||

## m_shop

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|店ID|shop_id|int(8)|○|○||
|店名|shop_name|varchar(100)||○||
|店説明|shop_explanation|varchar(200)||||
|店画像|shop_image|varchar(80)||||
|店緯度|shop_latitude|int(6)||||
|店経度|shop_longitude|int(6)||||
|登録日|reg_date|datetime||○||
|更新日|upd_date|datetime||||
|削除日|del_date|datetime||||

## m_shopCategory

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|店ID|shop_id|int(8)|○|○||
|店カテゴリID|shopCategory_id|int(8)|○|○||
|登録日|reg_date|datetime||○||
|更新日|upd_date|datetime||||
|削除日|del_date|datetime||||

## m_shopCategoryID

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|店ID|shopCategory_id|int(8)|○|○||
|店カテゴリー名|shopCategory_name|varchar(100)||○||
|登録日|reg_date|datetime||○||
|更新日|upd_date|datetime||||
|削除日|del_date|datetime||||
削除日|del_date|datetime||||

## t_shopExplanation

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|店ID|shop_id|int(8)|○|○||
|店説明|shop_explanation|varchar(200)||||
|店画像|shop_image|varchar(80)||||
|登録日|reg_date|datetime||○||
|更新日|upd_date|datetime||||
|削除日|del_date|datetime||||

## t_bulletinBoardComment

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|掲示板ID|bulletinBoard_id|int(8)|○|○|○|
|コメントID|comment_id|int(8)|○|○|○|
|ユーザーID|user_id|int(8)||○|○|
|コメント|comment|varchar(200)||○||
|コメント先ID|commentDestination_id|int(8)||||
|いいね(参考になった)|good_count|int(8)||○||
|登録日|reg_date|datetime||○||
|更新日|upd_date|datetime||||
|削除日|del_date|datetime||||

## t_RecruitmentBulletinBoard

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|募集掲示板ID|RecruitmentbulletinBoard_id|int(8)|○|○||
|ユーザーID|user_id|int(8)||○|○|
|募集掲示板タイトル|RecruitmentbulletinBoard_title|varchar(50)||○||
|コースID|course_id|int(8)||○|○|
|サイクリング予定日|schedule_date|datetime|||○||
|参加者数|participantUser_num|int(2)||○||
|登録日|reg_date|datetime||○||
|更新日|upd_date|datetime||||
|削除日|del_date|datetime||||

## t_RecruitmentBulletinBoardComment

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|掲示板ID|RecruitmentbulletinBoard_id|int(8)|○|○|○|
|コメントID|comment_id|int(8)|○|○|○|
|募集掲示板説明|RecruitmentbulletinBoard_explanation|varchar(200)||||
|ユーザーID|user_id|int(8)||○|○|
|コメント|comment|varchar(200)||○||
|コメント先ID|commentDestination_id|int(8)||||
|いいね(参考になった)|good_count|int(8)||○||
|登録日|reg_date|datetime|||○||
|更新日|upd_date|datetime|||||
|削除日|del_date|datetime|||||

## t_participantUser

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|募集掲示板ID|RecruitmentbulletinBoard_id|int(8)|○|○|○|
|ユーザーID|user_id|int(8)|○|○|○|
|参加順番|participant_num|int(2)||○||
|登録日|reg_date|datetime||○||
|更新日|upd_date|datetime||||
|削除日|del_date|datetime||||

## t_searchHistory

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|検索履歴ID|searchHistory_id|int(8)|○|○||
|ユーザーID|user_id|int(8)|○|○|○|
|検索ワード|searchWord|varchar(200)||○||
|登録日|reg_date|datetime||○||
|削除日|del_date|datetime||||

## t_checkpointPhoto
|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|写真ID|Photo_id|int(8)|○|○||
|チェックポイントID|checkpoint_id|int(8)|○|○|○|
|写真名(画像ファイル名)|Photo_name|varchar(200)||○||
|ユーザーID|user_id|int(8)||○|○|
|登録日|reg_date|datetime||○||
|削除日|del_date|datetime||||

## m_userImage
|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|ユーザー画像ID|userimage_id|int(8)|○|○||
|ユーザーID|user_id|int(8)|○|○|○|
|画像ファイル名|userimage_name|varchar(200)||○||
|登録日|reg_date|datetime||○||
|削除日|del_date|datetime||||
