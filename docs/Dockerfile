FROM docs/base:latest
MAINTAINER Mary Anthony <mary@docker.com> (@moxiegirl)

RUN svn checkout https://github.com/docker/compose/trunk/docs /docs/content/compose
RUN svn checkout https://github.com/docker/docker/trunk/docs /docs/content/docker
RUN svn checkout https://github.com/docker/swarm/trunk/docs /docs/content/swarm
RUN svn checkout https://github.com/docker/distribution/trunk/docs /docs/content/registry
RUN svn checkout https://github.com/docker/tutorials/trunk/docs /docs/content
RUN svn checkout https://github.com/docker/opensource/trunk/docs /docs/content/opensource
RUN svn checkout https://github.com/docker/machine/trunk/docs /docs/content/machine

ENV PROJECT=kitematic
# To get the git info for this repo
COPY . /src

COPY . /docs/content/$PROJECT/
