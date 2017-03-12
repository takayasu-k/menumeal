Database Settings

Shops

|  name   |  type  |  option  |
|:-------:|:------:|:--------:|
|  name   | string | NOT_NULL |
| address | string | NOT_NULL |
|   tel   | string |          |
| picture | string |          |

Staffs (deviseを使用)

|   name   |  type  |      option      |
|:--------:|:------:|:----------------:|
| shop_id  |  int   |   FOREIGN KEY    |
|  email   | string | NOT_NULL, UNIQUE |
| password | string |     NOT_NULL     |


Shop_details

|      name       |  type  |   option    |
|:---------------:|:------:|:-----------:|
|     shop_id     |  int   | FOREIGN KEY |
|     access      | string |             |
|     parking     | string |             |
| operating_hours | string |             |
|     holiday     | string |             |
|     budget      | string |             |
|     payment     | string |             |
|      seats      |  int   |             |
|  private_room   | string |             |
|     smoking     | string |             |
|       bar       | string |             |

Shop_pictures

|  name   |  type  |       option        |
|:-------:|:------:|:-------------------:|
| shop_id |  int   |     FOREIGN KEY     |
| picture | string |      NOT_NULL       |
|  type   |  int   | NOT_NULL, default:0 |
| user_id |  int   |     FOREIGN KEY     |


Menus

|     name     |  type  |       option        |
|:------------:|:------:|:-------------------:|
|   shop_id    |  int   |     FOREIGN KEY     |
|     name     | string |      NOT_NULL       |
|    price     |  int   |      NOT_NULL       |
|    status    |  int   | NOT_NULL, default:0 |
|     type     |  int   |      NOT_NULL       |
| desire_count |  int   | NO_NULL, default:0  |



Menus_reviews

|   name    | type |   option    |
|:---------:|:----:|:-----------:|
|  menu_id  | int  | FOREIGN KEY |
| review_id | int  | FOREIGN KEY |

Reviews

|    name    |  type  |       option        |
|:----------:|:------:|:-------------------:|
|  content   | string |      NOT_NULL       |
|  picture   | string |      NOT_NULL       |
|  user_id   |  int   |     FOREIGN KEY     |
|  menu_id   |  int   |     FOREIGN KEY     |
| like_count |  int   | NOT_NULL, default:0 |


Likes

|   name    | type |   option    |
|:---------:|:----:|:-----------:|
|  user_id  | int  | FOREIGN KEY |
| review_id | int  | FOREIGN KEY |

Comments

|   name    |  type  |   option    |
|:---------:|:------:|:-----------:|
| review_id |  int   | FOREIGN KEY |
|  user_id  |  int   | FOREIGN KEY |
|  content  | string |  NOT_NULL   |


Users (deviseを使用)

|   name   |  type  |      option      |
|:--------:|:------:|:----------------:|
|   name   |  int   |     NOT_NULL     |
|  email   | string | NOT_NULL, UNIQUE |
| password | string |     NOT_NULL     |
| picture  | string |                  |



Desired_menus

|  name   | type |   option    |
|:-------:|:----:|:-----------:|
| menu_id | int  | FOREIGN KEY |
| user_id | int  | FOREIGN KEY |

Eaten_menus

|  name   | type |   option    |
|:-------:|:----:|:-----------:|
| menu_id | int  | FOREIGN KEY |
| user_id | int  | FOREIGN KEY |

User_profiles

|   name   |  type  |       option        |
|:--------:|:------:|:-------------------:|
| user_id  |  int   |     FOREIGN KEY     |
| profile  | string |                     |
| birthday |  date  |                     |
|  gender  |  int   | NOT_NULL, default:0 |


Relationships

|    name     | type |   option    |
|:-----------:|:----:|:-----------:|
| follower_id | int  | FOREIGN KEY |
| followed_id | int  | FOREIGN KEY |
