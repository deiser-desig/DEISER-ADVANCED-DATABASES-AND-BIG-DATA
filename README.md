# DEISER-ADVANCED-DATABASES-AND-BIG-DATA
# Projeto: Aplicação Prática de Tecnologias de Banco de Dados e Big Data na E-Shop Brasil

# ESTUDO DE CASO
APLICAÇÃO PRÁTICA DE TECNOLOGIAS DE BANCO DE DADOS E BIG DATA EM UMA EMPRESA DE COMÉRCIO ELETRÔNICO.


## 1. Introdução:
Aplicação Prática de Tecnologias de Banco de Dados e Big Data em uma Empresa de Comércio Eletrônico.
1.1 APRESENTAÇÃO DO PROBLEMA: A E-Shop Brasil é uma das maiores plataformas de e-commerce do país, com milhões de clientes ativos e uma média de 100 mil pedidos por dia. Com esse grande volume de dados, surgem desafios relacionados à gestão eficiente da informação, personalização da experiência do cliente e otimização da logística — especialmente em regiões remotas.
Este projeto propõe uma solução prática e visual que utiliza tecnologias de banco de dados e Big Data para apoiar as áreas de marketing, vendas e operações da empresa.

1.2 OBJETIVO DO PROJETO: Garantir segurança e privacidade dos dados dos clientes.
Personalizar a experiência do cliente com base em dados históricos.
Otimizar a entrega e controle de estoque, especialmente em regiões remotas.
Implementar uma solução escalável e sustentável a longo prazo.
Desenvolver uma solução que utilize tecnologias de banco de dados avançadas (SQL, NoSQL) e Big Data para melhorar a gestão de dados e a logística da E-Shop Brasil, garantindo a segurança dos dados dos clientes, oferecendo experiências personalizadas e otimizando a entrega de produtos de forma eficiente e escalável.

## 2. Descrição do Projeto:
Este projeto apresenta uma solução prática para os desafios enfrentados pela empresa fictícia E-Shop Brasil, uma gigante do comércio eletrônico nacional. A proposta visa melhorar a gestão de dados e a eficiência logística da empresa utilizando tecnologias modernas.

2.1 USO DO DOCKER:
Utilizamos o Docker para criar um ambiente isolado e padronizado, facilitando a configuração e execução do projeto, além de garantir portabilidade entre diferentes sistemas operacionais.

2.2 CONTAINER COM MONGODB:
Foi configurado um container Docker com MongoDB, um banco de dados NoSQL orientado a documentos, ideal para armazenar grandes volumes de dados de maneira flexível e escalável.

2.3 APLICAÇÃO STREAMLIT (APP.PY):
Foi desenvolvido uma aplicação com Streamlit, que;
Se conecta ao banco MongoDB.
Permite inserir novos dados no banco.
Realiza edições e exclusões de dados existentes.
Concatena dados de diferentes coleções (ex: clientes + pedidos).
Consulta e exibe os dados em uma interface gráfica acessível via navegador.

3. PASSOS PARA A IMPLEMENTAÇÃO:
   






MONGODB (NOSQL): para armazenar e consultar grandes volumes de dados de forma flexível.
DOCKER: para garantir portabilidade e padronização do ambiente de desenvolvimento e produção.
STREAMLIT: para construir uma interface web simples e interativa que se comunica com o banco de dados.
A aplicação desenvolvida permite: Inserção de dados de clientes, produtos e pedidos no MongoDB. Manipulação (edição ou exclusão) dos dados já existentes. Concatenação de dados de diferentes coleções para análises integradas. Consultas dinâmicas e visualização dos resultados em uma interface intuitiva.
Essa arquitetura facilita a personalização da experiência do cliente com base no histórico de compras, garante segurança no armazenamento dos dados e contribui para decisões mais estratégicas na logística e estoque, especialmente em regiões remotas do Brasil.

APRESENTAÇÃO DO PROBLEMA: A E-Shop Brasil é uma das maiores plataformas de comércio eletrônico do país, com uma ampla gama de produtos de eletrônicos a itens de moda atendendo milhões de clientes em todo o território nacional. Com um crescimento expressivo desde sua fundação em 2010, a empresa já ultrapassou a marca de 5 milhões de clientes ativos e processa em média 100 mil pedidos por dia. Com o aumento da complexidade nas operações e o volume de dados gerados diariamente, a empresa enfrenta desafios significativos relacionados à gestão de dados, personalização da experiência do cliente e otimização logística. A equipe de Tecnologia da Informação TI da E-Shop Brasil foi encarregada de propor soluções inovadoras que envolvam tecnologias avançadas de banco de dados e Big Data, visando apoiar áreas como marketing, vendas e operações. O projeto precisa ser concluído antes do pico de vendas do final do ano, e a solução deve contemplar:  A segurança e privacidade dos dados dos clientes; a capacidade de personalizar a navegação e recomendações com base em comportamentos anteriores; a melhoria na eficiência da entrega e no controle de estoques, especialmente em regiões mais distantes; a escalabilidade e integração tecnológica, com foco na sustentabilidade a longo prazo. Sua missão é se colocar no papel dessa equipe e propor, de forma visual e prática, como a E-Shop Brasil pode superar esses desafios com base nos conhecimentos adquiridos sobre bancos de dados relacionais, NoSQL e Big Data.


### 3.1 Uso do Docker

O Docker é utilizado para criar um ambiente isolado, padronizado e portátil. Ele garante que a aplicação funcione da mesma forma em diferentes sistemas operacionais e facilita a execução do projeto por outros usuários.

### 3.2 Container com MongoDB

Um container MongoDB foi configurado para armazenar os dados de forma flexível e escalável, ideal para lidar com os grandes volumes de dados gerados diariamente pela E-Shop Brasil.

### 3.3 Aplicação em Streamlit (app.py)

A aplicação desenvolvida em Streamlit permite:

- Conectar ao MongoDB.
- Inserir dados no banco.
- Manipular dados existentes (editar e excluir).
- Concatenar dados de diferentes coleções.
- Realizar consultas e exibir os dados na interface gráfica.

## 4. Passos para Implementação

### 4.1 Comandos para Configurar e Executar o Ambiente

- Subir a infraestrutura com `docker-compose`:
  ```bash
  docker-compose up --build


 Descrição Técnica do Projeto
 Uso do Docker
O Docker é utilizado neste projeto para criar um ambiente isolado, padronizado e portátil, facilitando a configuração e execução da aplicação em qualquer sistema operacional. Ele permite empacotar a aplicação, as dependências do Python e o banco de dados MongoDB em containers independentes e interconectados.

 Configuração do Container com MongoDB
A aplicação utiliza o MongoDB como banco de dados NoSQL, executado dentro de um container Docker configurado via docker-compose.yml. O container expõe a porta padrão 27017, possibilitando a conexão da aplicação com o banco localmente. O volume de dados também é persistido usando volumes Docker, garantindo que as informações não sejam perdidas mesmo após o desligamento do container.

Aplicação em Streamlit (app.py)
A aplicação foi desenvolvida em Streamlit, uma biblioteca Python que permite a criação de interfaces web interativas com facilidade. A aplicação app.py:

Se conecta ao banco de dados MongoDB.

Permite inserir novos dados (clientes, produtos, pedidos).

Permite editar ou excluir registros existentes.

Realiza a concatenação de dados entre diferentes coleções, como combinar dados de clientes e pedidos.

Exibe consultas personalizadas diretamente na interface gráfica, com tabelas e filtros interativos.

 Passos para Implementação
 Comandos para subir o ambiente com Docker Compose:

docker-compose up --build
Esse comando cria os containers da aplicação e do MongoDB e os executa em conjunto.

 Alternativa com Dockerfile (se não usar o docker-compose):

docker build -t eshop-app .
docker run -p 8501:8501 eshop-app
Obs: Certifique-se de que o container do MongoDB esteja em execução separadamente caso use apenas o Dockerfile.


🧩 Funcionalidades da Aplicação
A aplicação oferece as seguintes funcionalidades principais:

Inserção de dados no MongoDB (ex: cadastro de clientes, produtos e pedidos).

 Manipulação de dados (edição ou exclusão de registros).

 Concatenação de dados entre coleções diferentes (ex: cruzamento de dados de clientes e pedidos).

 Consultas interativas com exibição dos dados em tabelas e filtros personalizados pela interface Streamlit.

 Testes e Exemplos
Para facilitar o entendimento do funcionamento da aplicação, a pasta /exemplos do projeto inclui:

Prints de tela mostrando as principais operações (inserção, edição, exclusão, concatenação e consultas).

 (Opcional) GIFs curtos mostrando a aplicação em funcionamento.

 Arquivos Necessários
Para rodar o projeto localmente, o repositório GitHub inclui:

Dockerfile e/ou docker-compose.yml: Definição e orquestração do ambiente Docker.

app.py: Código Python da aplicação em Streamlit.

dados_exemplo.json ou script gerador: Conjunto de dados falsos ou extraídos de plataformas como o Kaggle, usados para testes e simulação realista.

Estrutura do Projeto
e-shop-brasil/
├── README.md
├── Dockerfile (se necessário)
├── docker-compose.yml (se utilizado)
├── app.py
├── dados_exemplo.json (ou script gerador de dados)
└── exemplos/         # Prints ou GIFs das funcionalidades

docker-compose.yml
version: "3.8"

services:
  mongo:
    image: mongo:latest
    container_name: mongo
    ports:
      - "27017:27017"
    volumes:
      - mongo_data:/data/db

  app:
    build: .
    container_name: streamlit_app
    ports:
      - "8501:8501"
    depends_on:
      - mongo

volumes:
  mongo_data:

Dockerfile
FROM python:3.11

WORKDIR /app

COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

COPY . .

CMD ["streamlit", "run", "app.py", "--server.port=8501", "--server.address=0.0.0.0"]

requirements.txt

pymongo
streamlit
pandas

 app.py (Aplicação em Streamlit)
python
Copiar
Editar
import streamlit as st
from pymongo import MongoClient
import pandas as pd

# Conectar ao MongoDB
client = MongoClient("mongodb://mongo:27017/")
db = client["eshop"]
colecao_clientes = db["clientes"]
colecao_pedidos = db["pedidos"]

st.title("📦 Gestão de Dados - E-Shop Brasil")

menu = st.sidebar.selectbox("Selecione uma opção", ["Inserir Dados", "Visualizar Dados", "Editar Dados", "Deletar Dados", "Concatenar Coleções"])

if menu == "Inserir Dados":
    st.subheader("Inserir novo cliente")
    nome = st.text_input("Nome")
    email = st.text_input("Email")
    cidade = st.text_input("Cidade")
    if st.button("Inserir"):
        colecao_clientes.insert_one({"nome": nome, "email": email, "cidade": cidade})
        st.success("Cliente inserido com sucesso!")

elif menu == "Visualizar Dados":
    st.subheader("Clientes")
    dados = list(colecao_clientes.find({}, {"_id": 0}))
    st.dataframe(pd.DataFrame(dados))

elif menu == "Editar Dados":
    st.subheader("Editar cliente por email")
    email_ref = st.text_input("Email do cliente a editar")
    novo_nome = st.text_input("Novo nome")
    if st.button("Atualizar"):
        colecao_clientes.update_one({"email": email_ref}, {"$set": {"nome": novo_nome}})
        st.success("Cliente atualizado!")

elif menu == "Deletar Dados":
    st.subheader("Deletar cliente por email")
    email_del = st.text_input("Email do cliente a deletar")
    if st.button("Deletar"):
        colecao_clientes.delete_one({"email": email_del})
        st.success("Cliente deletado!")

elif menu == "Concatenar Coleções":
    st.subheader("Exibir clientes e seus pedidos")
    clientes = list(colecao_clientes.find({}, {"_id": 0}))
    pedidos = list(colecao_pedidos.find({}, {"_id": 0}))
    df_clientes = pd.DataFrame(clientes)
    df_pedidos = pd.DataFrame(pedidos)
    if not df_clientes.empty and not df_pedidos.empty:
        resultado = pd.merge(df_clientes, df_pedidos, on="email", how="inner")
        st.dataframe(resultado)
    else:
        st.warning("Coleções vazias.")

Dados de Exemplo (opcional) – dados_exemplo.json
  { "nome": "Ana Souza", "email": "ana@email.com", "cidade": "São Paulo" },
  { "nome": "João Silva", "email": "joao@email.com", "cidade": "Rio de Janeiro" }

git clone https://github.com/deiser-desig/DEISER-ADVANCED-DATABASES-AND-BIG-DATA/edit/main/README.md
cd e-shop-brasil

docker-compose up --build

http://localhost:8501




