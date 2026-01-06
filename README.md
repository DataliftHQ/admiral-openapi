# admiral-openapi

OpenAPI specifications for the Admiral API. Use these specs to generate HTTP clients, explore endpoints, or integrate with API tooling.

## Documentation

[View Interactive API Docs](https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/DataliftHQ/admiral-openapi/master/openapi.v3.yaml)

## Files

| File | Version |
|------|---------|
| `openapi.v3.yaml` | OpenAPI 3.1 |
| `openapi.swagger.yaml` | OpenAPI 2.0 (Swagger) |

## Usage

### Raw URLs

```
https://raw.githubusercontent.com/DataliftHQ/admiral-openapi/master/openapi.v3.yaml
https://raw.githubusercontent.com/DataliftHQ/admiral-openapi/master/openapi.swagger.yaml
```

### Client Generation

**Go (oapi-codegen)** - uses OpenAPI 2.0:

```bash
go install github.com/oapi-codegen/oapi-codegen/v2/cmd/oapi-codegen@latest
oapi-codegen -package api openapi.swagger.yaml > api/client.go
```

**Go (openapi-generator)** - uses OpenAPI 3.1:

```bash
openapi-generator-cli generate -i openapi.v3.yaml -g go -o ./client/go
```

**TypeScript**:

```bash
openapi-generator-cli generate -i openapi.v3.yaml -g typescript-fetch -o ./client/ts
```

**Python**:

```bash
openapi-generator-cli generate -i openapi.v3.yaml -g python -o ./client/python
```

## Feedback

Found an issue or have a suggestion? [Open an issue](https://github.com/DataliftHQ/admiral-community/issues).
