- Charter:
	- [https://github.com/cncf/toc/blob/main/tags/app-delivery.md](https://github.com/cncf/toc/blob/main/tags/app-delivery.md)
	  collapsed:: true
		- to write informational guides, tutorials, and whitepapers
		- support the TOC with our deeper know-how of "App Delivery" (developing, distributing, deploying, and managing cloud-native applications)
		- Scope:
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
		- https://github.com/cncf/tag-app-delivery/blob/main/cooperative-delivery-wg/charter/README.md#examples-of-known-patterns-aimed-to-deploy-applications
	- Other related groups
		- CNCF Security TAG
		  collapsed:: true
			- second pair of eyes on guidance to ensure we aren't recommending insecure practices.
		- Kubernetes SIG Apps
	-