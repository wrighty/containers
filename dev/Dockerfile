FROM ubuntu

# docker build -t dev .
# docker run -v ~/:/home/wrighty -it dev

RUN apt-get update
RUN apt-get install -y software-properties-common
RUN add-apt-repository ppa:gophers/archive
RUN apt-get update
RUN apt-get install -y golang-1.10-go git vim

#Note that golang-1.10-go puts binaries in /usr/lib/go-1.10/bin. If you want them on your PATH, you need to make that change yourself.
COPY .bashrc /root/
ENV PATH="/usr/lib/go-1.10/bin:${PATH}"

RUN \
  cd /root && \
  git clone https://github.com/wrighty/dotfiles.git && \
  cd /root/dotfiles && \
  git submodule update --init
RUN /root/dotfiles/install.sh
RUN vim +'silent :GoInstallBinaries' +qall
