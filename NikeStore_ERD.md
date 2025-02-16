```mermaid
erDiagram

PRODUCT{string ProductID PK
        string Product_Name
        string Supplier_Name
        string Supplier_ID FK
    }   
    INVENTORY{string InventoryID PK
              string ProductID FK
              string Sales_ID FK
              int Quantity}
    PRODUCT ||--o{ SALES:  has
    PRODUCT ||--o{ INVENTORY: supply
    CUSTOMER ||--|{ SALES : makes
    CUSTOMER{string Customer_ID PK
            string Cust_Last_Name
            string Cust_First_Name
            string Cust_Email}
    
    SALES ||--|{INVENTORY: impacts
    SALES{  string Sales_ID PK
            string Product_ID FK
            string Customer_ID FK}
   
```
