


### 1. **Diagramas de flujo (Flowcharts)**
- **Dirección de arriba a abajo** (`TB`)
- **Dirección de izquierda a derecha** (`LR`)
- **Dirección de derecha a izquierda** (`RL`)
- **Dirección de abajo hacia arriba** (`BT`)

```mermaid
graph TB
    A[Start] --> B{Decision}
    B -->|Yes| C[Option 1]
    B -->|No| D[Option 2]
```

### 2. **Diagramas de Gantt (Gantt charts)**
- Representación de cronogramas de proyectos con tiempos, dependencias y tareas.

```mermaid
gantt
    title Project Plan
    dateFormat  YYYY-MM-DD
    section Phase 1
    Task A           :a1, 2024-09-01, 10d
    Task B           :after a1  , 5d
```

### 3. **Diagramas de Clases UML (UML Class Diagrams)**
- Representa clases y sus relaciones en un sistema orientado a objetos.

```mermaid
classDiagram
    class Animal {
      +String name
      +int age
      +makeSound()
    }
    class Dog {
      +String breed
      +bark()
    }
    Animal <|-- Dog
```

### 4. **Diagramas de Secuencia (Sequence Diagrams)**
- Muestra la interacción entre actores o componentes a lo largo del tiempo.

```mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>Bob: Hello Bob, how are you?
    Bob-->>Alice: I am fine, thanks!
```

### 5. **Diagramas de Estado (State Diagrams)**
- Representa los diferentes estados de un objeto o sistema y las transiciones entre ellos.

```mermaid
stateDiagram
    [*] --> Inactive
    Inactive --> Active : Event
    Active --> Inactive : Timeout
```

### 6. **Diagramas de Entidad-Relación (ERD)**
- Modela las relaciones entre diferentes entidades en un sistema.

```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER {
      string name
      string address
    }
```

### 7. **Gráficos de Red (Network Diagrams)**
- Muestra redes de nodos interconectados.

```mermaid
graph LR
    A --- B
    B-->C[fa:fa-car Car]
    B-->D(fa:fa-cog Settings)
```

### 8. **Diagramas de Matriz de Viajes (User Journey Diagrams)**
- Ilustra el viaje del usuario a través de diferentes fases o estados.

```mermaid
journey
    title User Journey
    section Checkout
      Buy item: 5: User
      Confirm order: 3: User
      Payment: 2: User
```

### 9. **Gráficos de Tarta (Pie Charts)**
- Representa datos proporcionales en forma de gráfica circular.

```mermaid
pie
    title Market Share
    "Product A" : 40
    "Product B" : 30
    "Product C" : 20
    "Product D" : 10
```

### 10. **Diagramas de Tareas (Task Diagrams)**
- Representa tareas y su progreso o estado de completitud.

```mermaid
graph TD
    Task1 --> Task2
    Task2 --> Task3
    Task3 --> TaskComplete[Complete]
```

### 11. **Diagramas de Colaboración (C4 Diagrams)**
- Modela componentes, contenedores y relaciones en sistemas distribuidos o microservicios.

```mermaid
flowchart TB

    subgraph personalBankingCustomer[Personal Banking Customer]
        h1[-Person-]:::type
        d1[A customer of the bank, with   personal bank accounts]:::description
    end
    personalBankingCustomer:::person

    subgraph internetBankingSystem[Internet Banking System]
        h2[-Software System-]:::type
        d2[Allows customers to view   information about their bank   banks, and make payments]:::description
    end
    internetBankingSystem:::internalSystem

    subgraph mainframeBankingSystem[Mainfram Banking System]
        h3[-Software System-]:::type
        d3[Stores all of the core banking   information about customers,   accounts, transactions etc]:::description
    end
    mainframeBankingSystem:::externalSystem

    subgraph emailSystem[Email System]
        h4[-Software System-]:::type
        d4[The internal Microsoft Exchange   email system]:::description
    end
    emailSystem:::externalSystem

    personalBankingCustomer--Views account   balances, and   makes payments   using-->internetBankingSystem
    internetBankingSystem--Gets accounts   information from,   and makes   payments using-->mainframeBankingSystem
    internetBankingSystem--Sends emails using--> emailSystem
    emailSystem--Sends emails to-->personalBankingCustomer

%% Element type definitions

    classDef person fill:#08427b
    classDef internalSystem fill:#1168bd
    classDef externalSystem fill:#999999

    classDef type stroke-width:0px, color:#fff, fill:transparent, font-size:12px
    classDef description stroke-width:0px, color:#fff, fill:transparent, font-size:13px
```

### 12. **Diagramas de Tubería (Pipeline Diagrams)**
- Representa el flujo de datos o procesos a través de un pipeline.

```mermaid
graph LR
    A[Input] --> B[Process]
    B --> C[Output]
```

### 13. **Diagramas de Archivos y Carpetas (Git Graph)**
- Muestra visualmente la estructura y relaciones de carpetas y archivos, especialmente útil en proyectos Git.

```mermaid
gitGraph
    commit id: "Inicio del proyecto"
    branch develop
    checkout develop
    commit id: "Desarrollo inicial"
    checkout main
    commit id: "Primera versión"
    merge develop
```

### 14. **Diagramas de Comparación (Quadrant Diagrams)**
- Organiza conceptos o elementos en cuadrantes para comparación según dos criterios.

```mermaid
graph TD
    A["Eje X: Eficiencia"] --> B["Alta"]
    A --> C["Baja"]
    B --> D["Eje Y: Costo Alto"]
    B --> E["Eje Y: Costo Bajo"]
    C --> F["Eje Y: Costo Alto"]
    C --> G["Eje Y: Costo Bajo"]
```

### 15. **Diagramas de Control de Flujo (State Diagrams)**
- Muestra los estados de un sistema o proceso y las transiciones entre esos estados.

```mermaid
stateDiagram-v2
    [*] --> Inactivo
    Inactivo --> Activo : Evento1
    Activo --> Inactivo : Evento2
    Activo --> Finalizado : Evento3
    Finalizado --> [*]
```

### 16. **Diagramas de Requisitos (Requirement Diagrams)**
- Representa las relaciones entre requisitos y los elementos que los cumplen.

```mermaid
    requirementDiagram

    requirement test_req {
        id: 1
        text: the test text.
        risk: high
        verifymethod: test
    }

    element test_entity {
        type: simulation
    }

    test_entity - satisfies -> test_req

```

### 17. **Diagramas de Arquitectura de Software (C4: Container & Component Diagrams)**
- Se centra en la arquitectura de un sistema, modelando los componentes y contenedores.

```mermaid
graph TD
    subgraph "Customer Service"
        c2["API REST API Maneja solicitudes de clientes"]
        c3["Database MySQL Almacena información"]
    end
    c2 --> c4["Customer Customer.java Representa un cliente"]
```


### 18. **Diagramas Con estilo personalizado**
- Se le puede aplicar clases para personalizar el diagrama

```mermaid
flowchart LR
    id1(Start)-->id2{Decision Point}
    id2-->|Positive|id3(Auditoria Final)
    id2-->|Negative|id4(Detenido)
    id4-->id5(Final Alternativo)
    
    style id1 fill:#72B545,stroke:#72B545,stroke-width:2px,stroke-dasharray: 0 0,rx:10,ry:10
    style id2 fill:#FE814F,stroke:#FE814F,stroke-width:2px,rx:10,ry:10
    style id3 fill:#66B2FF,stroke:#F3682D,stroke-width:2px,stroke-dasharray: 5 5,rx:10,ry:10
    style id4 fill:#76CCD9,stroke:#76CCD9,stroke-width:2px,rx:10,ry:10
    style id5 fill:#FFC903,stroke:#FFC903,stroke-width:2px,rx:10,ry:10
```


```mermaid
%% Definición del fondo blanco
flowchart LR
    id1(Start)-->id2{Decision Point}
    id2-->|Positive|id3(Auditoria Final)
    id2-->|Negative|id4(Detenido)
    id4-->id5(Final Alternativo)

    %% Estilos de nodos con colores de borde especificados y texto negro
    style id1 fill:#fff,stroke:#72B545,stroke-width:2px,stroke-dasharray: 0 0,rx:10,ry:10,color:#000
    style id2 fill:#fff,stroke:#FE814F,stroke-width:2px,rx:10,ry:10,color:#000
    style id3 fill:#fff,stroke:#66B2FF,stroke-width:2px,stroke-dasharray: 5 5,rx:10,ry:10,color:#000
    style id4 fill:#fff,stroke:#76CCD9,stroke-width:2px,rx:10,ry:10,color:#000
    style id5 fill:#fff,stroke:#FFC903,stroke-width:2px,rx:10,ry:10,color:#000

```

```mermaid
flowchart LR
    id1(Start)-->id2{Decision Point}
    id2-->|Positive|id3(Auditoria Final)
    id2-->|Negative|id4(Detenido)
    id4-->id5(Final Alternativo)

    %% Estilos de nodos con colores de borde, texto negro y fondo claro
    style id1 fill:#D4E4D2,stroke:#72B545,stroke-width:2px,stroke-dasharray: 0 0,rx:10,ry:10,color:#000
    style id2 fill:#FAD2B2,stroke:#FE814F,stroke-width:2px,rx:10,ry:10,color:#000
    style id3 fill:#D0E1FF,stroke:#66B2FF,stroke-width:2px,stroke-dasharray: 5 5,rx:10,ry:10,color:#000
    style id4 fill:#E4F1F9,stroke:#76CCD9,stroke-width:2px,rx:10,ry:10,color:#000
    style id5 fill:#FDF6E4,stroke:#FFC903,stroke-width:2px,rx:10,ry:10,color:#000
```
