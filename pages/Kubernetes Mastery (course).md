- by Bret Fisher
	- Section 12:
		- 49. Exposing DockerCoins
			- Despite exposing my  `webui`  service,
				- I couldn't seem to get to it.
			- [https://minikube.sigs.k8s.io/docs/handbook/accessing/#nodeport-access](https://minikube.sigs.k8s.io/docs/handbook/accessing/#nodeport-access)
				- > The network is limited if using the Docker driver on Darwin, Windows, or WSL, and the Node IP is not reachable directly
				- when running  `minikube service webui --url`
				- I saw a new  `ssh`  process running
					- ```
					  ssh -o UserKnownHostsFile=/dev/null \
					  				      -o StrictHostKeyChecking=no \
					  				      -N \
					  				      docker@127.0.0.1 -p 57589 \
					  				      -i /Users/jtigger/.minikube/machines/minikube/id_rsa \
					  				      -L 61481:10.98.134.67:80
					  ```
						- There's an ssh daemon running on port  `57589`
			- Later (~2022-10-15), I attempted this section again, but using Rancher Desktop
				- [[Bret Fisher]] point shared this really cool tool: `shpod`
					- https://github.com/BretFisher/shpod
	- [[Keeping Containers in Good Health]]
		-
		-
	-