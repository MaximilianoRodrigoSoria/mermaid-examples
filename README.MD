


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
C4Component
Container_Boundary(c1, "Customer Service") {
    Component(c2, "API", "REST API")
    Component(c3, "Database", "MySQL")
}
c2 --> c3 : Reads/Writes Data
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
    requirement R1 {
        id: 1
        text: "El sistema debe permitir a los usuarios autenticarse"
    }
    testCase T1 {
        id: 101
        description: "Verificar autenticación correcta"
    }
    R1 -- T1
```

### 17. **Diagramas de Arquitectura de Software (C4: Container & Component Diagrams)**
- Se centra en la arquitectura de un sistema, modelando los componentes y contenedores.

```mermaid
graph TD
    subgraph "Customer Service"
        c2["API\nREST API\nManeja solicitudes de clientes"]
        c3["Database\nMySQL\nAlmacena información"]
    end
    c2 --> c3:\"Operaciones%.20CRUD\"
```