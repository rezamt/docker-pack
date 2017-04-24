FROM java:8

MAINTAINER rezamt@gmail.com

RUN wget https://repository.mulesoft.org/nexus/content/repositories/releases/org/mule/distributions/mule-standalone/3.8.1/mule-standalone-3.8.1.tar.gz
RUN cd /opt && tar xvzf ~/mule-standalone-3.8.1.tar.gz
RUN echo "081530788032f2af7fe1593bd6030f25 /mule-standalone-3.8.1.tar.gz" | md5sum -c
RUN rm ~/mule-standalone-3.8.1.tar.gz
RUN ln -s /opt/mule-standalone-3.8.1.tar.gz /opt/mule 

CMD [ "/opt/mule/bin/mule" ]