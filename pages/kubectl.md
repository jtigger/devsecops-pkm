- ztags: #cli #epic-note #kubernetes #tools
- ## Managing Config/Contexts
	- How to merge Kubernetes kubectl config files
		- https://medium.com/@jacobtomlinson/how-to-merge-kubernetes-kubectl-config-files-737b61bd517d
		- TL;DR. `kubectl` lets you specify a _path_ of kube config. 🙌🏻 And you can flatten that config.
		- ```
		  $ cp ~/.kube/config ~/.kube/config.bak 
		  $ KUBECONFIG=~/.kube/config:/path/to/new/config kubectl config view --flatten > /tmp/config 
		  $ mv /tmp/config ~/.kube/config 
		  $ rm ~/.kube/config.bak
		  ```
		-
- ## Authoring Resources
  collapsed:: true
	- API Docs
		- ... for a resource
		    ```console
		    $ kubectl explain service.spec
		    ```
		- ... for a hierarchy of resources
		    ```console
		    $ kubectl explain deployment.spec.template.spec.dnsConfig --recursive
		    ```
- ## Validating Resources
  id:: 63cd8fa2-5736-4f1e-8a17-30c5f60dec16
  collapsed:: true
	- One of the most reliable validation tools, use `--dry-run=server` to check manifests before applying
		- Example: an ESO v0.6.2's `ClusterSecretStore` did not support using session tokens.
		- ```
		  $ ytt -f aws-secretsmanager/ --data-values-env AWS | kubectl apply -f- --dry-run=server
		  secret/awssm-secret created (server dry run)
		  Error from server (BadRequest): error when creating "STDIN": ClusterSecretStore in version "v1beta1" cannot be handled as a ClusterSecretStore: strict decoding error: unknown field "spec.provider.aws.auth.secretRef.sessionTokenSecretRef" 
		  ```
- ## Querying
  collapsed:: true
	- Use `-o jsonpath` to select from the result. (note: escape the `.`)
	  ```console
	  kubectl get secrets default-ssl-certificate -o jsonpath={.data.'tls\.crt'}
	  ```
	  (src: https://vmware.slack.com/archives/CM3MKD77W/p1566588921089400)
- ## Troubleshooting
  collapsed:: true
	- get a shell on a container
		- ... (pod with one container)
		    ```console
		    $ kubectl exec -it ${POD_NAME} -- /bin/bash
		    ```
		- .. (pod with multiple containers)
		    ```console
		    $ kubectl exec -it ${POD_NAME} -c ${CONTAINER_NAME} -- /bin/bash
		    ```
	- verbose logging:
		- https://kubernetes.io/docs/reference/kubectl/cheatsheet/#kubectl-output-verbosity-and-debugging
- ## Resources
	- [Kubectl Kubernetes CheatSheet](https://github.com/dennyzhang/cheatsheet-kubernetes-A4)