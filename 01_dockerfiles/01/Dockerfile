FROM debian:latest

ENV TS3SERVER_LICENSE="accept"

EXPOSE 9987/udp
EXPOSE 30033/tcp
EXPOSE 10011/tcp

RUN apt-get update; \
apt-get install -y curl bzip2; \
curl https://files.teamspeak-services.com/releases/server/3.6.1/teamspeak3-server_linux_amd64-3.6.1.tar.bz2 -o ts.tar.bz2; \
tar -jxvf ts.tar.bz2;

ENTRYPOINT ["sh", "-c", "/teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh"] 
