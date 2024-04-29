- groups:
  + id
  + name
  + slug
  + auto_approval bool true
  + about null
  + user_id
  + cover_path 1024 nullable
  + thumbnail_path 1024 nullable
  + deleted_by nullable
  + deleted_at nullable

- group_users:
    + role string 25
    + status string 25
    + token string 1024 null
    + token_expire_date timestamp null
    + token_used timestamp null
    + user_id
    + group_by
    + created_by
    + created_at

- posts:
  + id
  + body longText nullable
  + user_id long
  + group_id long nullable
  + deleted_id long nullable
  + deleted_at datetime nullable
  + timestamps

- post_attachments:
  + post_id
  + name 255
  + path 255
  + mime 25
  + created_by
  + created_at

- post_reactions:
  - post_id
  - user_id
  - type 
  - created_at null

- comments:
  - post_id
  - user_id
  - comment text
  - created_at
  - updated_at

- followers:
  - user_id
  - follower_id
  - created_at null

- users:
  - username
  - cover_path
  - avatar_path
