```mermaid
erDiagram 
    PRODUCT ||--o{ CUSTOMER : has
    PRODUCT ||--o{ SALES:  has
    PRODUCT ||--o{ INVENTORY: supply
    CUSTOMER ||--|{ SALES : makes
    SALES ||--|{INVENTORY: reduces
```
