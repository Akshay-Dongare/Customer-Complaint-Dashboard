# Customer-Complaint-Dashboard
BI mini project
## Group Members 
1. BC218 Akshay Dongare
2. BC223 Jaydatta Patwe
3. BC213 Yash Dagadkhair
## Steps to run 
Upload dataset csv file (`customer_support_tickets.csv`) and PowerBI file (`report.pbix`) to PowerBI Desktop Application
## Flowchart
```mermaid
graph TD;
    Customer-Raises-Ticket-->Ticket-Logged-In-Database;
    Ticket-Logged-In-Database-->Change-Detected-By-PowerBI-Dashboard;
    Change-Detected-By-PowerBI-Dashboard-->Visualization_Updated;

```

## DFD
```mermaid
graph TD
    subgraph Customer
        C[Customer]
    end
    subgraph HelpDesk
        T[Ticket Logging System]
    end
    subgraph DataWarehouse
        D[Data Warehouse]
    end
    subgraph Monitoring
        P[PowerBI Dashboard]
        V[Visualization]
    end
    C-->|Raises Ticket|T
    T-->|Logs Ticket|D
    D-->|Change Detected|P
    P-->|Updates|V

    classDef boxStyle fill:#F2F2F2,stroke:#333,stroke-width:2px;
    class C,T,D,P,V boxStyle;
```
