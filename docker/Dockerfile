FROM docker.io/maven:latest

RUN git clone https://git.oschina.net/kidqhj/dockertest.git && \
	cd dockertest && \
	mvn package && \
	echo finish building...
	
ADD start.sh /
RUN chmod 755 /start.sh
	
EXPOSE 80
ENTRYPOINT ["/start.sh"]
