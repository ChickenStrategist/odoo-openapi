# Odoo API

OpenAPI 3.0 specification for Odoo API integration.

## Usage

### Import into Automation Platforms

Upload `openapi.json` to your automation platform's custom integration feature.

### Import into API Testing Tools

- **Postman**: Import > Link > Paste raw GitHub URL
- **Insomnia**: Import > URL > Paste raw GitHub URL
- **OpenAPI Generator**: `openapi-generator-cli generate -i openapi.json`

### Generate Client Libraries

```bash
# Python
openapi-generator-cli generate -i openapi.json -g python -o ./client-python

# JavaScript
openapi-generator-cli generate -i openapi.json -g javascript -o ./client-js

# PowerShell
openapi-generator-cli generate -i openapi.json -g powershell -o ./client-powershell
```

## Repository Structure

```
.
├── openapi.json              # OpenAPI 3.0 specification
├── README.md
└── LICENSE
```

## Contributing

Contributions welcome! Please submit a pull request.

## Author

Created by [Jake Pantano](https://github.com/ChickenStrategist)

## License

[MIT License](LICENSE)
