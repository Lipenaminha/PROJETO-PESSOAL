# PROJETO-PESSOAL
# 🛍️ Sistema de Controle de Vendas (C#)

Este é um projeto desenvolvido em C# com o objetivo de treinar conceitos de **orientação a objetos (POO)** e **lógica de programação**. A aplicação permite o registro de vendas feitas por clientes, calculando o lucro obtido em cada uma delas.

## 📌 O que o sistema faz

- Permite cadastrar múltiplos clientes.
- Registra informações de um produto vendido, incluindo o valor de venda e o custo.
- Calcula o lucro de cada venda.
- Exibe um resumo com o nome do cliente, o nome do produto e o lucro obtido.

## 🧱 Estrutura do Projeto

O sistema está organizado com **quatro classes principais**:

### 🧑 Cliente
A classe `Cliente` representa o comprador. Ela armazena o nome da pessoa que realizou a compra.

### 📦 Produto
A classe `Produto` representa o item vendido. Ela guarda:
- O nome do produto
- O valor pelo qual ele foi vendido
- O custo de aquisição
Além disso, possui uma função que calcula o lucro da venda (diferença entre o valor vendido e o custo).

### 💰 Venda
A classe `Venda` representa a transação completa. Ela faz **composição** com as classes `Cliente` e `Produto`, ou seja, uma venda contém tanto o cliente quanto o produto associado.

Além disso:
- Calcula o lucro total da venda com base nas informações do produto.
- Sobrescreve o método `ToString()` para exibir um resumo legível das vendas.

### 🧩 Modelo
A classe `Modelo` contém informações sobre o produto, como:
- Nome do produto
- Tamanho
- Cor
- Modelo

Essa classe é usada dentro da classe `Venda` para detalhar o produto que foi comprado.

## 💡 Conceitos de Orientação a Objetos Utilizados

- **Encapsulamento**: cada classe tem suas próprias responsabilidades e dados internos, como o nome do cliente, o preço do produto, etc.
- **Composição**: em vez de usar herança, o projeto utiliza composição. Uma `Venda` contém um `Cliente`, um `Produto` e um `Modelo`.
- **Sobrescrita de Método**: o método `ToString` foi sobrescrito na classe `Venda` para apresentar os dados de maneira personalizada.
- **Organização em Objetos**: o projeto representa entidades reais (cliente, produto, venda, modelo) em forma de classes e objetos.

## 📊 Exemplo de Funcionamento

Ao executar o programa, o usuário informa quantos clientes deseja cadastrar. Para cada cliente, são solicitados:
- Nome do cliente
- Nome do produto comprado
- Valor pelo qual o produto foi vendido
- Custo do produto

Com essas informações, o programa armazena os dados e, ao final, exibe uma lista de todas as vendas com o lucro obtido em cada uma.
