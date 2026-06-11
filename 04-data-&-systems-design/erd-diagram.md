```mermaid
erDiagram
    CUSTOMER ||--o{ WEB_ORDER : "places"
    WEB_ORDER ||--|| INVENTORY : "reserves"
    STORE ||--o{ INVENTORY : "holds"
    STORE ||--|{ POS_SYSTEM : "operates"

    CUSTOMER {
        string CustomerID PK
        string Name
        string Email
        string Phone
    }

    WEB_ORDER {
        string OrderID PK
        string CustomerID FK
        string OrderStatus "e.g., Pending, Picked, Collected"
        datetime OrderDate
        string CollectionStore_FK
    }

    INVENTORY {
        string SKUID PK
        string StoreID FK
        int QuantityAvailable "Walk-in stock"
        int QuantityReserved "BOPIS stock"
    }

    STORE {
        string StoreID PK
        string LocationName
        string ManagerEmail
    }

    POS_SYSTEM {
        string RegisterID PK
        string StoreID FK
        boolean IsOnline
    }
