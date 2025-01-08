# Introdução ao Banco de Dados

## Banco de Dados

Modelagem de dados é usado para determinar as regras de negocio e a arquitetura de um BD
descreve as estruturas logicas e fisicas
É uma abstração de informações de uma realidade (minimundo)
se divide em 3 modelos:

Conceitual,Logico e Fisico.

modelo de tarefas do usuario: **definição de regras e tecnologia**, relatorio descritivo do processo da tarefa do usuario
|
V
Modelo Conceitual: **Regras de negocio**, Ferramentas ou objetos, propiredades tecnicas e processos, mapeamento do dominio do usuario
|
V
Modelo Lógico: **Definição de regras e tecnologia**, definição de dados, funções e Projetos de regras
|
V
Modelo Físico: **Implementação** Pode representar tanto o projeto como a propria interface gráfica, o banco de dados e os programas.

SGBD (Sistema de gerenciamento de banco de dados), ele pode fazer alterações de dados

_ "o uso de um SGBD permite executar várias operações com os arquivos,
como deletar os que que já existem no banco de dados ou criar arquivos novos. Mas
também é possível deletar apenas os dados de algum arquivo existente, modificar
ou acrescentar dados"
"Dentro dessas funções, é possível verificar que a função do SGBD será a de manejar
tudo o que ele armazena. Continue conosco para saber sobre mais conceitos da
Modelagem de Dados!" _

### Minimundos e abstrações

"Minimundo ou regras de negócio (RN) é a criação de um documento com uma
descrição textual curta, que acontece a partir de determinadas informações. Nele,
é descrito os dados de como as coisas devem funcionar."

"Abstração, por sua vez, refere-se à “visão” que surge mentalmente com base em
qualquer realidade. Assim, o ato de abstrair consiste no processo mental utilizado
para selecionar características de objetos e situações, sendo que algumas serão
excluídas por não apresentarem relevância ao contexto."

--O minimundo é uma esquematização da realidade, e a abstração é como uma representação mental desta realidade.--

### Sistema de Gerenciamento de Banco de Dados (SGBD)

Exemplos de SGBDs: OracleDB, PostgreSQL, MySQL, MS SQLServer.

Cada SGBD tem que possuir pelo menos 4 elementos:
Dados: Info armazenadas no banco de dados
Software: Camada de software entre usuarios e banco de dados (Sendo esse o SGBD)
Hardware: Volumes de memoria secundários
Usuários: Existem 3 tipos principais: No topo está o programador, seguido do usuário final, e finalizando há o administrador do banco de dados conhecido por: DBA.

### Banco de Dados.

**O banco de dados nada mais é que um repositório para armazenar informações (dados) de qualquer natureza. Ele retrata aspectos do mundo real — ou seja, o conceito visto anteriormente de minimundo — em que qualquer mudança que se faça no minimundo é diretamente replicada no banco de dados.**

É normal chamar um banco de dados como "persistente" mesmo que não durem por muito tempo. Quando é persistente se sugere que as informações
contidas nele se dinstinguem quanto a tipos de dados temporarios, ou seja, qualquer dado que seja breve. EX: Dados de saida, entrada de bloco de controle de software, filas de trabalho, resultados intermediarios e instruções SQL

"Os dados persistem quando são aceitos pelo SGBD para a inserção no banco. Assim, somente será possível removê-los do banco, posteriormente, por meio de alguma solicitação explícita ao SGBD."

Os bancos de dados podem ser categorizados de varias maneiras de acordo com a sua arquitetura.

**Centralizada:** Aplicações ou clientes podem acessar o banco de dados. Precisa de alto processamento de servidor e um otimo desemenho do SGBD

Descentralizada: Há + de 1 servidor para o BD, sendo descentralizado. Garante autonomia local e auxilio na comunicação.

Distribuida: Dados compartilhados em muitos computadores e servidores. atualizações ou sincronismo para se certificar da integridade dos dados.

Replicada: essa arquitetura é copiado para muitos computadores ou servidores, metodologia de espelhamento. todos são identicos, quando altera no primeiro os outros são alterados em cascata. Garante a segurança das informações. Caso haja falha de algum host outro podera assumir seu lugar.

### Modelo Conceitual

Utiliza a analise dos recursos como base. Grupo de hipoteses do mund oreal. indica as regras de negocio do sistema.
Consiste no detalhamento de alto nivel para entender e descrever os detalhes da organização. (Escopo do projeto)

"É importante frisar que esse modelo não foca em questões como a abordagem
do banco de dados que será escolhida, nem em como será acessado ou quais
estruturas físicas serão desenvolvidas pelo SGBD.
A representação gráfica do modelo retrata determinada realidade em um contexto
e suas estruturas de dados, observe."

1 cliente realiza N compras
1 aluno possui N Matriculas
N professor leciona N aulas.

é a entidade relacionamento para banco de dados.

### Modelo lógico

Inicia qndo o modelo conceitual estiver concluido. Apresenta questoes referentes as possibildiades de abordagens tecnologicas do SGBD para
criar a logica dos relacionamentos que tem no modelo conceitual.

Detalha a forma lógica, relações entidades etc. Existem no banco de dados conforme a forma da abordagem.
A sua representação é um esquema lógico, possui tabelas, campos, chaves primarias.
*nome da tabela
*variaveis

*chave primária (chave primaria, todos precisam ter pelo menos 1.)
*chave estrangeira (Chave primaria colocada em outra tabela, para fazer o relacionamento.)

1:N O lado N recebe a FK (chave estrangeira)
N:N Nova tabela (a nova tabela recebe as duas chaves primarias, tendo assim apenas as 2 chaves estrangeiras)
1:1 União de Tabelas (junta as duas tabelas)

### Modelo físico.

Só é criado quando temos o lógico. Detalhamento de estruturas fisicas de deositos de dados, como tamanho dos campos.

um modelo fisico é composto por:
Estruturas físicas de depositos de dados
Requisitos de tratamentos
Utilização acessivel dos recursos tecnologicos

O modelo físico consiste na fase final, ou seja, aquela que antecede a criação de banco de dados, considerado como um aperfeiçoamento do modelo lógico.

Sempre que há chave estrangeira em alguma tabela, voce deve deixar elas para fazer por ULTIMO

### Vantagens de utilizar um banco de dados

*Velocidade
*Densidade
*Trabalho menos monótono
*Melhora de relacionamentos e produtividade
*Atualidade
*Proteção
*Reduz riscos na Operação
*Maior precisão nas decisões

As vantagens apresentadas são de aplicabilidade em escala maior nos ambientes de sistemas multiusuário, ou seja, em que o sistema de banco de dados será acessado por vários usuários simultaneamente.

"A primeira delas é o compartilhamento de dados. Esta partilha não é apenas
em relação aos sistemas existentes, mas sim para que possam compartilhar
informações de banco de dados."

"A segunda vantagem é a redução da redundância quando necessário. Em SGBD,
cada aplicação tem seus arquivos privados, podendo, com isso, haver um número
considerável de informações redundantes (repetidas), levando a um desperdício
no espaço de armazenamento. Mas, por meio da integração de arquivos, pode-se
reduzir essas redundâncias."

"A terceira vantagem, a qual o SGBD garantirá que um banco de dados dificilmente se
torne inconsistente para o usuário, certificando-se de que as mudanças em uma de
suas entradas sejam replicadas automaticamente para a outra entrada, realizando
a propagação das atualizações."

"A quarta vantagem é que poderá ser fornecido um suporte às transações.
Uma transação se refere a uma unidade lógica de trabalho de banco de dados
que, normalmente, contém várias operações desses bancos, principalmente as
relacionadas às alterações. Por exemplo, uma das possibilidades de suporte em
transações destaca a transferência bancária de um valor localizado na conta Y para
a conta X. Tal situação exige, pelo menos, duas operações:

*uma para retirar da conta Y;
*outra para depositar na conta X."

"Por fim, temos a última e quinta vantagem, que é a preservação da integridade. Isso
se deve, porque, observando o controle centralizado aplicado ao banco de dados,
ainda que não existam inconsistências entre as duas entradas que deveriam conter
o mesmo valor, o banco poderá ter informações incorretas, como um produto com
nome que não existe ou um funcionário com 800 horas de trabalho em um dia em
vez de oito horas."

### Teoria Relacional, Tabelas, Campos e Registros

Nos conceitos relacionais, a tabela (relação) diz respeito a um grupo de dados organizados em colunas (atributos) e linhas (tuplas).

Colunas simbolizam um atributo de dados, linhas o valor desse atributo, juntos geram um registro de uma tabela.
de acordo com a teoria relacional, há regras que determinam uma tabela de dados:

-Relação: É como cada tabela é referenciada;
-Tupla: Refere-se ao grupo de linhas que compõe a tabela.
-Colunas: Serão Nomeadas e retratam um domínio da tabela.

+outros pontos:
1- Não importa a disposição (organização) das linhas, pois não existirão linhas idênticas.
2- É necessário utilizar nomes para referenciar as colunas, não importando sua disposição (ordem).
3- Não haverá tabelas com nomes iguais no mesmo banco de dados, sendo que cada uma terá um nome diferente.
4- Outro conceito é a entidade, que se refere a qualquer objeto, coisa ou pessoa abstraído de alguma realidade para pertencer a uma tabela e guardar seus dados.
5- As colunas de uma tabela se referem aos seus componentes e valores, os quais devem ser indivisíveis.
Isso significa que não há colunas da espécie subgrupo, pois são elementos importantes que não autorizam a ocorrência múltipla de valores.

### Domínio

Consiste em ser um grupo de valores, a maioria das vezs infinito, que são determinados e nomeados, cujos atributos assumem os valores contidos.
Possivel definir separadamente das entidades, permitindo sua reutilização e padrão.
Domínio é um grupo com valores atômicos referente as uma coluna e sua tabela

ex:
aniversário: grupo de 8 digitos
celular: grupo de 11 digitos
rg: grupo de 10 digitos
setor: grupo de setores em uma organização.

idade: numero inteiro entre 0 e 140
celular: (XXX) XXXXX-XXXX, em que X = {0,1...9}

"
Na Prática
As restrições de domínio consideram por base a definição dos domínios de valores para todas as colunas de uma tabela. Geralmente, estabelecem-se e determinam os valores que uma tabela terá, resultando no domínio da coluna.

Essa situação possibilita, por exemplo, que os valores de determinado banco sejam revisados e certifica que as comparações tenham sentido ao realizar a validação das consultas.
"

é normal domínio ser definido por tipos de dados padrões, por exemplo: int, float, date, char, time, entre outros.

### Chave Primária

haverá uma coluna que sua chave nunca se repetirá determinado valor em outra linha, assim ao escolher um campo para ser a chave primária
sera passada a informação ao banco de dados de que não deverá haver dois registros c valor iguais.

Logo, uma tabela pode ter apenas uma chave primária, que costuma ser referenciada como COD, ID ou algo do tipo. De modo geral, ela será criada quando uma tabela possuir os seguintes propósitos:

-Unidade: Registro seja unico
-Valor: Registro não seja nulo
-Identificação: Registro possibilite a identificação da tabela

Chaves primárias podem ser divididas em 2 categorias:

Chave simples: É constituída de um único campo da tabela em que não terá dois valores ou o mesmo valor para mais de um registro.
Este não poderá ser nulo.
Chave Composta: É constituída por mais de um campo da tabela em que os valores poderão se repetir, mas não poderá haver combinações desses valores.

### Chave Estrangeira

Ela faz a ligação entre diferentes tabelas. Quando ha uma chave primária de uma tabela que pertence, igualmente aos campo s de outra tabela,
ocorre a referenciação de um componente em relação ao outro, em uma segunda tabela

objetivos:
Valor: Impossibilitar que seja adicionado no ID de uma tabela um valor não válido
Registro: Impossibilitar que seja deletado um registro referenciado em outra tabela.

+Chave estrangeiras possuem quantas chaves forem necessarias para referenciar as ligações em outras tabelas

### Normalização

A normalização consiste no conjunto de regras que buscam a organização de um projeto de BDD, reduzindo informações
ampliar a integridade e o desempenho. Apresenta os passo s para revisar os atributos de uma entidade, sua finalidade é impedir anomalias encontradas em rotinas de exclusão, alteração ou inclusão de registros no banco.

Podemos entender que a normalização impede que possíveis falhas no projeto de banco surjam, auxiliando na eliminação de mescla de assuntos e redundâncias desnecessárias referentes à essa mistura.

Nisso, varias regras são aplicadas nas tabelas para validar se estao estruturadas de acordo com o projeto de banco.
São 5 regras mas apenas as 1FN,2FN e 3FN são utilizadas.

Primeira Forma Normal (1FN)
É Uma tabela com todas as colunas compostas por um unico valor, não contendo algum grupo de colunas repetidas com atributos compostos ou em
uma linha. Utilizar 1FN consiste em remover da estrutura tds os itens repetidos.
(isso consiste em separar as funções. Em vez de ter uma tabela com tudo de um cliente, dividir em 2, a tabela clientes e a tabela telefones_clientes)

Segunda Forma Normal (2FN)
Tabela classificada como 1FN e que contém atributos que não participam da chave primária, mas dependem dela. Dessa forma, aplica-se a 2FN, que seria a remoção dos atributos. Com uma chave composta, ou seja, uma chave primária constituída por mais de um campo, todos os dados dependem apenas de alguma de sua parte.

Terceira Forma Normal (3FN)
Tabela classificada com 2FN e sem campos que dependem de outros tidos como não chaves. Em outras palavras, não pode haver atributos que não são chaves ligados a outros atributos não chaves, pois pode ocasionar anomalias de exclusão, inclusão ou alteração.
Sendo assim, aplica-se a 3FN, que consiste em remover da estrutura esses campos que dependem de outros campos que não são chaves.

https://www.youtube.com/watch?v=8CkMX2qXgdY
