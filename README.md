# go-weather-app
Simple go weather app

```
go-weather-app/                     
├── src/        
│   ├── application/                    # This folder can contain application-wide configurations and settings.
│   │   └── config.go       
│   ├── entry_points/                   # This folder can contain modules that serve as entry points to your application.
│   │   └── main.go     
│   ├── utils/                          # This folder can hold utility functions and helper modules.
│   │   ├── helpers.go      
│   │   └── decorators.go       
│   └── domain/     
│       ├── aggregates/                 # Aggregates encapsulate multiple related entities and value objects into a single unit.
│       │   ├── weather.go
│       │   └── widget.go
│       ├── repositories/               # This subfolder contains interfaces that define the contract for accessing and managing your domain aggregates.
│       │   ├── weather_repository.go
│       │   └── widget_repository.go
│       ├── services/                   # Domain services encapsulate domain logic that doesn't naturally fit within an aggregate or entity.
│       │   ├── weather_service.go
│       │   └── widget_service.go
│       └──  value_objects/             # This subfolder contains modules that define value objects.
│           ├── temperature.go
│           ├── weather_condition.go
│           ├── wind_speed.go
│           ├── precipitation.go
│           └── widget.go
└── infrastructure/     
    ├── persistence/                    # This subfolder deals with the technical details of how your application's data is stored and retrieved.
    │   ├── database.go
    │   ├── repositories/               # This subfolder contains modules that define the repository interfaces, which represent a module that handles data access and storage.
    │   │   ├── weather_repository.go
    │   │   └── widget_repository.go
    └── external_services/              # This subfolder can contain modules that interact with external services like payment gateways, notification services, etc.   
        └── weather_api.go
```