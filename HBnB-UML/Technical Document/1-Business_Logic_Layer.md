# __Business Logic Layer__

```mermaid
classDiagram
    class Entity {
        +id: UUID4
        +created_at: DateTime
        +updated_at: DateTime
        +create()
        +update()
        +delete()
    }
    class User {
        +first_name: String
        +last_name: String
        -email: String
        -password: String
        +check_administrator(): Boolean
        +register_user()
        +update_user_info()
    }
    class Place {
        +title: String
        +description: String
        +price_per_night: Float
        +latitude: Float
        +longitude: Float
        +get_owner(): User
        +list_amenities(): List[Amenity]
        +calculate_average_rating(): Float
    }
    class Review {
        +rating: Integer
        +comment: String
        +get_user(): User
        +get_place(): Place
    }
    class Amenity {
        +name: String
        +description: String
        +list_places(): List[Place]
    }
    Entity <|-- User
    Entity <|-- Place
    Entity <|-- Review
    Entity <|-- Amenity
    User "1" -- "0..*" Review : leaves
    User "1" -- "0..*" Place : owns
    Place "1" -- "0..*" Amenity : has
    Place "1" -- "0..*" Review : receives
    ```
