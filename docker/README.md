`32 & 64bit` Debian Jessie build environments
---
* Build the containers with:

`docker build -t $USER/your_image_name /path/to/Dockerfile`

* Use the [`dki` script](https://github.com/itoffshore/debian-scripts/blob/master/docker/dki) to start a build environment with a `data-only` container:

`dki -i your_image_name -c some_other_name`

* Attach to the container with:

`docker attach some_other_name`
