FROM ubuntu

# docker build -t golang .
# docker run -v ~/:/home/wrighty -it dev

RUN apt-get update
RUN apt-get install -y software-properties-common
RUN add-apt-repository ppa:gophers/archive
RUN apt-get update
RUN apt-get install -y golang-1.10-go git vim

#Note that golang-1.10-go puts binaries in /usr/lib/go-1.10/bin. If you want them on your PATH, you need to make that change yourself.
COPY .bashrc /root/
