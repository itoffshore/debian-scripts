######################################################
# Dockerfile to build Alpine Linux DATA-ONLY image   #
######################################################

# Set the base image
FROM alpine

# File Author / Maintainer
MAINTAINER Stuart Cardall

# Update the repository sources list
#RUN apk update
#RUN apk upgrade

################## BEGIN INSTALLATION ######################

# Install nothing for a data-only container

##################### INSTALLATION END #####################

# Usage: USER [UID]
USER 1000

# Set default container command
ENTRYPOINT ["echo", "data-only-container"]

