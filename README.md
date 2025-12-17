# Azure Architecture Examples

A comprehensive collection of Azure architecture patterns, demos, and reference implementations demonstrating real-world scenarios. This repository focuses on cloud-native design principles, security best practices, scalability patterns, and operational excellence.

## 🎯 Overview

This repository serves as a practical learning resource for architects, developers, and DevOps engineers looking to build production-ready solutions on Azure. Each example includes infrastructure-as-code, application code, and detailed documentation explaining the architectural decisions and trade-offs.

## 📚 Learning Goals

By exploring these examples, you will learn:

- **Cloud-Native Architecture**: Design patterns for building scalable, resilient applications
- **Infrastructure as Code**: Automate Azure infrastructure deployment using Bicep
- **Security Best Practices**: Implement Azure security features and compliance requirements
- **Observability**: Monitor, log, and troubleshoot distributed systems
- **Cost Optimization**: Design cost-effective solutions without compromising performance
- **DevOps Practices**: CI/CD pipelines, testing strategies, and deployment automation
- **Microservices Patterns**: Service communication, data management, and resilience
- **Serverless Computing**: Build event-driven architectures with Azure Functions

## 🏗️ Use Cases

This repository covers common Azure architecture patterns including:

### Web Applications
- **Multi-tier Web Apps**: Scalable web applications with Azure App Service, Azure SQL, and Azure Front Door
- **Static Web Apps**: Modern JAMstack applications with Blazor WebAssembly and Azure Static Web Apps
- **Microservices**: Containerized services with Azure Kubernetes Service (AKS) or Azure Container Apps

### Data & Analytics
- **Real-time Analytics**: Stream processing with Azure Event Hubs and Azure Stream Analytics
- **Data Warehousing**: Modern data platforms with Azure Synapse Analytics
- **Data Lake**: Scalable data storage with Azure Data Lake Storage Gen2

### Integration & Messaging
- **Event-Driven Architecture**: Asynchronous messaging with Azure Service Bus and Event Grid
- **API Management**: Centralized API gateway with Azure API Management
- **Enterprise Integration**: B2B and B2C scenarios with Azure Logic Apps

### AI & Machine Learning
- **ML Operations**: Deploy and manage machine learning models with Azure ML
- **Cognitive Services**: Integrate AI capabilities like vision, speech, and language

### Security & Identity
- **Zero Trust Architecture**: Identity-based security with Azure AD and Managed Identities
- **Network Security**: Hub-spoke topology with Azure Firewall and Application Gateway
- **Data Protection**: Encryption, Key Vault integration, and compliance

## 📁 Repository Structure

```
azure-architecture-examples/
├── infra/                  # Infrastructure as Code (Bicep)
│   ├── modules/           # Reusable Bicep modules
│   ├── environments/      # Environment-specific configurations
│   └── main.bicep        # Main infrastructure template
├── src/                   # Application Source Code
│   ├── .NET/             # .NET applications
│   ├── Blazor/           # Blazor web applications
│   └── shared/           # Shared libraries and utilities
├── docs/                  # Documentation
│   ├── architecture/     # Architecture diagrams and ADRs
│   ├── guides/           # Step-by-step implementation guides
│   └── best-practices/   # Azure best practices
├── .github/              # GitHub Actions workflows
└── README.md             # This file
```

## 🚀 Getting Started

### Prerequisites

- [Azure Subscription](https://azure.microsoft.com/free/)
- [Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli) (v2.40+)
- [.NET SDK](https://dotnet.microsoft.com/download) (v8.0+)
- [Bicep](https://learn.microsoft.com/azure/azure-resource-manager/bicep/install) (latest)
- [Visual Studio Code](https://code.visualstudio.com/) or [Visual Studio](https://visualstudio.microsoft.com/)

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/DavidTroska/azure-architecture-examples.git
   cd azure-architecture-examples
   ```

2. **Login to Azure**
   ```bash
   az login
   az account set --subscription <your-subscription-id>
   ```

3. **Deploy Infrastructure**
   ```bash
   cd infra
   az deployment group create \
     --resource-group <your-resource-group> \
     --template-file main.bicep \
     --parameters @environments/dev.parameters.json
   ```

4. **Build and Run Applications**
   ```bash
   cd src/<example-app>
   dotnet restore
   dotnet build
   dotnet run
   ```

5. **Explore Documentation**
   Browse the `docs/` directory for architecture diagrams, implementation guides, and best practices.

## 🔧 Development Workflow

1. **Infrastructure First**: Deploy Azure resources using Bicep templates
2. **Application Development**: Build applications using the deployed infrastructure
3. **Testing**: Run unit, integration, and end-to-end tests
4. **Monitoring**: Configure Application Insights and Azure Monitor
5. **Deployment**: Use CI/CD pipelines for automated deployments

## 📖 Documentation

- [Architecture Overview](docs/architecture/README.md)
- [Bicep Infrastructure Guide](infra/README.md)
- [Application Development Guide](src/README.md)
- [Best Practices](docs/best-practices/README.md)

## 🤝 Contributing

Contributions are welcome! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-pattern`)
3. Commit your changes (`git commit -m 'Add amazing architecture pattern'`)
4. Push to the branch (`git push origin feature/amazing-pattern`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🌟 Additional Resources

- [Azure Architecture Center](https://learn.microsoft.com/azure/architecture/)
- [Azure Well-Architected Framework](https://learn.microsoft.com/azure/architecture/framework/)
- [Azure Bicep Documentation](https://learn.microsoft.com/azure/azure-resource-manager/bicep/)
- [.NET on Azure](https://learn.microsoft.com/dotnet/azure/)

## 📧 Contact

For questions, feedback, or discussions, please open an issue in this repository.

---

**Built with ❤️ for the Azure community**
