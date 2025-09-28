# Software Architecture Diagrams with Mermaid

This repository provides a collection of software architecture diagrams generated with Mermaid and assisted by GitHub Copilot in VS Code.

The goal is to offer clear, well-documented, and reusable diagrams that illustrate different possible software architecture styles and patterns. These diagrams can serve as educational material, technical documentation, or reference models for real-world projects.

## Key Features

- Multiple architecture models: monolithic, layered, client-server, microservices, event-driven, serverless, hexagonal, cloud-native, and more.
- Mermaid-based diagrams: human-readable, easy to edit, and integrable into markdown documentation.
- Copilot-assisted generation: prompts and code examples demonstrate how GitHub Copilot can automate and accelerate the creation of architecture diagrams.
- Well-documented examples: every diagram includes comments that explain the roles of components and their interactions.
- Consistency and clarity: components use explicit, descriptive names (e.g., `Web Client`, `API Gateway`, `Authentication Service`, `PostgreSQL Database`).
- Comparison of alternatives: side-by-side visualization of different architectures to highlight trade-offs and design choices.

## Example

```mermaid
flowchart TD
  %% Legend / Title (use legend instead of 'title' for broad compatibility)
  subgraph Legend
    direction TB
    T[Title: Microservices with API Gateway]
  end

    A[Web Client] --> B[API Gateway]
    B --> C[Authentication Service]
    B --> D[Product Catalog Service]
    C --> E[(User Database)]
    D --> F[(Product Database)]

%% Explanation:
%% - The Web Client interacts with the API Gateway.
%% - The API Gateway routes requests to microservices.
%% - The Authentication Service manages secure access.
%% - The Product Catalog Service handles product-related data.
%% - Each service manages its own database (database-per-service pattern).
```

## How to use

- Open this repository with VS Code.
- Ensure you have the recommended extensions installed (see `.vscode/extensions.json`).
- Open any `.md` file and preview Mermaid diagrams:
  - Right-click the editor → "Open Preview"
  - Or use: Ctrl+Shift+V (Windows) for Markdown preview; some Mermaid previews may require the Mermaid extension's preview command.

## Structure

- `diagrams/`: Mermaid diagram files grouped by architecture style
- `prompts/`: Copilot prompt templates to generate/extend diagrams
- `.vscode/`: recommended extensions for better authoring experience

## Diagram Library

- Monolithic: [Traditional Monolithic Application](diagrams/monolith/monolithic-basic.md)
- Layered: [Layered (n-tier) Architecture](diagrams/layered/layered-architecture.md)
- Client-Server: [Client-Server with Reverse Proxy](diagrams/client-server/client-server-basic.md)
- Microservices:
  - [API Gateway with BFFs](diagrams/microservices/api-gateway-bff.md)
  - [Saga Pattern (Orchestration)](diagrams/microservices/saga-orchestration.md)
  - [Saga Pattern (Choreography)](diagrams/microservices/choreography/saga-choreography.md)
- Event-Driven: [Event-Driven Architecture with CQRS](diagrams/event-driven/event-driven-cqrs.md)
- Serverless: [Serverless Web Backend](diagrams/serverless/serverless-web-backend.md)
- Cloud-Native: [Kubernetes with Service Mesh](diagrams/cloud-native/cloud-native-k8s-istio.md)
- Hexagonal: [Ports & Adapters Architecture](diagrams/hexagonal/hexagonal-architecture.md)
- IoT: [IoT Edge-to-Cloud Architecture](diagrams/iot/iot-edge-cloud.md)
- AI / ML: [Machine Learning Pipeline Architecture](diagrams/ai-ml/ml-pipeline.md)
- Data Mesh: [Data Mesh Domain-Oriented Platform](diagrams/data-mesh/data-mesh-domains.md)
- Vertical Slice: [Vertical Slice Architecture](diagrams/vertical-slice/vertical-slice-architecture.md)
- DevOps: [DevOps Reference Architecture](diagrams/devops/devops-reference-architecture.md)

## License

MIT
