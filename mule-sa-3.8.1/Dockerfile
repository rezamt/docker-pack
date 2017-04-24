FROM java:8

MAINTAINER rezamt@gmail.com

RUN wget -O ~/mule-standalone-3.8.1.tar.gz https://repository.mulesoft.org/nexus/content/repositories/releases/org/mule/distributions/mule-standalone/3.8.1/mule-standalone-3.8.1.tar.gz 
RUN cd /opt && tar xvzf ~/mule-standalone-3.8.1.tar.gz
RUN rm ~/mule-standalone-3.8.1.tar.gz
RUN ln -s /opt/mule-standalone-3.8.1 /opt/mule 

CMD [ "/opt/mule/bin/mule" ]