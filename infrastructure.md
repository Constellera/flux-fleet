# Infrastructure

Documentation about the cluster global infrastructure configurations.

## Traefik

The default Traefik traffic manager installed by k3s via helm chart needs to be modified via a `HelmChartConfig` object to enable the more modern Kubernetes Gateway API for managing ingress traffic and configure additional entry points used by applications.

Additionally, it should be mentioned that enabling the Gateway API and the experimental channels in the Helm values does not automatically install the extended Custom Resource Definitions, so they need to be configured here as well. Rest assured the Traefik Gateway Class is configured and deployed automatically when enabled in the Helm chart.

