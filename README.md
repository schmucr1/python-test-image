# python-test-image

For testing the docker image creation process

## Usage of singularity image

If the Docker image is in the public registry then no token is required.
Otherwise, one needs to generate a "read packages" token first and then set
the Singularity environment variables as shown below in order to use the
(private) image

```bash
export SINGULARITY_DOCKER_USERNAME=<username>
export SINGULARITY_DOCKER_PASSWORD=<read-packages token>

singularity run docker://ghcr.io/schmucr1/python-test-image:from-github:main python
```
