# Marvel Heroes
<p>
Essa SPA (Single Page Application) lista herois da Marvel consumindo da API developer.marvel.com.
</p>

## Entendendo a Consulta
<p>
Para o uso da API é necessário criar um usuário, é possível realizar até 3 mil chamadas.

Na documentação do site é repassado o link para consumir a API, são necessárias algumas informações de usuário para as consultas.

Link para consumo da API: http://gateway.marvel.com/v1/public/characters?ts=TIMESTAMP&apikey=PUBLICKEY&hash=HASH

</br>
Como é possível observar é necessário essas 3 informações para o consumo da API:

TimeStamp - É possível pegar esse dado através do comando Math.floow(Date.now() / 1000) no console do navegador.

Public Key - É possível pegar esse dado no próprio site após logar com seu usário e visualizar os detalhes da sua conta.

Hash - É o MD5 da concatenação da TimeStamp, com a Public Key, mais a Private Key(disponivel nos detalhes da conta).
</p>

## Limitando a Quantidade de Heróis Listados

<p>
 Na própria API é possível limitar a quantidade do uso de hérois que serão listados.
 
 Basta adicionar o parametro "limit" no link como é mostrado abaixo:
 
 http://gateway.marvel.com/v1/public/characters?ts=TIMESTAMP&apikey=PUBLICKEY&hash=HASH&limit=20
 
 Caso esse parâmetro não seja especificado não apresentará problema na listagem, pois o valor padrão é de 20.
</p>
