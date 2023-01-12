# <REPO-NAME>
Custom implementation of iterative image diffusion process

### Build & Run docker

- `docker build -t <repo-name> .` - to build docker
- To run a container, use:
```
docker run -d -it --init \
--gpus=all \
--ipc=host \
--volume="$PWD:/app" \
--volume="/home/:/hhome" \
--volume="/usr/local/cuda:/usr/local/cuda" \
--publish="7777:7777" \
--publish="7777:7778" \
<repo-name> bash
```
- To execute container bash interface, run: `docker exec -it <container_id> bash` 

#### Run jupyter server

- `jupyter lab --no-browser --ip 0.0.0.0 --port 7777 --allow-root --notebook-dir=.`
