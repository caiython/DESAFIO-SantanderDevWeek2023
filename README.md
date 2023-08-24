# Desafio de ETL para Análise de Uso de Cartões de Crédito

Este repositório apresenta a solução para um desafio de ETL (Extração, Transformação e Carregamento) com o objetivo de analisar o uso de cartões de crédito dos usuários. O projeto aborda a criação de um banco de dados, a manipulação de dados brutos, a geração de alertas personalizados com base nos dados e a visualização dos resultados transformados.

## 🎲 Banco de Dados

Antes de iniciar o processo de ETL, é realizada a criação do banco de dados local `sqlite`, criando as tabelas necessárias para armazenar as informações relevantes. As tabelas desempenham um papel crucial na estruturação dos dados. Entre as tabelas incluídas estão:

- `users`: Armazena dados de usuários;
- `accounts`: Mantém informações de contas bancárias;
- `cards`: Registra detalhes de cartões de crédito;
- `news`: Contém mensagens e alertas.

Essa etapa de preparação do banco de dados é fundamental para a integridade e organização dos dados que serão posteriormente transformados e analisados no processo de ETL.

## 📊 Processo de ETL

O processo de ETL desenvolvido neste desafio consiste nas seguintes etapas:

1. Extração dos Dados
Os dados brutos são extraídos do banco local SQLite através de uma `query` e da biblioteca `pandas`, que contém informações sobre os usuários, os limites dos cartões de crédito e o uso dos cartões.

2. Transformação dos Dados
Os dados extraídos são submetidos a uma série de transformações. Um cálculo é realizado para obter a porcentagem de uso dos cartões de crédito de cada usuário, então a maior porcentagem de uso é selecionada. Com base nessa porcentagem, são gerados alertas personalizados que sugerem ações aos usuários, dependendo do nível de utilização.

3. Carregamento dos Dados
Os resultados transformados são carregados de volta ao banco SQLite, numa tabela reservada para estes alertas. Cada usuário é associado a uma mensagem de alerta correspondente ao seu nível de uso de cartão de crédito.

## 📋 Estrutura do Repositório

O repositório está organizado da seguinte forma:

- `desafio.ipynb`: Jupyter Notebook contendo todo o código fonte e sua documentação;
- `SDW2023.db`: Banco de dados SQLite;
- `README.md`: Este arquivo de documentação.

## 🚀 Executando o Projeto
1. Clone este repositório para o seu ambiente local.
Certifique-se de ter o Python e as bibliotecas do Jupyter Notebook, Pandas e SQLite3 instaladas;
2. Execute o Jupyter Notebook na pasta clone do repositório e abra o arquivo `desafio.ipynb` para ter acesso ao código e sua documentação;
3. Caso deseje executar o código, apague o banco `SDW2023.db` da sua pasta clone do repositório.

## 💡 Resultados
Com o código completo, é possível visualizar os resultados transformados através do processo de ETL. Os alertas personalizados, gerados com base na porcentagem de uso de cartão de crédito, foram carregados no banco de dados e podem ser acessados por outros serviços que entreguem a mensagem ao usuário.

---

Obrigado por ler até aqui! - [Caiython](https://github.com/caiython) 😊