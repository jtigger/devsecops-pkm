- It's a set of gates to ensure that the container is fully used, but not more...
- Probes
	- If a container is a slow starter, it should be warmed up: that's "startup"
	- If a container is struggling, it should get a break: that's a drop in "readiness"
		- for this to be meaningful, you need at least two instances ('cause one is gonna carry more load while the other cools off)
	- If a container has failed, it should be put down: that's "liveness"
- Autoscaling: when the load reaches a certain point, add more instances.
- Thought: should (can?) autoscaling be set to key off of "readiness"?
-