# policy-test

# Descrição Rápida

Esse projeto deve criar uma interface que permita o manuseio e edição de regras de jogo, bem como de times e seus jogadores como parte de um dashboard.

# Requerimentos

- Haverá autenticação de usuário
- Dashboard terá 4 sessões principais no Home, como demonstrado na primeira imagem.
- A sessão Teams and Rosters deve poder listar, acrescentar, editar ou remover times (Um Roster é um time)
- A sessão Policies deve poder listar, acrescentar, editar ou remover itens
- Os comandos para alterar os dados persistidos devem fazer um fingir uma requisição web

# Especificações

- uuid neste contexto (uma string única, mas modificável. Tipo os handlers to twitter, para marcar alguém)
- Os modelos utilizados aqui são:
  -- Usuário
  --- id, nome, sobrenome, uuid, avatar_url, tipo
  -- Time
  --- id, uuid, coach_id
  -- TeamPlayers (a ligação entre um jogador e um time)
  --- id, team_id, player_id
  -- TeamCoaches (a ligação entre um time e um treinador)
  -- Policies (as regras)
  --- id, state, league, rules (um array de strings é suficiente por enquanto)
- As sessões que ligam um team a uma policy podem ser eliminadas do design e da lógica

# Sugestões

- A autenticação pode acontecer sem um backend, usando por exemplo "senha_certa" como uma chave que autentique e qualquer outra coisa como uma falha.
- Um modo de fazer o mock das requisições web é criar uma função e joga os parâmetros da requisição para o console
- Se quiser fazer um sistema completo com Rails, incluindo o backend, fique a vontade
- Se quiser fazer um SPA, react é preferível, mas não obrigatório
- Testes são bem vindos
- Há questões em aberto. Pergunte tudo o que achar relevante para esclarecer.
