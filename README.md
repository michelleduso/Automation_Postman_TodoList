# API Automation with Postman

Este projeto contém a automação de testes de API utilizando o Postman para testar os métodos **GET**, **POST** e **PUT** de uma API REST. Além disso, foram implementados testes de contrato para validação do **Schema** da API.

## Pré-requisitos

Para executar este projeto, você precisará ter os seguintes softwares instalados:

- [Node.js](https://nodejs.org/) (para execução do Newman)
- [Postman](https://www.postman.com/) (para visualizar a coleção de testes)
- [Newman](https://www.npmjs.com/package/newman) (para rodar a coleção de testes via CLI)

## Configuração do Ambiente

1. Clone o repositório do projeto de backend que será testado:
   
```bash
git clone https://github.com/michelleduso/todolist
```

## Executando o Projeto Localmente

1. Navegue até o diretório do projeto clonado:

```bash
cd todolist
```

2. Execute o projeto localmente. Certifique-se de que ele esteja rodando na porta 8080:
   
```bash
mvn spring-boot:run
```

3. Acesse a documentação da API (Swagger) através da URL:
   
```bash
http://localhost:8080/swagger-ui/index.html#/
```

##  Executando os Testes Automatizados 

Este projeto utiliza o Newman para rodar a coleção de testes do Postman via linha de comando.

1. Instalação do Newman
   
Certifique-se de que o Newman está instalado. Caso contrário, instale-o globalmente via npm:

```bash   
npm install -g newman
```

2. Clonar Repositório de Automação

Clone este repositório de automação (caso ainda não tenha feito):

```bash   
git clone https://github.com/seu-usuario/seu-repositorio-de-automacao.git
```

3. Executar Testes com Newman

Navegue até o diretório do projeto de automação:  

```bash   
cd seu-repositorio-de-automacao
```

Execute a coleção de testes utilizando o Newman:

```bash   
newman run collection.json -r html
```

Ou

```bash   
newman run "collection.json" -e "environment.json" -r htmlextra
```

- collection.json é o arquivo da coleção do Postman.
- O parâmetro -r html gera o relatório em formato HTML.

# Relatórios
  
Ao executar os testes com o Newman, um relatório em HTML será gerado. Ele será salvo no diretório onde o comando foi executado e pode ser visualizado abrindo o arquivo newman que será gerado.

# Testes Implementados
## Métodos Validados

- GET: Testes de retorno de dados, validação de status code e tempo de resposta.
- POST: Testes de criação de novos recursos na API.
- PUT: Testes de atualização de recursos existentes.

## Teste de Contrato
Os testes de contrato garantem que o Schema da API segue o formato esperado para as respostas.
