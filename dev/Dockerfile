FROM ubuntu

# docker run -v ~/:/home/wrighty -it 030b5ad6a03b

#RUN \
#  apt-get update && \
#  apt-get -y upgrade && \
#  apt-get install -y build-essential && \
#  apt-get install -y software-properties-common && \
#  apt-get install -y byobu curl git htop man unzip vim wget



#Note that golang-1.10-go puts binaries in /usr/lib/go-1.10/bin. If you want them on your PATH, you need to make that change yourself.
RUN apt-get update
RUN apt-get install -y software-properties-common
RUN add-apt-repository ppa:gophers/archive
RUN apt-get update
RUN apt-get install -y golang-1.10-go git vim

COPY .bashrc /root/

#ENTRYPOINT ["/usr/lib/go-1.10/bin/go"]
#CMD ["version"]
