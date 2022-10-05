```uml
@startuml

skinparam class {
    '図の背景
    BackgroundColor Snow
    '図の枠
    BorderColor Black
    'リレーションの色
    ArrowColor Black
}

!define MASTER_MARK_COLOR Orange 
!define TRANSACTION_MARK_COLOR DeepSkyBlue

package "Gohunt" as target_system {
    
    
    entity "ユーザーマスタ" as users  <m_users> <<M,MASTER_MARK_COLOR>> {
        + user_id[PK]
        --
        user_name
        # userimage_id [FK]
        user_mail
        user_pass
        age
        sex_Flag
        reg_date
        upd_date
    }
    
    entity "プレユーザーマスタ" as pre_users  <m_pre_users> <<M,MASTER_MARK_COLOR>> {
        + pre_user_id[PK]
        --
        pre_user_mail
        pre_user_token
        reg_date
        upd_date
    }
    
    entity "ショップマスタ" as m_shop  <m_shop> <<M,MASTER_MARK_COLOR>> {
        +shop_id[PK]
        --
        shop_id
        user_id
        shop_latitude
        shop_longitude
        shop_address
        reg_date
        upd_date
    }
    
    entity "タグマスタ" as m_tag  <m_tag> <<M,MASTER_MARK_COLOR>> {
        +tag_id[PK]
        --
        tag_name
        reg_date
        upd_date
    }
    
    entity "ショップExpテーブル" as t_shopExplanation <t_shopExplanation> <<M,MASTER_MARK_COLOR>> {
        +shop_id[PK]
        --
        shop_name
        shop_explanation
        shop_image
        # tag_id [FK]
        reg_date
        upd_date
    }
@enduml
```
