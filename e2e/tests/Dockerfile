FROM node:18-slim

RUN apt-get update -qq && apt-get install -qy \ 
    ca-certificates \
    bzip2 \
    curl \
    libfontconfig \
    --no-install-recommends

RUN curl -I https://registry.yarnpkg.com

RUN yarn global add phantomjs-prebuilt
ADD . /app
WORKDIR /app
CMD ./tests.sh
