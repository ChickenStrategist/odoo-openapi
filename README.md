# Odoo External API

Official OpenAPI 3.0 specification for Odoo API integration with Rewst.

## Documentation
[Rewst Custom Integration Guide](https://docs.rewst.help/documentation/configuration/integrations/custom-integrations/custom-integrations-v2)

## Specification Details
- **Version**: 18.0
- **Base URL**: `https://{instance}.odoo.com`
- **Authentication**: N/A

## Description
Odoo is an open-source ERP platform that provides external API access via XML-RPC and JSON-RPC. This specification covers the publicly available endpoints for interacting with Odoo models and data.

**Note:** Access to the external API is only available on Custom Odoo pricing plans. Access is not available on One App Free or Standard plans.

## Authentication
Odoo uses either username/password or API keys for authentication. The authenticate method returns a user ID (uid) that must be used in subsequent API calls.

## Common Models
- `res.partner`: Partners (contacts, customers, vendors)
- `sale.order`: Sales orders
- `sale.order.line`: Sales order lines
- `product.product`: Products
- `product.template`: Product templates
- `account.move`: Invoices and journal entries
- `purchase.order`: Purchase orders
- `stock.picking`: Inventory operations
- `res.users`: System users
- `ir.model`: Model metadata
- `ir.model.fields`: Field metadata

## Usage

### Import into Rewst
1. Navigate to: Rewst Dashboard > Configuration > Integrations
2. Create Custom Integration
3. Upload `openapi.json` from this repository
4. Configure authentication parameters
5. Test connection

### Import into API Testing Tools
- **Postman**: Import > Link > Paste raw GitHub URL
- **Insomnia**: Import > URL > Paste raw GitHub URL
- **OpenAPI Generator**: `openapi-generator-cli generate -i openapi.json`

## Repository Structure
```
.
├── openapi.json              # Primary OpenAPI 3.0 specification
├── assets/                   # Integration assets (logos, guides)
├── README.md                 # This file
└── .github/
    └── workflows/
        └── validate-openapi.yml  # CI validation
```

## Validation
This specification is automatically validated on every commit using GitHub Actions.

## Contributing
Maintained by Rewst APAC Automation Team.

## Support
- **Technical Support**: roc@rewst.io
- **Documentation**: [Rewst Docs](https://docs.rewst.help)

## License
Private repository - Rewst LLC internal use only.
