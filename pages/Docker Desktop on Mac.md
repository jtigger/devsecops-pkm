- launches a VM as a node (via [[hyperkit]])
- Getting access to that VM:
	- https://gist.github.com/BretFisher/5e1a0c7bcca4c735e716abf62afad389
	- https://github.com/justincormack/nsenter1
		- Notably: how to install additional packages
		- ```console
		  docker run -it --rm --privileged --pid=host justincormack/nsenter
		  $ mount -o remount,rw /
		  $ mkdir /var/cache/apk
		  $ apk add htop
		  ```
- <p>There is an error with your mermaid syntax. Please rectify and render again.</p>
  {{renderer :mermaid_odumtl}}
	- ```mermaid 
	  graph TD;
	    A --> B
	    subgraph one
	  ```
	- ```mermaid 
	  graph TD;
	    A --> B
	    subgraph one
	  ```
-