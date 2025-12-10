flowchart TD
    FE[Frontend] --> GW[API Gateway]

    GW --> AUTH[AuthService]

    AUTH --> DS[DriversService]
    AUTH --> VS[VehiclesService]
    AUTH --> RS[RoutesService]

    subgraph Microservices
        DS
        VS
        RS
    end

    Microservices --> FS[FuelService]
