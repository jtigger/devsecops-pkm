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
- <img src="http://localhost:3000/img/ICBmbG93Y2hhcnQgVEIKICAgIGMxLS0-YTIKICAgIHN1YmdyYXBoIG9uZQogICAgYTEtLT5hMgogICAgZW5kCiAgICBzdWJncmFwaCB0d28KICAgIGIxLS0-YjIKICAgIGVuZAogICAgc3ViZ3JhcGggdGhyZWUKICAgIGMxLS0-YzIKICAgIGVuZAo" />
  {{renderer :mermaid_odumtl}}
	- ```mermaid 
	  flowchart TB
	      c1-->a2
	      subgraph one
	      a1-->a2
	      end
	      subgraph two
	      b1-->b2
	      end
	      subgraph three
	      c1-->c2
	      end
	  ```
-
-