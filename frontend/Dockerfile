FROM ubuntu:22.04

RUN apt-get update && apt-get install -y \
    git \
    curl \
    vim \
    bash \
    ca-certificates \
    && rm -rf /var/lib/apt/lists/*

RUN curl -fsSL https://deb.nodesource.com/setup_22.x | bash - \
    && apt-get install -y nodejs \
    && rm -rf /var/lib/apt/lists/*

RUN git config --global user.name "Rafael" \
    && git config --global user.email "rafaelddem@gmail.com"

RUN git clone https://github.com/rafaelddem/projedata_frontend.git /var/www/html

WORKDIR /var/www/html

RUN npm install

CMD ["npm", "start"]
