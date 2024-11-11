📁 **Project File Changes**

This section outlines the modifications made to various project files during the development process. Below is a list of the files that have been updated:

📄 **2_real.md** - Contains updates related to the real-time data processing module.

📄 **3_environments.md** - Includes changes to the environment configuration settings.

📄 **4_ui.md** - Details the adjustments made to the user interface components.

📄 **5_formulas.md** - Lists the new and updated formulas used in the project.

📄 **6_Symbols.md** - Documents the changes to the symbol definitions.

📄 **7_Semblance.md** - Describes the updates to the semblance analysis algorithms.

📄 **README.md** - Provides an overview of the project and the recent changes.


Here’s a Mermaid chart for the system architecture based on the provided requirements:

```mermaid
```mermaid
flowchart TD
    %% On-Premises / Clinic Site
    subgraph On-Premises
        A1[IoT Edge Devices]:::device
        A2[IoT Gateway]:::device
        A1 --> A2
    end

    %% Azure Cloud
    subgraph Azure Cloud
        A2 --> B1[Azure IoT Hub]:::cloud
        B1 --> B2[Azure Stream Analytics]:::cloud
        B1 --> B3[Device Management]:::cloud
        B1 --> B4[Security & Authentication]:::cloud
    end

    %% Data Storage
    subgraph Data Storage
        B2 --> C1[Azure Data Lake / Cosmos DB / SQL Database]:::storage
        C1 --> C2[Data Retention & Compliance]:::storage
    end

    %% Processing and Analytics
    subgraph Processing and Analytics
        B2 --> D1[Azure Functions]:::processing
        D1 --> D2[Order Management System]:::processing
        C1 --> E1[Power BI / Synapse Analytics]:::processing
    end

    %% Monitoring and Alerts
    subgraph Monitoring and Alerts
        B1 --> F1[Azure Monitor]:::monitoring
        F1 --> F2[Real-Time Alerts for Medical Staff]:::monitoring
    end

    %% API Management
    subgraph API Management
        E1 --> G1[Azure API Management]:::api
        G1 --> G2[External Systems / Patient Portals]:::api
    end

    %% Security and Compliance Layer
    subgraph Security and Compliance
        C1 --> H1[Azure Active Directory]:::security
        C1 --> H2[Azure Policy - HIPAA / GDPR Compliance]:::security
    end

    %% Diagram Annotations
    classDef device fill:#EFEFEF,stroke:#333,stroke-width:2px;
    classDef cloud fill:#D0E1F9,stroke:#333,stroke-width:2px;
    classDef storage fill:#F9E79F,stroke:#333,stroke-width:2px;
    classDef processing fill:#A9DFBF,stroke:#333,stroke-width:2px;
    classDef monitoring fill:#F5B7B1,stroke:#333,stroke-width:2px;
    classDef api fill:#D7BDE2,stroke:#333,stroke-width:2px;
    classDef security fill:#FAD7A0,stroke:#333,stroke-width:2px;
```
```

### Explanation

- **On-Premises (Clinic Site)**: IoT Edge Devices push data to the IoT Gateway, which connects to Azure.
- **Azure Cloud**: IoT Hub ingests data, processes it with Stream Analytics, and uses device management for upkeep.
- **Data Storage**: Raw and processed data is stored in Azure Data Lake, Cosmos DB, and SQL Database.
- **Processing and Analytics**: Azure Functions automate tasks, and Power BI/Synapse Analytics visualize data for insights.
- **Monitoring and Alerts**: Azure Monitor tracks system health and triggers real-time alerts.
- **API Management**: Manages API access for secure integration with external systems.
- **Security and Compliance Layer**: Azure AD manages access, and Azure Policy ensures compliance with regulations like HIPAA and GDPR. 

This layout provides a comprehensive view for a buildable, scalable architecture.