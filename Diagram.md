```mermaid
classDiagram
    class User {
        +username: str
        +password: str
        +login()
        +logout()
        +encrypt_message()
        +decrypt_message()
    }

    class Image {
        +name: str
        +path: str
        +encrypt()
        +decrypt()
    }

    class Database {
        +host: str
        +port: int
        +username: str
        +password: str
        +store_image()
        +retrieve_image()
    }

    class Encryption {
        +algorithm: str
        +key: str
        +encrypt()
        +decrypt()
    }

    User --> Image
    Image --> Encryption
    Image --> Database
    Encryption --> User
    Database --> Encryption
