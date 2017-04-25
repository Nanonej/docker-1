FROM debian

RUN apt-get update && apt-get install -y \
	wget \
	bzip2

WORKDIR /root

RUN wget http://dl.4players.de/ts/releases/3.0.13.6/teamspeak3-server_linux_amd64-3.0.13.6.tar.bz2 \
	&& tar jxvf teamspeak3-server_linux_amd64-3.0.13.6.tar.bz2

RUN rm teamspeak3-server_linux_amd64-3.0.13.6.tar.bz2

EXPOSE 9987

CMD ["/root/teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh"]
