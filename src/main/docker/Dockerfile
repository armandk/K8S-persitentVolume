FROM java:8
VOLUME /tmp


# RUN mkdir /Certificates

#install Spring Boot artifact
ADD /maven/*.jar spring-pet-1.0.0.jar
RUN sh -c 'touch /spring-pet.jar'
RUN mkdir /opt/ccid-conf
RUN chmod -R 700 /opt/ccid-conf

ENV JAVA_OPTS=""

ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom  -jar /spring-pet.jar " ]

# ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -Dspring.config.location=file:////opt/ccid-conf/application_cr.properties -jar /ccid-cr.jar " ]
