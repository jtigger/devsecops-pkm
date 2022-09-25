title:: Infrastructure for Apps: Cooperative Delivery

- a [[CNCF App Delivery TAG]] White Paper
- https://docs.google.com/document/d/1RgKFYRX4jhJCH9q_2wDMogctwU2AYAZZRHUCKBJpHkg/edit
- Raw Notes
	- People are seeing real benefits from [[GitOps]] and [[Infrastructure as Code]]
	- but there's a gap between those delivering apps and those delivering "infrastructure capabilities"
- Questions I had:
  collapsed:: true
	- Where does the development experience fit in to all this?
	-
- Projects Mentioned
  collapsed:: true
	- Backstage
		- From Spotify
		- A platform for building "Developer Portal"s
			- units of JavaScript/TypeScript "packages" that either provide a UI, a backend integration, and/or proxy to 3rd party services
		- "Single Pane of Glass" for Developers
	- Crossplane
		- Create/Manage infrastructure pieces by creating instances of CRDs
			- like GCP Config Connector, but vendor-neutral
	- Dapr
		- Distributed APplication Runtime
		- a sidecar that proxies common distributed systems interactions
			- pub/sub
			- service req/res
			- state management
		- apps generate Dapr "events" that get turned into API calls.
	- KubeVela
		- Alibaba Cloud
		- Two parts:
			- An abstraction (specifically the Open Application Model) that describes the application
			- A Continuous Delivery Platform that takes that OAM and "orchestrates" the deployment of it.
	-
		-