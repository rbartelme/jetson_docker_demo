# jetson_docker_demo
For CyVerse Advanced Container Camp Fall 2021

## Required Hardware:
[NVIDIA Jetson Nano](https://developer.nvidia.com/buy-jetson?product=jetson_nano&location=US)

## Clone this Repository:
`git clone https://github.com/rbartelme/jetson_docker_demo/`

## Getting the container image:
The interesting thing about the NVIDIA Jetson Nano is the ARM64 processor. This makes docker a bit of a pain, however the people at NVIDIA put together [this repo](https://github.com/NVIDIA-AI-IOT/jetson-pose-container/) to run the Jupyter Lab Data Science stack.

```
git clone https://github.com/tokk-nv/jetson-pose-container
cd jetson-pose-container
./scripts/set_nvidia_runtime.sh
./scripts/copy-jetson-ota-key.sh
```


## Spinning the container up:
Run statement modified from NVIDIA's quick start guide. Be sure to `cd` into the `jetson-pose-container` directory before proceeding.

`sudo ./run.sh -v ~/jetson_docker_demo/:/workdir`

## Do Fun Stuff with CUDA Cores in Jupyter lab

## Next Steps

K3S cluster of Jetson Nanos to test sharing of cuda cores.
