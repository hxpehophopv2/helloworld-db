# helloworld-db

## UserType

| Type | Description |
| customer | Customer of the system |
| admin | Admin of the system |

## User

| Attribute | Data Type | Description | Constraints |
| --- | --- | --- | --- |
| user_id | serial | UID of the user | Primary key |
| firstname | varchar(255) | User's firstname | Not null |
| surname | varchar(255) | User's surname | Not null |
| phonenumber | varchar(10) | User's phone number | Not null |
| user_type | UserType | User's role | Default(customer) |

## Appointment

| Attribute | Data Type | Description | Constraints |
| --- | --- | --- | --- |
| appointment_id | serial | UID of the appointment | Primary key |
| broken_part | varchar(255) | The part of the car that is broken and needs to be fixed | Null |
| short_description | varchar(255) | Brief description of the appointment | Null |
| user_id | integer | User ID of the user that created this appointment | Foreign key, Not null |
| car_id | integer | Car ID of the car that needs fixing | Foreign key, Not null |

## Car

| Attribute | Data Type | Description | Constraints |
| --- | --- | --- | --- |
| car_id | serial | UID of the car | Primary key |
| brand | varchar(255) | Brand of the car | Not null |
| model | varchar(255) | Model of the car | Not null |
| owner | integer | Owner of the car | Not null |

## Movie

| Attribute | Data Type | Description | Constraints |
| --- | --- | --- | --- |
| movie_id | serial | UID of the movie | Primary key |
| category_id | integer | Category of the movie | Foreign key, Not null |
| title | varchar(255) | The movie title | Not null |
| duration | integer | Duration of the movie (in minutes) | Not null |
| dub_language | varchar(255) | The language of the movie's audio | Not null |
| sub_language | varchar(255) | The language of the movie's captions | Not null |

## Customer

| Attribute | Data Type | Description | Constraints |
| --- | --- | --- | --- |
| customer_id | serial | UID of the customer | Primary key |
| firstname | varchar(255) | Customer's firstname | Not null |
| surname | varchar(255) | Customer's lastname | Not null |
