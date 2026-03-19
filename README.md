### Diagrama de Escolha de Endereço

```mermaid
sequenceDiagram
 participant U as Usuário
 participant A as APP (FrontEnd)
 participant B as Backend
 participant D as Bancos de dados

 U->>A: Clica em "Escolher Endereço"
 A->>B: Solicita endereços (latitude/longitude atual)
 B->>D: Consulta endereços cadastrados
 D-->>B: Retorna lista de endereços
 Note over B: Calcula distâncias em KM
 B-->>A: Retorna lista de endereços + distâncias
 A-->>U: Exibe listas de endereços com KM
