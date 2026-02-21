FROM ubuntu

RUN apt-get update && apt-get install -y \
    openjdk-17-jdk \
    maven \
    git \
    curl \
    vim \
    && rm -rf /var/lib/apt/lists/*

RUN git config --global user.name "Rafael" \
    && git config --global user.email "rafaelddem@gmail.com"

RUN git clone https://github.com/rafaelddem/projedata_backend.git /var/www/html \
    && chmod +x /var/www/html/mvnw

WORKDIR /var/www/html

RUN mvn dependency:go-offline spring-boot:help

# RUN mvn flyway:migrate

# RUN mvn spring-boot:run
# CMD ["mvn", "spring-boot:run"]

CMD ["sleep", "infinity"]
