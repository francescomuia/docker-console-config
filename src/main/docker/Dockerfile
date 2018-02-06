FROM java:8-jre

MAINTAINER Francesco Muià <francescoMuia83@gmail.com>

ARG version

ADD /maven/docker-console-config-$version.jar /app/docker-console-config.jar

CMD ["java", "-Xmx200m", "-jar", "/app/docker-console-config.jar"]

HEALTHCHECK --interval=10s --timeout=3s CMD curl -f http://localhost:8888/health || exit 1

EXPOSE 8888