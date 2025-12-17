# Infrastructure as Code (Bicep)

This directory contains Azure Infrastructure as Code templates using Bicep.

## Structure

- `modules/` - Reusable Bicep modules
- `environments/` - Environment-specific deployments (dev, staging, prod)
- `main.bicep` - Main infrastructure template

## Getting Started

To deploy the infrastructure:

```bash
az deployment group create \
  --resource-group <your-rg> \
  --template-file main.bicep
```

## Best Practices

- Use modules for reusable components
- Parameterize environment-specific values
- Follow Azure naming conventions
- Document all parameters and outputs
