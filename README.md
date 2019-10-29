# Teste para Estágio de Desenvolvimento Web

# Como você será avaliado

O intuito deste teste é analisar a capacidade de responder ao desafio abaixo com uma solução criativa. Entendemos que no início da carreira, muitas vezes, não temos experiência ou conhecimentos sobre tecnologias específicas. Por isso nesse teste você terá a chance de mostrar a capacidade de **pesquisar e propor** uma solução simples e funcional.

Quando finalizar o teste, publique tudo no seu [Github](https://github.com/) e envie um e-mail com o título `[Teste Estágio] Finalizado` para [alexandre.ubaldo@eduxe.com.br](mailto:alexandre.ubaldo@eduxe.com.br).

> **ATENÇÃO**: Os bônus não são obrigatórios, priorize os requisitos básicos. Entretanto os mesmos podem lhe diferenciar dos demais candidatos.


A data final para a conclusão do desafio é **05/11/2019**

### O que nós gostaríamos :thumbsup:
- Código organizado
- Instruções de uso e configuração de seus projetos
- Commits explicando o processo de construção do projeto

### O que nós não gostaríamos :thumbsdown:
- Descobrir que não foi você quem fez seu teste.
- Ver commits gigantes, sem mensagens ou com `-m` sem pé nem cabeça.


# Missão backend

Desenvolver uma **API JSON** em **Python** ou **Node** ou **PHP**, que utilize todos os seguintes métodos (`GET`, `POST`).  

### Bônus
* Utilize Laravel :star: :star:
* Escreva testes para **API**  :star:
* Automatize o processo de criação do banco e tabelas  :star:

## Cadastro de candidatos a bolsa atleta

Nesse processo ficticio, será criado um cadastro de dados básicos de candidatos a uma bolsa ficticia.

Monte uma base de candidatos com a seguinte estrutura:

|Propriedade|Tipo|Descrição|
|---|---|---|
|name|string|Nome do candidato|
|date_of_birth|date|Data de nascimento do candidato|
|zip_code|string|Código de Endereçamento Postal do candidato|
|city|string|Cidade do Candidato|
|state|string|Estado do Candidato|

Utilize **PostgreSQL** ou **MySQL** para armazenar os dados que a **API** irá consumir.

### API endpoints

`GET /candidates`

Retorna todos do método:

 ```json
[
    {
        "id": 1,
        "name": "José Augusto",
        "date_of_birth": "2002-10-05",
        "zip_code": "30350120",
        "city": "Belo Horizonte",
        "state": "MG"
    },
    {
        "id": 2,
        "name": "Maria das Graças",
        "date_of_birth": "2003-07-15",
        "zip_code": "30122120",
        "city": "Campinas",
        "state": "SP"
    },
    ...
]
```

---

`POST /candidates`

Adiciona um novo candidato. Apenas candidatos que se encaixem nos critérios abaixo serão aceitos. Caso os dados enviados não sejam válidos o endpoint deverá retornar erro com code status **422**.
1. Residir no estado de Minas Gerais ou São Paulo.
2. Ter entre 15 e 18 anos de idade.

Corpo da Requisição:
```json
{
    "name": "José Augusto",
    "date_of_birth": "1995-10-05",
    "zip_code": "30350120"
}
```

---

**Recursos adicionais para uso**

Para validar o estado do candidato você verá descobri-lo através do CEP. Recomendamos o uso da API gratuita VIACEP.

[https://viacep.com.br/](https://viacep.com.br/)

# Missão frontend

Desenvolver um projeto para a interface de usuário em **javascript** utilizando **Vue.js** ou **React** para viabilizar a listagem e inclusão de candidatos.  

### Bônus
* Crie um projeto novo que possa ser executado via `yarn serve` :star: :star:
* Não utilize frameworks (exemplo: vuetify, material ui) :star:

## Listagem de candidatos

Utilize o endpoint criado na missão backend (`GET /candidates`) para receber e em seguida listar todos os candidatos cadastrados. Abaixo você tem uma sugestão de layout para a tela.

![Tela de Listagem](https://s3-us-west-2.amazonaws.com/tenant.w2b3n.com.br/exemplos/listagem-candidatos.png "Tela de Listagem")

### Bônus
* Seguir o layout (estrutura) sugerido. :star: :star:
* Uma cor de ícone de listagem diferente para cada usuário :star:

## Adicionar candidatos

Utilize o endpoint criado na missão backend (`POST /candidates`) para enviar um candidato para cadastro. **Caso o endpoint retorne code status 422 a interface deverá exibir uma mensagem de erro informando que o cadastro não poderá ser realizado.**

Abaixo você tem uma sugestão de layout para a tela.

![Tela de Cadastro](https://s3-us-west-2.amazonaws.com/tenant.w2b3n.com.br/exemplos/cadastro-candidatos.png "Tela de Cadastro")

![Tela de Cadastro com erros](https://s3-us-west-2.amazonaws.com/tenant.w2b3n.com.br/exemplos/cadastro-erro.png "Tela de Cadastro com erros")

### Bônus
* Seguir o layout (estrutura) sugerido. :star: :star:
* Utilizar máscaras nos campos :star:
* Validar o cadastro também no frontend :star:

## Dúvidas

Em caso de dúvidas envie um e-mail com o título `[Teste Estágio] Dúvidas` para [alexandre.ubaldo@eduxe.com.br](mailto:alexandre.ubaldo@eduxe.com.br).
