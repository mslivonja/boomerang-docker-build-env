FROM ceeac/boomerang-build-env:base

RUN apt-get -y update && \
    apt-get install -y --no-install-recommends \
    g++-8 \
    lcov \
    curl

ENV CC  /usr/bin/gcc-8
ENV CXX /usr/bin/g++-8
