- https://github.com/moby/hyperkit
- [[minikube]] creates a VM to host containers:
	- ```console
	  $ ps -ef | grep com.docker.hyperkit
	  $ hyperkit -h
	  ```
- Breaking down a hyperkit invocation:
	- ```
	  com.docker.hyperkit \
	    -A \
	    -u \
	    -F vms/0/hyperkit.pid \     # location of PID
	    -c 8 \                      # number of CPUs
	    -m 8192M \
	    -s 0:0,hostbridge \         # 
	    -s 31,lpc \
	    -s 1:0,virtio-vpnkit,path=vpnkit.eth.sock,uuid=91274488-f6c7-4b55-9257-5443787f98fe \
	    -U a49160bb-38fe-4fd1-b388-f022ae741c2f \
	    -s 2:0,virtio-blk,/Users/jtigger/Library/Containers/com.docker.docker/Data/vms/0/data/Docker.raw \
	    -s 3,virtio-sock,guest_cid=3,path=vms/0,guest_forwards=1525 \
	    -s 4,virtio-rnd \
	    -l com1,null,asl,log=vms/0/console-ring \
	    -f kexec,/Applications/Docker.app/Contents/Resources/linuxkit/kernel,/Applications/Docker.app/Contents/Resources/linuxkit/initrd.img,earlyprintk=serial page_poison=1 vsyscall=emulate panic=1 nospec_store_bypass_disable noibrs noibpb no_stf_barrier mitigations=off linuxkit.unified_cgroup_hierarchy=1 console=ttyS0 console=ttyS1 tsc=reliable noapic vpnkit.connect=connect://2/1999 vpnkit.disable=osxfs-data 
	  ```