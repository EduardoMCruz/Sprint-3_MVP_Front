# Consultass eletrônicos

Esse projeto tem como objetivo permitir um usuário realizar as ações de listar, cadastrar, editar e excluir Consultass eletrônicos 

---
## Como executar em modo de desenvolvimento

1- Rodar a API localmente de acordo com as instruções da API.

2- Abrir o arquivo index.html no seu browser.

## Como executar através do Docker

Certifique-se de ter o [Docker](https://docs.docker.com/engine/install/) instalado e em execução em sua máquina.


```
$ docker build -t mvp_front .
```

Uma vez criada a imagem, para executar o container basta executar, seguinte o comando:

```
$ docker run --rm -p 8080:80 mvp_front
```

Uma vez executando, para acessar o front-end, basta abrir o [http://localhost:8080/#/](http://localhost:8080/#/) no navegador.

## Integração com API externa

### API de exportar excel
A API externa com a qual a integração foi realizada tem como objetivo gerar excel, onde toda a API e documentação estão disponíveis no [link] (https://github.com/SheetJS/sheetjs)
Para usar, não é necessário nenhuma licença de uso nem criação de usuário. A API utiliza licença Apache License 2.0. A classe XLSX do [script](https://cdn.sheetjs.com/xlsx-0.20.0/package/dist/xlsx.full.min.js).


### API de Especialidades
Além de se comunicar com os serviços de Consultass, o front-end também se comunica com uma API de Especialidades, em que a listagem de Especialidades é carregada no momento do carregamento da página e é usado para auxiliar o usuário a preencher o formulário de inclusão de Consultas sem erros de digitação no Especialidade, melhorando a experiência do usuário.
Estou usando a rota get da API de Especialidades, que retorna todos os Especialidades cadastrados no sistema
