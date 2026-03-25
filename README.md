# Nitro MCP Validate

A GitHub Action that validates MCP feature collections against the Nitro registry.

## Usage

```yaml
- uses: ChilliCream/nitro-mcp-validate@v16
  with:
    stage: <stage>
    mcp-feature-collection-id: <mcp-feature-collection-id>
    api-key: <api-key>
    # Optional
    tool-patterns:
      - ./mcp/tools/**/*.graphql
    prompt-patterns:
      - ./mcp/prompts/**/*.json
    cloud-url: <cloud-url>
```

## Inputs

| Name                        | Required | Description                                                     |
| --------------------------- | -------- | --------------------------------------------------------------- |
| `stage`                     | Yes      | The name of the stage                                           |
| `mcp-feature-collection-id` | Yes      | The ID of the MCP Feature Collection                            |
| `api-key`                   | Yes      | API key for authentication                                      |
| `tool-patterns`             | No       | One or more file patterns to locate MCP tool definition files   |
| `prompt-patterns`           | No       | One or more file patterns to locate MCP prompt definition files |
| `cloud-url`                 | No       | The URL of the Nitro registry                                   |

At least one of `prompt-patterns` or `tool-patterns` should be provided.

If you self-host Nitro or use a dedicated hosted instance, you can specify the `cloud-url` input to point to your instance.
