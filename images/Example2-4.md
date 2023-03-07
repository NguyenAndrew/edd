```mermaid
graph LR
    style A fill:#A9A9A9,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style B fill:#A9A9A9,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style C fill:#fff,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style D fill:#fff,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style E fill:#fff,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    A[Make a program that plays any song from a spreadsheet]
    B[Convert a song into CSV]
    C[Play CSV]
    D[Provide a WAV File]
    E[Convert WAV to CSV]
    A --> B
    A --> C
    B --> D
    B --> E
```