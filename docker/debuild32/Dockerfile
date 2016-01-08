#############################################################
# Dockerfile to build 32bit Debian Jessie Build Environment #
#############################################################

# Set the base image
FROM eriol/debian-i386:jessie

# File Author / Maintainer
MAINTAINER Stuart Cardall

# add files
ADD apt.conf /etc/apt/apt.conf
ADD debdeps /usr/bin/debdeps

# Update the repository sources list
RUN apt-get update
RUN apt-get upgrade -y

# Set the env variables to non-interactive
ENV DEBIAN_FRONTEND noninteractive
ENV DEBIAN_PRIORITY critical
ENV DEBCONF_NOWARNINGS yes

################## BEGIN INSTALLATION ######################

# Install build tools
RUN apt-get install -y sudo build-essential devscripts equivs pbuilder fakeroot strace quilt dh-make cmake dpkg-dev autoconf automake libtool pkg-config apt-utils \
ruby ruby-dev less nano wget curl git net-tools inetutils-ping dialog htop openssh-client mlocate --no-install-recommends
# Install FPM https://github.com/jordansissel/fpm
# requires ruby ruby-dev
RUN gem install fpm
RUN apt-get clean
##################### INSTALLATION END #####################

ENV USER change_me
ENV HOME /build
ENV DEBFULLNAME Change Me
ENV DEBEMAIL user@host

# Create sudo user
RUN useradd -m -d $HOME --shell /bin/bash --uid 1000 $USER
RUN usermod -a -G sudo $USER
RUN echo "$USER:docker"|chpasswd

# add local repo "deb file:/build/apt ./"
ADD local.list /etc/apt/sources.list.d/local.list

# Usage: USER [UID]
USER $USER
ENTRYPOINT ["/bin/bash"]

