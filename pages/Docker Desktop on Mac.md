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
- <img src="http://localhost:3000/img/ICBmbG93Y2hhcnQgTFIKICAgIGMxLS0-ZG9ja2VyZAogICAgc3ViZ3JhcGggImRvY2tlci1kZXNrdG9wIChWTSkiCiAgICAgIGRvY2tlcmQKICAgICAgYnJpZGdlOjMxNzk4LS0-Tm9kZVBvcnQ6MzE3OTgKICAgICAgc3ViZ3JhcGggIms4cyBjbHVzdGVyIgogICAgICBOb2RlUG9ydDozMTc5OC0tPlBvZDo4MAogICAgICBlbmQKICAgIGVuZAogICAgc3ViZ3JhcGggImhvc3QgbWFjaGluZSIKICAgIGMxLS0-YzIKICAgIGVuZAo" />
  {{renderer :mermaid_odumtl}}
	- ```mermaid 
	  flowchart LR
	      c1-->dockerd
	      subgraph "docker-desktop (VM)"
	        dockerd
	        bridge:31798-->NodePort:31798
	        subgraph "k8s cluster"
	        NodePort:31798-->Pod:80
	        end
	      end
	      subgraph "host machine"
	      c1-->c2
	      end
	  ```
-
-