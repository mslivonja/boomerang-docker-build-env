FROM ceeac/boomerang-build-env:gcc7-release

RUN apt-get -y update && \
    apt-get install -y --no-install-recommends \
    doxygen \
    git \
    ca-certificates

RUN cd /tmp && \
    git clone https://github.com/BoomerangDecompiler/boomerang.git

RUN cd /tmp/boomerang && \
    mkdir build && \
    cd build && \
    cmake .. && \
    make -j$(nproc) && \
    make install

RUN mkdir -p /workspace