- ## Overview
	- very beginner friendly
	- launches a VM as a node.
		- https://github.com/moby/hyperkit
		- ```console
		  $ ps -ef | grep com.docker.hyperkit
		  $ hyperkit -h
		  ```
		- PID: `~/Library/Containers/com.docker.docker/Data/vms/0/hyperkit.pid`
		-
- Compare to other [[Local Development Kubernetes]] tools.
- ## Cheat Sheet
	- include logging
	    ```
	    minikube <command> --logtostderr --v=2
	    ```
- ## Resources
	- https://cheatsheet.dennyzhang.com/cheatsheet-minikube-a4