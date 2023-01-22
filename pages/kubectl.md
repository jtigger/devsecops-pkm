- ztags: #cli #epic-note #kubernetes #tools
- ## Authoring Resources
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
	- One of the most reliable validation tools, use `--dry-run=server` to check
- ## Querying
	- Use `-o jsonpath` to select from the result. (note: escape the `.`)
	  ```console
	  kubectl get secrets default-ssl-certificate -o jsonpath={.data.'tls\.crt'}
	  ```
	  (src: https://vmware.slack.com/archives/CM3MKD77W/p1566588921089400)
- ## Troubleshooting
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