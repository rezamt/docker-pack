FROM java:8

LABEL maintainer "REZAMT.AT.GMAIL.COM"

ENV MULE_HOME /opt/mule
ENV MULE_APPS /opt/mule/apps 
ENV MULE_CONF /opt/mule/conf
ENV MULE_LOGS /opt/mule/logs
ENV MULE_DOMAINS /opt/mule/domains

ENV MULE_APP_LONG "default"
ENV MULE_APP "default"


RUN wget -O /tmp/mule-standalone-3.8.1.tar.gz https://repository.mulesoft.org/nexus/content/repositories/releases/org/mule/distributions/mule-standalone/3.8.1/mule-standalone-3.8.1.tar.gz 
COPY ./echo-mule.tar /tmp/echo-mule.tar
RUN cd /opt && tar xvzf /tmp/mule-standalone-3.8.1.tar.gz
RUN ln -s /opt/mule-standalone-3.8.1 /opt/mule 
RUN cd /opt/mule/apps && tar xvzf /tmp/echo-mule.tar
RUN rm /tmp/mule-standalone-3.8.1.tar.gz
RUN rm /tmp/echo-mule.tar

CMD [ "/opt/mule/bin/mule" ]