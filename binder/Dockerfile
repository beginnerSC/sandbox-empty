# Latex-Online container
#
# VERSION       1

# use the ubuntu base image provided by dotCloud
FROM node:8.9.1-stretch

# MAINTAINER Andrey Lushnikov aslushnikov@gmail.com

# Sorted list of used packages.
RUN apt-get clean && apt-get update && apt-get install -y \
    texlive-xetex \ 
    texlive-fonts-recommended \
    texlive-generic-recommended

# Add xindy-2.2 instead of makeindex.
# ADD ./packages/xindy-2.2-rc2-linux.tar.gz /opt
# ENV PATH="/opt/xindy-2.2/bin:${PATH}"

# COPY ./util/docker-entrypoint.sh /

# EXPOSE 2700
# CMD ["./docker-entrypoint.sh"]
