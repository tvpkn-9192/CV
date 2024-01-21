```mermaid
   flowchart TD
    A[ProductTestPage] -->|With invalid products| B[ProductSearch]
    B -->|Toggle ShowValidProducts btn| C[ProductSearch]
    A -->|Without invalid products| C[ProductSearch]
    C --> |Click Test btn| D[TestInstanceDialog]
    D --> |Click BeginTest takes to actual testing page| E[TestDataEntry]
    E --> |Enter measurement & press enter| F[Validate measurement]
    F --> |Click Abort btn & enter reason for abort| G[Abort]
    F --> |Complete Test| H[Test Next Serial]
    H --> |Click TestNextSerial btn| D
```





```mermaid
   flowchart TD
    A[ProductTestPage] -->|With invalid products| B(ProductSearch with invalid products)
    B -->|Toggle ShowValidProducts btn| C(ProductSearch with valid products)
    A -->|Without invalid products| C
    C --> |Click Test btn| D(TestInstanceDialog)
    D --> |Click BeginTest takes to actual testing page| E(TestDataEntry)
    E --> |Enter measurement & press enter| F(Validate measurement)
    F --> |Click Abort btn & enter reason for abort| G(Abort)
    F --> |Complete Test| H(Test Next Serial)
    H --> |Click TestNextSerial btn| D
```




```mermaid
   flowchart TD
    A[ProductTestPage] -->|With invalid products| B(Invalid products)
    B -->|Toggle ShowValidProducts btn| C(Valid products)
    A -->|Without invalid products| C(Valid products)
    C --> |Click Test btn| D(TestInstanceDialog)
    D --> |Click BeginTest btn| E(TestDataEntry)
    E --> |Enter measurement & press enter| F(Validate measurement)
    F --> |Click Abort btn| G(Abort)
    F --> |Complete Test| H(Test Next Serial)
    H --> |Click TestNextSerial btn| D
    G --> |Enter reason for abort, Click Abort btn & Click on ProductSearch at top left| A
```
