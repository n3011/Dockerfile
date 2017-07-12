FROM nvidia/cuda:8.0-cudnn5-runtime-ubuntu14.04
LABEL maintainer "Ishant Mrinal Haloi <mrinalhaloi11@gmail.com>"
 
RUN apt-get update && apt-get install -y --no-install-recommends \
         cuda-core-$CUDA_PKG_VERSION \
         cuda-misc-headers-$CUDA_PKG_VERSION \
         cuda-command-line-tools-$CUDA_PKG_VERSION \
         cuda-nvrtc-dev-$CUDA_PKG_VERSION \         
         cuda-nvml-dev-$CUDA_PKG_VERSION \         
         cuda-nvgraph-dev-$CUDA_PKG_VERSION \         
         cuda-cusolver-dev-$CUDA_PKG_VERSION \         
         cuda-cublas-dev-$CUDA_PKG_VERSION \         
         cuda-cufft-dev-$CUDA_PKG_VERSION \         
         cuda-curand-dev-$CUDA_PKG_VERSION \         
         cuda-cusparse-dev-$CUDA_PKG_VERSION \         
         cuda-npp-dev-$CUDA_PKG_VERSION \         
         cuda-cudart-dev-$CUDA_PKG_VERSION \         
         cuda-driver-dev-$CUDA_PKG_VERSION && \
     rm -rf /var/lib/apt/lists/*
 
RUN apt-get update && apt-get install -y build-essential git libatlas-base-dev libopencv-dev
RUN apt-get install -y wget unzip

RUN apt-get install -y python-dev python-pip python-numpy python-setuptools
RUN pip install --upgrade pip
# Install tensorflow and commonly used opencv scipy 
RUN pip install tensorflow-gpu scipy opencv-python

ENV LIBRARY_PATH /usr/local/cuda/lib64/stubs:${LIBRARY_PATH}
