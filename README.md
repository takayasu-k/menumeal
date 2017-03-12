Database Settings

Shops

|  name   |  type  |  option  |
|:-------:|:------:|:--------:|
|  name   | string | NOT_NULL |
| address | string | NOT_NULL |
|   tel   | string |          |
| picture | string | DEFAULT  |

Staffs (deviceを使用)

|     name     |  type  |      option      |
|:------------:|:------:|:----------------:|
| shop_id (FK) |  int   |                  |
|    email     | string | NOT_NULL, UNIQUE |
|   password   | string |     NOT_NULL     |


Shop_details
|      name       |  type  | option |
|:---------------:|:------:|:------:|
|  shop_id (FK)   |  int   |        |
|     access      | string |        |
|     parking     | string |        |
| operating_hours | string |        |
|     holiday     | string |        |
|     budget      | string |        |
|     payment     | string |        |
|   no_of_seats   |  int   |        |
|  private_room   | string |        |
|     smoking     | string |        |
|       bar       | string |        |

Shop_pictures

|     name     |  type  |  option  |
|:------------:|:------:|:--------:|
| shop_id (FK) |  int   |          |
|   picture    | string | NOT_NULL |
|     type     |  int   | NOT_NULL |
| user_id (FK) |  int   |          |


Menus

|     name     |  type  |  option  |
|:------------:|:------:|:--------:|
| shop_id (FK) |  int   |          |
|     name     | string | NOT_NULL |
|    price     |  int   | NOT_NULL |
|  status_id   |  int   | DEFAULT  |
| type_id (FK) |  int   |          |
| desire_count |  int   |          |


Menu_types(drink/food/others)

| name |  type  | option |
|:----:|:------:|:------:|
| type | string |        |

Menu_status

|  name  |  type  | option |
|:------:|:------:|:------:|
| status | string |        |

Menus_reviews

|      name      | type |  option  |
|:--------------:|:----:|:--------:|
|  menu_id (FK)  | int  |          |
| review_id (FK) | int  |          |

Reviews

|     name     |  type  |  option  |
|:------------:|:------:|:--------:|
|   content    | string | NOT_NULL |
|   picture    | string | NOT_NULL |
| user_id (FK) |  int   |          |
| menu_id (FK) |  int   |          |
|  like_count  |  int   |          |


Likes

|      name      | type | option |
|:--------------:|:----:|:------:|
|  user_id (FK)  | int  |        |
| review_id (FK) | int  |        |

Comments

|      name      |  type  |  option  |
|:--------------:|:------:|:--------:|
| review_id (FK) |  int   |          |
|  user_id (FK)  |  int   |          |
|    content     | string | NOT_NULL |


Users

|   name   |  type  |      option      |
|:--------:|:------:|:----------------:|
|   name   |  int   |     NOT_NULL     |
|  email   | string | NOT_NULL, UNIQUE |
| password | string |     NOT_NULL     |
| picture  | string |     DEFAULT      |



Desired_menus

|     name     | type |  option  |
|:------------:|:----:|:--------:|
| menu_id (FK) | int  |          |
| user_id (FK) | int  |          |

Eaten_menus

|     name     | type |  option  |
|:------------:|:----:|:--------:|
| menu_id (FK) | int  |          |
| user_id (FK) | int  |          |
|     date     | date | NOT_NULL |

User_profiles

|     name     |  type  |  option  |
|:------------:|:------:|:--------:|
| user_id (FK) |  int   |          |
|   profile    | string | DEFAULT  |
|   birthday   |  date  |          |
|    gender    |  enum  |          |


Relationships

|       name       | type |  option  |
|:----------------:|:----:|:--------:|
| follower_id (FK) | int  |          |
| followed_id (FK) | int  |          |
