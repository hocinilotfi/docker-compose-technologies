FROM jenkins/jenkins:lts-jdk11

USER root

# Installer Docker CLI (pas inclus dans l'image officielle)
RUN apt-get update && apt-get install -y docker.io

# Copier la liste des plugins à installer
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt

# Installer les plugins listés dans plugins.txt
RUN jenkins-plugin-cli --plugin-file /usr/share/jenkins/ref/plugins.txt

USER jenkins

