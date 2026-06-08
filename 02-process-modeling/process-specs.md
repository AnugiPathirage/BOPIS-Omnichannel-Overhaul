```mermaid
graph TD
    %% Customer Online Journey
    Customer[Customer Places BOPIS Order Online] --> Ecom[E-Commerce Platform]
    Ecom -->|Order Queued| Batch[12-Hour Batch Process Delay]
    Batch --> ERP[Central ERP / Inventory Database]

    %% Physical Store Journey
    WalkIn[Walk-in Customer] --> POS[Store POS System]
    POS -->|Processes Sale| Floor[Shop Floor Rack]

    %% Staff Fulfillment Journey
    Staff[Store Associate] -->|Manually checks| Tablet[Secondary Web Tablet]
    Tablet -->|Reads Web Order| Floor
    Floor -->|Item Already Sold| Cancel[Order Cancelled & Refunded]

    %% The Technical Disconnect
    ERP -.->|Asynchronous 12h Sync| POS

    %% Highlight Bottlenecks in Red
    style Batch fill:#f9d0c4,stroke:#333,stroke-width:2px,color:#900
    style Tablet fill:#f9d0c4,stroke:#333,stroke-width:2px,color:#900
    style Cancel fill:#f9d0c4,stroke:#333,stroke-width:2px,color:#900
