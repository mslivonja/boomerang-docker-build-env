FROM ubuntu:bionic

RUN useradd -m boomerang
WORKDIR /home/boomerang/
ENV HOME /home/boomerang

RUN apt-get -y update && \
    apt-get install -y --no-install-recommends \
    make \
    cmake \
    ccache \
    qt5-default \
    git \
    libcapstone-dev \
    flex \
    wget \ 
    build-essential

RUN cd /tmp && \
    wget http://ftp.gnu.org/gnu/bison/bison-3.4.tar.gz && \
    tar -zxvf bison-3.4.tar.gz && \
    rm -f bison-3.4.tar.gz && \
    cd bison-3.4 && \
    ./configure && \
    make && \ 
    make install && \
    ln -s /usr/local/bin/bison /usr/bin/bison && \
    rm -Rf /tmp/*bison*

COPY . boomerang
RUN chown -R boomerang:boomerang boomerang
