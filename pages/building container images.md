- ```
  standard_init_linux.go:211: exec user process caused "exec format error"
  ```
- Typically means that you're trying to run an image on a runtime on a different CPU architecture.
- Use docker buildx
	- ```
	  docker buildx build --platform=linux/amd64 -t ...
	  ```