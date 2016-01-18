FROM docker.io/maven:latest

RUN svn co --username hjqi --password qhj840922  "svn://172.16.31.128/dockertest"  --force --no-auth-cache && \
	cd dockertest && \
	mvn package && \
	echo finish building...
	
ADD start.sh /
RUN chmod 755 /start.sh
	
EXPOSE 80
ENTRYPOINT ["/start.sh"]
