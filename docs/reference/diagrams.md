# Diagrams

DocsForge integrates [Mermaid.js](https://mermaid.js.org) for creating diagrams with text.

## Configuration

Mermaid support is enabled by default:

``` yaml
markdown_extensions:
  - pymdownx.superfences:
      custom_fences:
        - name: mermaid
          class: mermaid
          format: !!python/name:pymdownx.superfences.fence_code_format
```

## Flowchart

``` markdown
``` mermaid
graph LR
    A[Start] --> B{Is it?}
    B -->|Yes| C[OK]
    C --> D[Rethink]
    D --> B
    B ---->|No| E[End]
```
```

``` mermaid
graph LR
    A[Start] --> B{Is it?}
    B -->|Yes| C[OK]
    C --> D[Rethink]
    D --> B
    B ---->|No| E[End]
```

## Sequence diagram

``` markdown
``` mermaid
sequenceDiagram
    participant User
    participant DocsForge
    participant GitHub
    
    User->>DocsForge: Write documentation
    User->>DocsForge: Run build
    DocsForge-->>User: Static site
    User->>GitHub: git push
    GitHub-->>User: Deployed site
```
```

``` mermaid
sequenceDiagram
    participant User
    participant DocsForge
    participant GitHub
    
    User->>DocsForge: Write documentation
    User->>DocsForge: Run build
    DocsForge-->>User: Static site
    User->>GitHub: git push
    GitHub-->>User: Deployed site
```

## Class diagram

``` markdown
``` mermaid
classDiagram
    class Site {
        +String name
        +String url
        +build()
        +serve()
    }
    class Theme {
        +String name
        +configure()
    }
    Site --> Theme : uses
```
```

``` mermaid
classDiagram
    class Site {
        +String name
        +String url
        +build()
        +serve()
    }
    class Theme {
        +String name
        +configure()
    }
    Site --> Theme : uses
```

## State diagram

``` markdown
``` mermaid
stateDiagram-v2
    [*] --> Draft
    Draft --> Review: Submit
    Review --> Published: Approve
    Review --> Draft: Reject
    Published --> [*]
```
```

``` mermaid
stateDiagram-v2
    [*] --> Draft
    Draft --> Review: Submit
    Review --> Published: Approve
    Review --> Draft: Reject
    Published --> [*]
```

## Gantt chart

``` markdown
``` mermaid
gantt
    title DocsForge Roadmap
    dateFormat  YYYY-MM-DD
    section Q1
    Core features    :done, a1, 2025-01-01, 2025-02-28
    Testing          :active, a2, 2025-03-01, 2025-03-31
    section Q2
    Release          :a3, 2025-04-01, 2025-04-30
    Documentation    :a4, 2025-05-01, 2025-06-30
```
```

``` mermaid
gantt
    title DocsForge Roadmap
    dateFormat  YYYY-MM-DD
    section Q1
    Core features    :done, a1, 2025-01-01, 2025-02-28
    Testing          :active, a2, 2025-03-01, 2025-03-31
    section Q2
    Release          :a3, 2025-04-01, 2025-04-30
    Documentation    :a4, 2025-05-01, 2025-06-30
```

## Pie chart

``` markdown
``` mermaid
pie title Distribution
    "Documentation" : 40
    "Code" : 35
    "Tests" : 20
    "Config" : 5
```
```

``` mermaid
pie title Distribution
    "Documentation" : 40
    "Code" : 35
    "Tests" : 20
    "Config" : 5
```

## Git graph

``` markdown
``` mermaid
gitGraph
    commit
    branch develop
    checkout develop
    commit
    commit
    checkout main
    merge develop
    commit
```
```

``` mermaid
gitGraph
    commit
    branch develop
    checkout develop
    commit
    commit
    checkout main
    merge develop
    commit
```

## Mindmap

``` markdown
``` mermaid
mindmap
  root((DocsForge))
    Getting Started
      Installation
      Quick Start
    Setup
      Colors
      Fonts
      Navigation
    Reference
      Admonitions
      Code Blocks
      Diagrams
```
```

``` mermaid
mindmap
  root((DocsForge))
    Getting Started
      Installation
      Quick Start
    Setup
      Colors
      Fonts
      Navigation
    Reference
      Admonitions
      Code Blocks
      Diagrams
```

## Next steps

- [Data tables](data-tables.md)
- [Formatting](formatting.md)
