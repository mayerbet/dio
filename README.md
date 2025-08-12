# 📦 Banco de Dados E-commerce

Este projeto é um modelo de banco de dados relacional para um sistema de **E-commerce**, desenvolvido como parte de um desafio da [DIO]  
O modelo foi criado no **MySQL Workbench** e busca representar de forma clara as entidades, relacionamentos e regras de negócio comuns em plataformas de venda online.

---

## 🛠 Tecnologias Utilizadas
- **MySQL** (Modelagem e script SQL)
- **MySQL Workbench** (Criação do DER e diagramas)
- **GitHub** (Versionamento e compartilhamento)

---

## 📐 Modelagem e Regras de Negócio

O modelo contempla:

### **1. Cliente PF e PJ**
- Uma conta pode ser **Pessoa Física (PF)** ou **Pessoa Jurídica (PJ)**.
- Um mesmo **email** não pode estar associado a mais de um cliente.
- Foi utilizada **herança por tabelas filhas**:
  - `Cliente` (dados comuns)
  - `ClientePF` (dados específicos como CPF, data de nascimento)
  - `ClientePJ` (dados específicos como CNPJ, razão social)
- Um cliente **não pode** ser PF e PJ ao mesmo tempo.

### **2. Pagamento**
- Um cliente pode ter **mais de uma forma de pagamento** cadastrada.
- Dados de cartão armazenam **número, nome, validade e bandeira**, sem armazenar o CVC por questões de segurança.
- Relacionamento **1:N** entre Cliente e Pagamento.
- A relação entre **Pedido e Pagamento** é:
  - **1:1** (pagamento único por pedido) ou


### **3. Entrega**
- Possui **status** e **código de rastreio**.
-Está diretamente ligada ao pedido (**1:1**)
- Inclui campos opcionais para **data de envio** e **Previsão entrega**.

---

## 📊 Diagrama Entidade-Relacionamento (DER)

---

## 🔑 Principais Entidades
- **Cliente**  
- **ClientePF**  
- **ClientePJ**  
- **Pagamento**  
- **Pedido**  
- **Entrega**  
- **Produtos**  
- **Fornecedor**  
- **Estoque**  

---

## 🚀 Como Executar
1. Clone o repositório:
   ```bash
   git clone https://github.com/SEU_USUARIO/seu-projeto.git
