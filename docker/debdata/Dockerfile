#############################################################
# Dockerfile to build Debian Jessie DATA-ONLY image #
#############################################################

# Set the base image  
FROM debian:jessie-backports

# File Author / Maintainer
MAINTAINER Stuart Cardall  

# Set the env variables to non-interactive
ENV DEBIAN_FRONTEND noninteractive
ENV DEBIAN_PRIORITY critical
ENV DEBCONF_NOWARNINGS yes

################## BEGIN INSTALLATION ######################

# Install nothing for a data-only container

##################### INSTALLATION END #####################

# Usage: USER [UID]
USER 1000

# Set default container command
ENTRYPOINT ["echo", "data-only-container"]

