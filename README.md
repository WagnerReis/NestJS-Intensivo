## Repositório do intensivo de NestJS do canal FullCycle

# Temas abordados:
- API REST
- Cron Job
- Queues

Neste projeto foi criado uma API REST para criar tweets, possui um cron job que a cada 5 segundos verifica quantos tweets existem no banco de dados, se existirem 10 ou mais retorna os tweets encontrados de 10 em 10, e a cada retorno adiciona-os em uma fila do redis.

Para executar o projeto basta clonar em sua maquina e executar o comando ```docker-compose up```

Voce precisará também de dois endpoints, que podem ser usados no insomnia ou post
O primeiro é uma rota do tipo POST para criar os tweets: ```http://localhost:3000/tweets```
Body de exemplo: 
```
{
  "text": "Conteudo do tweet"
}
```
O segundo é uma rota do tipo GET para listar os tweets: ```http://localhost:3000/tweets```
