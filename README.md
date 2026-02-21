

1) Para iniciar o sistema rode:

```docker-compose up -d --build```

Ou, caso seja necessário garantir que nenhum dado anterior seja mantido, rode:

```docker-compose build --no-cache```
```docker-compose up -d```


2) Uma vez iniciado os containers, entre dentro container do backend com o comando:

```docker exec -it projedata_api bash```


3) Dentro do container, vá até a pasta "/var/www/html":

```cd /var/www/html```


4) Limpar o banco de dados. Esse passo somente será necessário se for preciso apagar todos os registros e tabelas, caso contrário pular para o próximo passo:

```mvn flyway:clean```


5) Rodar as migrations. Esse passo somente será necessário a primeira vez que o sistema for iniciado, ou se as tabelas forem apagadas (passo anterior):

```mvn flyway:migrate```


6) Iniciar o backend:

```mvn spring-boot:run```
