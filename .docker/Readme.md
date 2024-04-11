# Building Docker Images for Benchmarking
## Note
This is a pre-release proof-of-concept version based off an existing Anaconda environment.
In the future there will be different images per benchmarked environment.

These Docker environments are used in the Github workflows which will be built-out over time.

## Building steps
1. `docker build -t trex22/initial_py311_grad_cam_py_torch-v1 .`
2. `docker push trex22/initial_py311_grad_cam_py_torch-v1`
3. `docker scan trex22/initial_py311_grad_cam_py_torch-v1`
