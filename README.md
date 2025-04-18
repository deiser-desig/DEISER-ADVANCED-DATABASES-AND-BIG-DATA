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
PRIMEIRO,  Clonar o repositório
```bash
git clone https://github.com/deiser-desig/e-shop-brasil.git
cd e-shop-brasil
SEGUNDO, Subir a infraestrutura com Docker:
docker-compose up --build
ou, se for utilizado o Dockerfile diretamente:
docker build -t eshop-app .
docker run -p 8501:8501 eshop-app
TERCEIRO, Executar a aplicação Streamlit
Acessando o navegador:
http://localhost:8501

3.1 INSRUÇÕES PARA EXECUTAR A APLICAÇÃO EM STREAMLIT (APP.PY)

Acessando o navegador:

http://localhost:8501

4. FUNCIONALIDADES DA APLICAÇÃO:
A aplicação possui as seguintes funcionalidades principais:

Inserir dados no banco MongoDB.
Editar ou excluir dados já existentes.
Concatenar dados entre diferentes coleções (ex: clientes e pedidos).
Realizar consultas e visualizar os dados de forma interativa.
Exibir os resultados na interface gráfica com tabelas e filtros.

4.1 TESTES E EXEMPLOS:

Exemplo_edicao.png
Descrição: Tela onde o usuário atualiza o nome de um cliente a partir do email.

Simulação: No menu "Editar Dados"

É preenchido: Email do cliente: lucas@email.com
Novo nome: Lucas M. Lima

ai é clicado em “Atualizar”

E o print é com a mensagem “Cliente inserido com sucesso!”

5. ARQUIVOS NECESSÁRIOS:

Para garantir o correto funcionamento da aplicação e facilitar a avaliação do projeto, o repositório deve conter os seguintes arquivos e diretórios:
Dados Iniciais: Utilizar dados reais de plataformas como o Kaggle, dados de e-commerce, vendas ou clientes.
Criar dados falsos (mock) diretamente via formulário na aplicação ou usando bibliotecas como Faker (opcional).

Dockerfile (se necessário)
Arquivo responsável por configurar o ambiente Docker da aplicação manualmente.
Exemplo de um Dockerfile: FROM python:3.10
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
CMD ["streamlit", "run", "app.py", "--server.port=8501", "--server.address=0.0.0.0"]

Docker-compose.yml (recomendado)
Permite subir simultaneamente o MongoDB e a aplicação em containers separados.
Exemplo de docker-compose.yml:
version: '3.8'
services:
  mongodb:
    image: mongo
    container_name: mongo-container
    ports:
      - "27017:27017"
    volumes:
      - mongo-data:/data/db
app:
    build: .
    container_name: streamlit-app
    ports:
      - "8501:8501"
    depends_on:
      - mongodb
volumes:
  mongo-data:

 app.py
Arquivo principal da aplicação em Streamlit, que implementa:
Conexão com MongoDB
Inserção de dados
Edição e exclusão
Consulta e concatenação de dados
Interface gráfica interativa

Exemplos/ (opcional)
Diretório contendo prints de tela ou GIFs que demonstram o uso real da aplicação, como:
Inserção de dados, visualização e edição, exclusão e concatenação
Resultados exibidos. Esses exemplos servem como guia visual para quem for testar a aplicação.

6. Estrutura Sugerida do Repositório
markdown
Copiar
Editar
E-Shop-Brasil/
├── README.md
├── Dockerfile
├── docker-compose.yml
├── app.py
├── requirements.txt
└── exemplos/
    ├── exemplo_insercao.png
    ├── exemplo_visualizacao.png
    ├── exemplo_edicao.png
    └── exemplo_delecao.png


7. CONCLUSÃO:
A implementação da solução proposta para a E-Shop Brasil demonstra, na prática, como tecnologias modernas de banco de dados e Big Data podem transformar operações de comércio eletrônico. Utilizando MongoDB em um ambiente containerizado com Docker e uma interface interativa desenvolvida em Streamlit, foi possível criar uma aplicação robusta, escalável e funcional para gerenciar dados de forma segura e eficiente. A aplicação permite desde a inserção e manipulação de dados até a visualização e concatenação de diferentes coleções, promovendo insights valiosos para decisões estratégicas em áreas como marketing, logística e vendas. Além disso, o uso de Docker garante portabilidade e padronização do ambiente, enquanto o MongoDB oferece flexibilidade e desempenho no tratamento de dados não estruturados. Com isso, a E-Shop Brasil estaria mais preparada para enfrentar os desafios de crescimento, personalização da experiência do cliente e eficiência logística, alinhando-se com as exigências da LGPD e garantindo uma base tecnológica sustentável para o futuro.









   









