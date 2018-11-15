# dockerjenkinstest
# use a node base image
FROM ubuntu

# set maintainer
LABEL maintainer "miiro@getintodevops.com"

# set a health check
HEALTHCHECK --interval=5s \
            --timeout=5s \
            CMD curl -f www.google.com || exit 1

# tell docker what port to expose
EXPOSE 8000
