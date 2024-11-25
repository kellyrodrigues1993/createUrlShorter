# 🌐 Encurtador de URL com AWS Lambda e S3


## Descrição

Este projeto implementa uma função **AWS Lambda** que recebe uma URL original e um tempo de expiração, gera um código curto único para essa URL e armazena as informações no **Amazon S3**. A função retorna o código curto gerado, que pode ser usado para acessar a URL original dentro do período de expiração especificado.

---

## 🚀 Funcionalidades

- **Geração de links curtos**: A função cria um código único para cada URL fornecida.
- **Armazenamento seguro no S3**: Os dados da URL (original e tempo de expiração) são armazenados no **Amazon S3** como um arquivo JSON.
- **Tempo de expiração configurável**: O usuário pode definir o tempo de expiração para o link curto, após o qual o link expirará.

---

## 🔧 Tecnologias Utilizadas

- **AWS Lambda**: Para executar a função sem a necessidade de servidores.
- **Amazon S3**: Para armazenar os dados das URLs e o tempo de expiração.
- **Java 17**: Linguagem de programação utilizada para implementar a função Lambda.
- **AWS SDK**: Para integração com os serviços da AWS.
- **Jackson**: Biblioteca para manipulação de JSON.

---

## 📋 Como Funciona

1. O usuário envia uma requisição POST para o endpoint da função Lambda, fornecendo a URL original e o tempo de expiração desejado.
2. A função Lambda gera um código curto único usando **UUID**.
3. A URL original e o tempo de expiração são armazenados no **S3** como um arquivo JSON.
4. A função retorna o código curto gerado, que pode ser utilizado para acessar a URL original dentro do período de expiração.

---

## 🚀 Como Rodar Localmente

git clone https://github.com/kellyrodrigues/create-url-shortener.git
cd create-url-shortener
