# Tool Documentation Schema

This document defines the standardized schema for documenting tools in the Open Source Security Catalog.

## Schema Overview

Each tool should be documented as a YAML file following this schema. The schema ensures consistency across all tool entries and enables automated processing and integration.

## Required Fields

### Basic Information
- `name`: Tool name (string)
- `category`: Primary category (string) - must match one of the defined categories
- `secondary_categories`: Additional categories (array of strings) - optional, for tools spanning multiple domains
- `description`: Brief description of the tool's purpose and capabilities (string)
- `project_url`: Primary project URL (string)
- `license`: License type (string)

### Capabilities
- `capabilities`: List of key features and capabilities (array of strings)

## Optional Fields

### Documentation & Resources
- `documentation_url`: Link to official documentation (string)
- `github_url`: GitHub repository URL (string)
- `docker_url`: Docker Hub or container registry URL (string)

### Deployment Information
- `deployment`: Deployment configuration details (object)
  - `compatible_envs`: Supported environments (array of strings)
  - `helm_chart`: Helm chart URL if available (string)
  - `docker_compose`: Docker Compose file URL if available (string)
  - `ansible_playbook`: Ansible playbook URL if available (string)

### Integration Examples
- `integration_examples`: Real-world usage examples (array of objects)
  - `name`: Example name (string)
  - `description`: Description of the integration (string)
  - `url`: Link to example or documentation (string)

### Metadata
- `tags`: Relevant tags for categorization and search (array of strings)
- `maintainers`: List of maintainers or organizations (array of strings)
- `last_updated`: Last update date (string, YYYY-MM-DD format)
- `version`: Current version (string)

## Category Definitions

Tools must be categorized into one of these predefined categories:

- `endpoint-detection`: Endpoint Detection & Response (EDR), agent-based monitoring
- `siem-platform`: Security Information and Event Management platforms
- `infrastructure-security`: Infrastructure as Code scanning, compliance, hardening
- `cloud-security`: Cloud-specific security tools for AWS, Azure, GCP, and multi-cloud environments
- `threat-intelligence`: Threat feeds, IOC management, intelligence platforms
- `network-security`: Network monitoring, intrusion detection, traffic analysis
- `vulnerability-management`: Vulnerability scanning, assessment, remediation
- `digital-forensics`: Incident response, forensics, memory analysis
- `identity-access`: Authentication, authorization, identity management
- `secrets-management`: Secret scanning, vault solutions, credential management
- `email-security`: Email filtering, anti-spam, secure email gateways
- `compliance`: Compliance frameworks, audit trails, reporting

## Example Schema

```yaml
name: Wazuh
category: endpoint-detection
secondary_categories:
  - siem-platform
description: >
  Open-source unified SIEM and XDR platform for threat detection, visibility, and compliance.
  Provides comprehensive security monitoring across endpoints, cloud workloads, and containers
  with real-time threat detection and automated incident response capabilities.
capabilities:
  - Endpoint Detection and Response (EDR)
  - Security Information and Event Management (SIEM)
  - File integrity monitoring
  - Log analysis and correlation
  - Intrusion detection
  - Vulnerability detection
  - Compliance monitoring
  - Incident response
project_url: https://github.com/wazuh/wazuh
documentation_url: https://documentation.wazuh.com/
github_url: https://github.com/wazuh/wazuh
license: GPL-2.0
deployment:
  compatible_envs:
    - AWS
    - Azure
    - GCP
    - Kubernetes
    - On-premises
  helm_chart: https://github.com/wazuh/wazuh-helm
  docker_compose: https://github.com/wazuh/wazuh-docker
integration_examples:
  - name: Kubernetes Monitoring
    description: Deploy Wazuh agents as DaemonSets to monitor Kubernetes workloads
    url: https://documentation.wazuh.com/current/deployment-options/kubernetes-deployment.html
  - name: AWS CloudTrail Integration
    description: Monitor AWS CloudTrail logs for security events
    url: https://documentation.wazuh.com/current/amazon/index.html
tags:
  - SIEM
  - Agent-based
  - Elastic Stack
  - Compliance
  - Log Analysis
maintainers:
  - Wazuh Inc.
last_updated: 2024-01-15
version: "4.8.0"
```

## Validation Rules

1. **Required fields** must be present and non-empty
2. **Category** must match one of the predefined categories exactly
3. **URLs** must be valid HTTP/HTTPS URLs
4. **Tags** should be lowercase and use hyphens for multi-word tags
5. **Capabilities** should be concise but descriptive
6. **Description** should be 2-3 sentences maximum

## File Naming Convention

Tool files should be named using lowercase with hyphens, matching the tool's common name:
- `wazuh.yaml`
- `osquery.yaml`
- `crowdsec.yaml`
- `opencti.yaml`

## Schema Versioning

This schema is version 1.0. Future versions will maintain backward compatibility where possible, with deprecated fields marked clearly.
