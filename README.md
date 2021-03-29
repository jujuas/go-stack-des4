# GoStack - Desafio 4
## 🚀 Sobre o desafio

Nesse desafio, foi necessário realizar uma aplicação utilizando *Node.js junto ao TypeScript*, utilizando o conceito de *models, repositories e services*!

Essa é uma aplicação para armazenar transações financeiras de entrada e saída, que deve permitir o cadastro e a listagem dessas transações.


## Rotas da aplicação


**POST /transactions**
A rota deve receber title, value e type dentro do corpo da requisição, sendo type o tipo da transação, que deve ser income para entradas (depósitos) e outcome para saídas (retiradas). Ao cadastrar uma nova transação, ela deve ser armazenada dentro de um objeto com o seguinte formato :
```javascript
{
  "id": "uuid",
  "title": "Salário",
  "value": 3000,
  "type": "income"
}

```
</br>

**GET /transactions** 
Essa rota deve retornar uma listagem com todas as transações que você cadastrou até agora, junto com o valor de soma de entradas, 
retiradas e total de crédito. Essa rota deve retornar um objeto com o formato a seguir:

```javascript
{
  "transactions": [
    {
      "id": "uuid",
      "title": "Salário",
      "value": 4000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Freela",
      "value": 2000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Pagamento da fatura",
      "value": 4000,
      "type": "outcome"
    },
    {
      "id": "uuid",
      "title": "Cadeira Gamer",
      "value": 1200,
      "type": "outcome"
    }
  ],
  "balance": {
    "income": 6000,
    "outcome": 5200,
    "total": 800
  }
}
```
