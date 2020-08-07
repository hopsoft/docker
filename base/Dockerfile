FROM ubuntu:20.04
MAINTAINER Nathan Hopkins <natehop@gmail.com>

# install common dependencies
RUN apt-get -y update\
 && apt-get -y upgrade\
 && apt-get -y --force-yes install\
 bash\
 build-essential\
 curl\
 dirmngr\
 git\
 gnupg\
 libssl-dev\
 vim\
 zlib1g-dev\
 && apt-get clean

SHELL ["/bin/bash", "-l", "-c"]

# silence git warnings
RUN git config --global advice.detachedHead false

# download and setup asdf
RUN git clone --depth 1 https://github.com/asdf-vm/asdf.git $HOME/.asdf\
 && echo "source $HOME/.asdf/asdf.sh" >> $HOME/.bashrc\
 && echo "source $HOME/.asdf/asdf.sh" >> $HOME/.profile
ENV PATH="${PATH}:/asdf/.asdf/shims:/asdf/.asdf/bin"
