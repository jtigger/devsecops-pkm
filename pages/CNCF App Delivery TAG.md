- Charter:
  id:: 63306602-0365-4873-9e26-9336616d3907
	- [https://github.com/cncf/toc/blob/main/tags/app-delivery.md](https://github.com/cncf/toc/blob/main/tags/app-delivery.md)
		- to write informational guides, tutorials, and whitepapers
		- support the TOC with our deeper know-how of "App Delivery" (developing, distributing, deploying, and managing cloud-native applications)
		- Scope:
		  collapsed:: true
			- Application definition, including description, parameter and configuration
			- Guidance and practice for application design and development
				- was: 12 Factor Apps
			- Application bundling and deployment
				-
			- Package management
				- i.e. versioning and dependencies
			- Application delivery workflow and strategy
			- Configuration source driven workflow
				- aka GitOps?
			- Release management
- Projects that fall under this TAG's focus:
  id:: 2131995b-952b-47f6-8f80-7c5c662fec99
  collapsed:: true
	- Brigade
	  collapsed:: true
		- Event-driven scripting
		- JavaScript / TypeScript
		- Do their own Authn/Authz
		- sounds a lot like more managed/controlled GitHub Actions
	- Buildpacks
	  collapsed:: true
		- a way to build a container image from source without a Dockerfile
		- all required tooling to create an application for a specific app framework
		- defined workflow for creating applications with that tooling
	- CloudEvents
	  collapsed:: true
		- Specification for describing events "in The Cloud"
	- Flux
	  collapsed:: true
		- GitOps: implemented
		-
	- Flagger
	  collapsed:: true
		- Progressive Delivery
			- slowly releasing your changes to more and more instances
			- while running tests or ensuring that everything is running all along.
	- Helm
	  collapsed:: true
		- Package Manager for Kubernetes
	- Kubernetes
	  collapsed:: true
		- Orchestrator
- Cooperative Delivery Working Group Charter:
  id:: 44b040e2-2e9f-4e9c-bae2-3a53310bbe60
  collapsed:: true
	- https://github.com/cncf/tag-app-delivery/blob/main/cooperative-delivery-wg/charter/README.md#examples-of-known-patterns-aimed-to-deploy-applications
- Other related groups
  id:: 8922db3c-f371-457e-b2ea-bc43bbb6507e
	- CNCF Security TAG
	  collapsed:: true
		- second pair of eyes on guidance to ensure we aren't recommending insecure practices.
	- Kubernetes SIG Apps