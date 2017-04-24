FROM java:8

LABEL maintainer "REZAMT.AT.GMAIL.COM"

ENV MULE_HOME /opt/mule
ENV MULE_APPS /opt/mule/apps 
ENV MULE_CONF /opt/mule/conf
ENV MULE_LOGS /opt/mule/logs
ENV MULE_DOMAINS /opt/mule/domains 

RUN wget -O ~/mule-standalone-3.8.1.tar.gz https://repository.mulesoft.org/nexus/content/repositories/releases/org/mule/distributions/mule-standalone/3.8.1/mule-standalone-3.8.1.tar.gz 
RUN cd /opt && tar xvzf ~/mule-standalone-3.8.1.tar.gz
RUN rm ~/mule-standalone-3.8.1.tar.gz
RUN ln -s /opt/mule-standalone-3.8.1 /opt/mule 

CMD [ "/opt/mule/bin/mule" ]