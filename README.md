Database Settings

Shops

|         |        |   |
|:-------:|:------:|:-:|
|   id    |  int   |   |
|  name   | string |   |
| address |  text  |   |
|   tel   | string |   |
| picture | string |   |

Staffs

|          |        |   |
|:--------:|:------:|:-:|
|    id    |  int   |   |
| shop_id  |  int   |   |
| password | string |   |


Shop's details

|              |      |   |
|:------------:|:----:|:-:|
|   shop_id    | int  |   |
|    access    | text |   |
|   parking    | text |   |
|  ope_hours   | text |   |
|   holiday    | text |   |
|    budget    | text |   |
|   payment    | text |   |
| no_of_seats  | text |   |
| private_room | text |   |
|   smoking    | text |   |
|     bar      | text |   |

Shop's pictures

|         |        |   |
|:-------:|:------:|:-:|
|   id    |  int   |   |
| shop_id |  int   |   |
| picture | string |   |
|  type   |  int   |   |
| user_id |  int   |   |


Menus

|            |        |   |
|:----------:|:------:|:-:|
|     id     |  int   |   |
|  shop_id   |  int   |   |
|    name    | string |   |
|   price    |  int   |   |
| status_id  |  int   |   |
|  type_id   |  int   |   |
| want_count |  int   |   |


Menu types

|      |      |   |
|:----:|:----:|:-:|
|  id  | int  |   |
| type | text |   |

Menu_status

|        |      |   |
|:------:|:----:|:-:|
|   id   | int  |   |
| status | text |   |

Menu_reviews

|           |     |   |
|:---------:|:---:|:-:|
|  menu_id  | int |   |
| review_id | int |   |

Reviews

|            |        |   |
|:----------:|:------:|:-:|
|     id     |  int   |   |
|  content   |  text  |   |
|  picture   | string |   |
|  user_id   |  int   |   |
|  menu_id   |  int   |   |
| like_count |  int   |   |


Likes

|           |     |   |
|:---------:|:---:|:-:|
|  user_id  | int |   |
| review_id | int |   |

Comments

|           |      |   |
|:---------:|:----:|:-:|
|    id     | int  |   |
| review_id | int  |   |
|  user_id  | int  |   |
|  content  | text |   |


Users

|          |        |   |
|:--------:|:------:|:-:|
|    id    |  int   |   |
|   name   |  int   |   |
|  email   | string |   |
| password | string |   |
| picture  | string |   |


Wants(食べたい)

|         |     |   |
|:-------:|:---:|:-:|
| menu_id | int |   |
| user_id | int |   |

Tabeta(食べた)

|         |     |   |
|:-------:|:---:|:-:|
| menu_id | int |   |
| user_id | int |   |
|  date   |  ?  |   |

User's details

|          |      |   |
|:--------:|:----:|:-:|
| user_id  | int  |   |
| profile  | text |   |
| birthday | date |   |
|   sex    | text |   |


Relationships

|             |     |   |
|:-----------:|:---:|:-:|
| follower_id | int |   |
| followed_id | int |   |
