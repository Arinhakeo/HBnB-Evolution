```mermaid
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
    class FacadePattern {
        <<Definition>>
        The Facade pattern provides a simplified interface
        to a complex subsystem. It encapsulates a group
        of interfaces in a higher-level interface,
        making the subsystem easier to use.
    }
    PresentationLayer --> BusinessLogicLayer : Uses Facade Pattern
    BusinessLogicLayer --> PersistenceLayer : Performs Database Operations
    FacadePattern .. BusinessLogicLayer : Implements
    %% note right of PresentationLayer : The facade pattern simplifies access to business services.
