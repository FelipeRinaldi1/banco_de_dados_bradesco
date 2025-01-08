# Resumo: Modelagem de Banco de Dados Relacional

## 1. Introdução

Durante a modelagem de banco de dados, é essencial considerar desde a criação da ideia até sua execução prática para que o projeto funcione na realidade. Nesse contexto, a integridade do banco de dados é crucial, e Edgar Codd estabeleceu 12 regras que definem bancos relacionais. Além disso, restrições de integridade garantem a consistência e a exatidão dos dados.

---

## 2. 12 Regras de Codd para Bancos Relacionais

### Regra 0

Um banco de dados precisa ser categorizado como um sistema de gerenciamento relacional.

### Regra 1

Os dados devem ser apresentados em nível lógico, por meio de tabelas.

### Regra 2

Os dados devem ser acessíveis logicamente por uma combinação de nome de tabela, coluna e chave.

### Regra 3

Deve haver suporte a valores nulos, indicando ausência de dados.

### Regra 4

O catálogo de dados deve ser baseado no modelo relacional.

### Regra 5

O SGBD deve ter uma linguagem para definição, manipulação e detalhamento de dados.

### Regra 6

O sistema deve tratar atualizações em visões de dados.

### Regra 7

Deve haver suporte para operações de alto nível como inserção, exclusão e atualização.

### Regra 8

Mudanças físicas, como armazenamento, devem ser independentes dos dados.

### Regra 9

Os dados lógicos devem ser independentes de alterações nas tabelas básicas.

### Regra 10

As regras de integridade devem ser independentes.

### Regra 11

O banco deve permitir independência de distribuição de dados.

### Regra 12

As regras de integridade não devem ser transpostas em linguagens de baixo nível.

---

## 3. Restrições de Integridade

As restrições de integridade mantêm a consistência e exatidão dos dados em um banco de dados. São categorizadas em cinco tipos:

### 3.1. **Integridade Referencial**

Garante que registros filhos tenham um registro pai correspondente, usando chaves estrangeiras.

### 3.2. **Integridade de Vazio**

Determina se o preenchimento de uma coluna é obrigatório ou opcional, permitindo valores nulos.

### 3.3. **Integridade de Chave**

Garante que os valores de chaves primárias sejam únicos e não nulos, preservando registros distintos.

### 3.4. **Integridade Definida pelo Usuário**

Permite a criação de regras personalizadas de acordo com as necessidades do negócio.

### 3.5. **Integridade de Domínio**

Refere-se ao tipo de dado permitido em uma coluna, como valores monetários, datas ou textos, garantindo consistência.

---

## 4. Tipos de Restrições

As restrições são aplicadas para garantir a validade dos dados armazenados:

- **Check:** Valida os dados com base em expressões lógicas (e.g., maior ou menor que).
- **Nulidade:** Determina se os valores de uma coluna podem ser nulos ou não.
- **Unicidade:** Garante que combinações de atributos sejam únicas.
- **Unique:** Exige que os valores de uma coluna sejam distintos.
- **Default:** Define valores padrões para colunas.
