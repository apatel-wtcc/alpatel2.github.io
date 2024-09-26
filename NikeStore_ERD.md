erDiagram
    PRODUCT {
        string product_id PK
        string product_name
        float price
        int stock_quantity
    }

    CUSTOMER {
        string customer_id PK
        string customer_name
        string email
        string phone_number
    }

    SALE {
        string sale_id PK
        string customer_id FK
        string product_id FK
        date sale_date
        int quantity
        float total_price
    }

    INVENTORY {
        string product_id PK FK
        int stock_quantity
        date last_updated
    }

    PRODUCT ||--o{ SALE : sells
    CUSTOMER ||--o{ SALE : purchases
    PRODUCT ||--o{ INVENTORY : has
