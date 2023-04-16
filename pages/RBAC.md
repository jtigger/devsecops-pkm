- Notes:
	- In Kubernetes 1.24, Service Account Tokens are no longer automatically generated. Instead,
		- The `LegacyServiceAccountTokenNoAutoGeneration` feature gate is beta, and enabled by default. When enabled, Secret API objects containing service account tokens are no longer auto-generated for every ServiceAccount. Use the [TokenRequest](https://kubernetes.io/docs/reference/kubernetes-api/authentication-resources/token-request-v1/) API to acquire service account tokens, or if a non-expiring token is required, create a Secret API object for the token controller to populate with a service account token by following this [guide](https://kubernetes.io/docs/concepts/configuration/secret/#service-account-token-secrets). ([#108309](https://github.com/kubernetes/kubernetes/pull/108309), [@zshihang](https://github.com/zshihang))
		  collapsed:: true
			- src: https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.24.md#urgent-upgrade-notes
			-