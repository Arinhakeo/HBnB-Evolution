```mermaid
classDiagram
    class User {
        +UUID id
        +String firstName
        +String lastName
        +String email
        +String password
        +boolean isAdmin
        +Date createdAt
        +Date updatedAt
        +register()
        +updateProfile()
        +deleteAccount()
    }

    class Place {
        +UUID id
        +String title
        +String description
        +double price
        +double latitude
        +double longitude
        +Date createdAt
        +Date updatedAt
        +listAmenities()
        +addAmenity(Amenity amenity)
        +removeAmenity(Amenity amenity)
    }

    class Review {
        +UUID id
        +int rating
        +String comment
        +Date createdAt
        +Date updatedAt
        +createReview()
        +updateReview()
        +deleteReview()
    }

    class Amenity {
        +UUID id
        +String name
        +String description
        +Date createdAt
        +Date updatedAt
    }

    %% Relationships
    User "1" --o "0..*" Place : owns >
    Place "1" o-- "0..*" Review : has >
    Place "1" o-- "0..*" Amenity : includes >

        %% Notes
    %% User class represents registered users of the system
    %% Place class represents accommodation listings
    %% Review class allows users to rate and comment on places
    %% Amenity class represents features or services offered by a place
    %% Relationships show that:
    %%   - A User can own multiple Places (or none)
    %%   - A Place can have multiple Reviews (or none)
    %%   - A Place can include multiple Amenities (or none)
    %% All classes include creation and update timestamps for auditing
