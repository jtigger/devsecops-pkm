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
- <img src="http://localhost:3000/img/ICBmbG93Y2hhcnQgTFIKICAgIGMxLS0-YTIKICAgIHN1YmdyYXBoICJkb2NrZXItZGVza3RvcCIKICAgIGExLS0-YTIKICAgICAgc3ViZ3JhcGggIms4cyBjbHVzdGVyIgogICAgICBiMS0tPmIyCiAgICAgIGVuZAogICAgZW5kCiAgICBzdWJncmFwaCAiaG9zdCBtYWNoaW5lIgogICAgYzEtLT5jMgogICAgZW5kCg" />
  {{renderer :mermaid_odumtl}}
	- ```mermaid 
	  flowchart LR
	      c1-->a2
	      subgraph "docker-desktop"
	      a1-->a2
	        subgraph "k8s cluster"
	        b1-->b2
	        end
	      end
	      subgraph "host machine"
	      c1-->c2
	      end
	  ```
-
-