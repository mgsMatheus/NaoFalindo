# NãoFalindo

Uma API para o sistema de controle de gastos pessoais.

## Endpoints

- Despesas
  - [Cadastrar](#cadastrar-despesa)
  - Listar todas
  - Apagar
  - Ataulizar
  - Detalhes
- Receitas
  - Cadastrar
  - Listar todas
  - Apagar
  - Atualizar
  - Detalhes

### Cadastrar Despesa
`POST` /naoFalindo/api/despesa

*Exemplo de requisição*

| campo | tipo | obrigatório | descricao 
|-------|------|:-------------:|-----------
|valor|decimal|sim o valor da despesa|data|data|sim a data da despesa|
contaId|inteiro|sim| o id de uma conta previamente cadastrada 
categoriaId|inteiro|sim| o id de uma conta previamente cadastrada
descricao|texto|nao| 

```json
{ 
  valor: 100.59,
  data: '2023-12-27',
  contaId: 1, 
  categoriaID: 1,
  descricao: 'cinema com os amigos'
}

``` 

### Detalhes Despesa

`GET` naofalindo/api/despesa/{id} 

*Resposta*
| codigo | descricao
|------- | ---------
| 201 | a despesa foi cadastrada com sucesso
| 400 | campos invalidos

*Exemplos de resposta*
```json
{ 
  valor: 100.59,
  data: '2023-12-27',
  contaId: 1, 
  categoriaID: 1,
  descricao: 'cinema com os amigos'
}
```