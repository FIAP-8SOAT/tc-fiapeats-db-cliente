# Fiapeats DB - Cliente
Repositório do banco de dados utilizado pelo microsserviço de cliente do projeto Fiapeats.

## Visão Geral do Projeto

Este projeto tem como objetivo implementar um sistema de autoatendimento para uma lanchonete em expansão. O sistema visa solucionar os problemas de gerenciamento de pedidos, como confusão entre atendentes e cozinha, erros nos pedidos e atrasos na entrega. Um banco de dados robusto é essencial para armazenar e gerenciar as informações relacionadas aos pedidos, produtos, clientes e categorias.

### Contexto do Problema

Com o crescimento da lanchonete, a falta de um sistema de controle de pedidos torna o atendimento caótico e ineficiente. Exemplos de problemas:

- Pedidos complexos mal interpretados ou esquecidos.
- Erros na entrega dos pedidos.
- Dificuldades em gerenciar estoques e garantir agilidade no atendimento.

A solução proposta é um sistema de autoatendimento que permita aos clientes realizarem seus pedidos de forma autônoma e precisa, integrando-se com um banco de dados para gerenciar eficientemente os dados.

---

## Por que um Banco de Dados Relacional?

Para este projeto, optamos por utilizar um banco de dados relacional devido aos seguintes motivos:

### 1. **Estruturação de Dados**
Bancos de dados relacionais oferecem uma estrutura bem definida com tabelas, colunas e relacionamentos. Isso permite organizar os dados de forma lógica e eficiente, essencial para gerenciar informações como pedidos, produtos, clientes e categorias.

### 2. **Integridade dos Dados**
Os bancos de dados relacionais garantem a integridade dos dados por meio de restrições como chaves primárias e estrangeiras. Isso assegura que relacionamentos, como entre pedidos e produtos, sejam mantidos corretamente.

### 3. **Consultas Avançadas**
Com a linguagem SQL, podemos realizar consultas complexas e detalhadas, permitindo recuperar informações específicas e gerar relatórios úteis para a gestão do negócio.

### 4. **Escalabilidade Vertical**
Embora sistemas relacionais possam ter limitações em grandes volumes distribuídos, eles são altamente eficazes em escalabilidade vertical, o que atende perfeitamente ao caso de uma lanchonete em expansão.

### 5. **Conformidade com Transações**
A conformidade com o modelo ACID (Atomicidade, Consistência, Isolamento e Durabilidade) é fundamental para garantir que as operações no banco de dados, como registros de pedidos, sejam realizadas de forma confiável e sem inconsistências.

Com essas características, um banco de dados relacional é a escolha ideal para garantir a organização, confiabilidade e eficiência no gerenciamento dos dados da lanchonete.

---

## Escolha do PostgreSQL

Optamos pelo **PostgreSQL** como o sistema gerenciador de banco de dados para este projeto devido a várias razões que se alinham com os requisitos do sistema:

### 1. **Confiabilidade e Robustez**
O PostgreSQL é conhecido por sua alta confiabilidade, garantindo que os dados sejam armazenados de forma segura e íntegra. Isso é fundamental em um ambiente onde os pedidos dos clientes devem ser gerenciados sem erros.

### 2. **Flexibilidade no Modelagem de Dados**
Com o suporte a diversos tipos de dados e funcionalidades como JSON, o PostgreSQL permite flexibilidade na modelagem de dados. Isso é útil para gerenciar informações complexas sobre produtos e pedidos personalizados.

### 3. **Desempenho e Escalabilidade**
Com capacidade de lidar com um grande volume de dados e conexões simultâneas, o PostgreSQL suporta o crescimento da lanchonete sem comprometer o desempenho.

### 4. **Integridade Referencial**
A gestão de chaves estrangeiras e restrições garante a integridade dos dados, como associar produtos corretamente aos pedidos e clientes às suas respectivas compras.

### 5. **Open Source e Comunidade Ativa**
Sendo um software de código aberto, o PostgreSQL oferece liberdade de uso sem custos de licenciamento, além de contar com uma comunidade ativa que disponibiliza documentação e suporte.

---

## Estrutura do Banco de Dados

#### 3. **Tabela `cliente`**
Registra os clientes que fazem pedidos no sistema.

| Campo       | Tipo       | Descrição                     |
|-------------|------------|---------------------------------|
| `documento`        | VARCHAR     | CPF/CNPJ do cliente |
| `nome`      | VARCHAR    | Nome do cliente               |
| `email`  | VARCHAR    | E-mail do cliente           |

---

## Benefícios do Banco de Dados na Solução do Problema

1. **Organização dos Pedidos**
   - O banco de dados garante que cada pedido seja registrado e associado ao cliente e aos produtos selecionados.
   
2. **Evita Erros e Confusões**
   - Com a integração do sistema com a cozinha, os pedidos são enviados de forma clara e precisa.

3. **Gestão de Estoque**
   - É possível rastrear os produtos mais vendidos e gerenciar os estoques de forma eficiente.

4. **Escalabilidade para Expansão**
   - O sistema suporta o aumento no volume de pedidos e clientes conforme a lanchonete expande.