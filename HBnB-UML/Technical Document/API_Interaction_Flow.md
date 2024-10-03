:::mermaid
classDiagram
    class PresentationLayer {
        <<Interface>>
        +UserService
        +PlaceService
        +ReviewService
        +AmenityService
        +APIEndpoints
    }

    class BusinessLogicLayer {
        +User
        +Place
        +Review
        +Amenity
    }

    class PersistenceLayer {
        +UserRepository
        +PlaceRepository
        +ReviewRepository
        +AmenityRepository
    }

    PresentationLayer --> BusinessLogicLayer : Utilise le Patron de Façade
    BusinessLogicLayer --> PersistenceLayer : Effectue des Opérations sur la Base de Données

    note right of PresentationLayer : Le patron de façade simplifie l'accès aux services métier.