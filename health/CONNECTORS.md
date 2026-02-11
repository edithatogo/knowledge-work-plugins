# Health Plugin Connectors

This document describes the connector categories and setup instructions for the health plugin.

## Connector Categories

### Document Storage

Healthcare organizations typically use enterprise document management systems:

| Connector | Use Case | Authentication |
|-----------|----------|----------------|
| SharePoint | Microsoft 365 environments | OAuth 2.0 / Entra ID |
| Box | Cloud content management | OAuth 2.0 / JWT |
| Egnyte | Hybrid cloud storage | OAuth 2.0 / API Key |
| Google Drive | Google Workspace | OAuth 2.0 |

### Issue Tracking

For complaint management, incident tracking, and workflow automation:

| Connector | Use Case | Authentication |
|-----------|----------|----------------|
| Jira | IT service management | API Token / OAuth |
| ServiceNow | Enterprise service management | OAuth 2.0 / Basic |
| Azure DevOps | Development tracking | PAT / OAuth |

### Clinical Systems

Integration points for clinical data (organization-specific):

| Connector | Use Case | Authentication |
|-----------|----------|----------------|
| Epic FHIR | EHR data access | OAuth 2.0 / SMART |
| Cerner | EHR integration | OAuth 2.0 / API Key |
| Custom APIs | Organization systems | Varies |

## Setup Instructions

### 1. Document Storage (SharePoint Example)

```json
{
  "mcpServers": {
    "sharepoint": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-sharepoint"],
      "env": {
        "SHAREPOINT_TENANT": "your-tenant.sharepoint.com",
        "SHAREPOINT_CLIENT_ID": "${SHAREPOINT_CLIENT_ID}",
        "SHAREPOINT_CLIENT_SECRET": "${SHAREPOINT_CLIENT_SECRET}"
      }
    }
  }
}
```

### 2. Issue Tracking (Jira Example)

```json
{
  "mcpServers": {
    "jira": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-jira"],
      "env": {
        "JIRA_BASE_URL": "https://your-org.atlassian.net",
        "JIRA_EMAIL": "${JIRA_EMAIL}",
        "JIRA_API_TOKEN": "${JIRA_API_TOKEN}"
      }
    }
  }
}
```

### 3. Clinical Systems (FHIR Example)

```json
{
  "mcpServers": {
    "fhir": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-fhir"],
      "env": {
        "FHIR_BASE_URL": "https://fhir.your-org.com/r4",
        "FHIR_CLIENT_ID": "${FHIR_CLIENT_ID}",
        "FHIR_CLIENT_SECRET": "${FHIR_CLIENT_SECRET}"
      }
    }
  }
}
```

## Authentication Best Practices

1. **Never commit credentials** - Use environment variables
2. **Use service accounts** - Dedicated accounts for automation
3. **Rotate credentials** - Regular key rotation schedule
4. **Least privilege** - Grant minimum required permissions
5. **Audit access** - Enable logging for compliance

## Troubleshooting

### Common Issues

| Issue | Solution |
|-------|----------|
| Authentication failed | Verify credentials and token expiration |
| Permission denied | Check OAuth scopes and API permissions |
| Connection timeout | Verify network access and firewall rules |
| Rate limiting | Implement backoff and retry logic |

### Getting Help

1. Check connector documentation
2. Review MCP server logs
3. Contact your IT security team for access issues
