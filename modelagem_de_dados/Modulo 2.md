# Bancos de Dados Relacionais: Conceitos e Modelo Entidade Relacionamento (MER)

No segundo módulo, apresentaremos os principais conceitos sobre os bancos de dados relacionais, que têm por finalidade armazenar e prover acessos a dados relacionados.

O modelo relacional foi criado para sanar dificuldades com dados desnecessários, provendo um padrão mundialmente seguido para buscar dados que poderiam ser utilizados por qualquer sistema, de modo eficiente, intuitivo e flexível, a fim de guardar e acessar os dados estruturados.

---

## Modelo Entidade Relacionamento (MER)

### Origem do MER

O Modelo Entidade Relacionamento (MER) foi criado em 1976 como uma maneira de unificação das visões de um banco de dados relacional, tendo por base a **Teoria Relacional**, desenvolvida em 1970.

Reconhecido como MER, o modelo recebeu vários aperfeiçoamentos ao longo dos anos, por outros estudiosos, os quais auxiliaram na evolução do metamodelo inicial. Com isso, traz uma abordagem conceitual e considera o mundo real como algo com **relacionamentos e entidades**.

Um elemento essencial do Modelo Entidade Relacionamento (MER) é o **Diagrama Entidade-Relacionamento (DER)**, que é a representação visual de objetos de dados.

### Abstração no MER

A maioria das extensões de um metamodelo tem como fundamento alguns métodos de abstração, como:

- **Agregação**
- **Classificação**
- **Generalização**

Esses métodos auxiliam na separação da realidade em partes importantes para o desenvolvimento do sistema, removendo peculiaridades que não influenciam o ambiente a ser modelado.

---

## Elementos do MER

O MER possui três classes de objetos principais:

1. **Entidades**
2. **Relacionamentos**
3. **Atributos**

### 1. Entidades

As **entidades** se referem a qualquer coisa do mundo que se pretende guardar informações. Elas podem ser de dois tipos principais:

#### Tipos de Entidades

- **Físico**: Pessoas físicas ou jurídicas, como empresas, fornecedores, funcionários e clientes.
- **Lógico**: Objetos materiais ou abstratos, como veículos, produtos, projetos, disciplinas, vendas, empréstimos ou viagens.

#### Representação Gráfica

Entidades são representadas por **retângulos** no Diagrama Entidade-Relacionamento, com um substantivo no singular, como “cliente”.

#### Classificação das Entidades

- **Entidades Fortes**: Não dependem de outras entidades para existir. Exemplo: “Produto”.
- **Entidades Fracas**: Dependem de outras entidades para existir. Exemplo: “Venda” depende de “Produto”.
- **Entidades Associativas**: Vinculam entidades a um relacionamento existente. Exemplo: “Item da Venda” relaciona “Produto” e “Venda”.

---

### 2. Relacionamentos

Os **relacionamentos** demonstram a associação entre entidades e o mundo real ou eventos que vinculam objetos existentes.

#### Representação Gráfica

No Diagrama Entidade-Relacionamento, relacionamentos são simbolizados por **losangos** e conectados às entidades com **linhas**.

#### Nomeação

Relacionamentos são nomeados por **verbos**, como “vende”, “trabalha” ou “contém”.

#### Cardinalidade

A cardinalidade define o grau de relação entre as entidades. Existem três tipos principais:

1. **Um para um (1:1)**: Exemplo: Um gerente chefia uma seção.
2. **Um para muitos (1:N)**: Exemplo: Uma seção pode ter vários funcionários.
3. **Muitos para muitos (N:N)**: Exemplo: Um fornecedor fornece vários produtos.

---

### 3. Atributos

Os **atributos** descrevem as características de uma entidade ou de um relacionamento. Cada atributo pertence a um **domínio**, que é o conjunto de valores válidos.

#### Classificação dos Atributos

1. **Chave (Identificador)**: Identifica de forma única uma ocorrência da entidade (Exemplo: CPF).
2. **Não Chave (Descritivo)**: Detalha características que não são únicas (Exemplo: Nome, Idade).
3. **Referencial**: Faz referência a outra entidade (Exemplo: RG de um cliente em uma venda).

#### Estrutura dos Atributos

- **Simples**: Determinado por apenas um atributo (Exemplo: Peso, Nome).
- **Composto**: Determinado por múltiplos atributos (Exemplo: Endereço = Rua + Bairro + Cidade).
- **Multivalorado**: Possui mais de um valor (Exemplo: Telefones de um cliente).
- **Derivado**: Calculado a partir de outro atributo (Exemplo: Idade derivada de Data de Nascimento).
- **Determinante**: Distingue uma entidade de forma única (Exemplo: Matrícula, CNPJ).

---

## Diagrama Entidade-Relacionamento (DER)

### O que é o DER?

O **DER** (Diagrama Entidade-Relacionamento) é a representação gráfica do MER, usada para tornar concretas as abstrações do modelo.

#### Diferença entre MER e DER

- **MER**: Modelo conceitual, abstrato.
- **DER**: Representação gráfica do MER, similar a um fluxograma.

#### Elementos Gráficos no DER

- **Retângulo**: Representa entidades.
- **Elipse**: Representa atributos.
- **Losango**: Representa relacionamentos.
- **Linha**: Conecta entidades e relacionamentos.

---

## Generalização e Especialização

Essas extensões do MER são usadas para representar hierarquias entre entidades com atributos em comum.

- **Generalização**: Combina entidades com atributos semelhantes em uma única entidade genérica.  
  Exemplo: Entidades “Carro” e “Moto” podem ser generalizadas para “Veículo”.

- **Especialização**: Divide uma entidade genérica em subentidades com características específicas.  
  Exemplo: Entidade “Médico” pode ser especializada em “Médico Residente” e “Médico Efetivo”.

---

## Condicionalidade de Relacionamento e Autorrelacionamento

### Condicionalidade de Relacionamento

Define quando uma entidade pode ou não se relacionar com outra. Exemplos:

- Participação **total**: Uma entidade sempre participa de um relacionamento.
- Participação **parcial**: Uma entidade pode ou não participar de um relacionamento.

### Autorrelacionamento

Ocorre quando uma entidade está associada a si mesma.  
Exemplo: Uma entidade “Funcionário” pode estar relacionada a outra ocorrência da mesma entidade, como “Chefe” e “Subordinado”.
