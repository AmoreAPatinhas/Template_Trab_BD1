# TRABALHO 01: Amor&Partinhas
Trabalho desenvolvido durante a disciplina de BD1

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Isabella Bissoli: <isabellabg244@gmail.com><br>
Isabella Sampaio: <isabellasmsantos47@gmail.com><br>
Ludmila Dias: ludmiladias.inf@gmail.com <br>
Marcela Starling: marcela.sfl@hotmail.com <br>
Renzo Avance: <renzogavance@gmail.com><br>


### 2.INTRODUÇÃO E MOTIVAÇÃO<br>
Este documento contém a especificação do projeto do banco de dados Amor&Patinhas

> É de extrema importância ter um sistema eficiente de controle para auxiliar os administradores e voluntários no gerenciamento das atividades internas e na vida dos animais. O abrigo Amor&Patinhas atua não apenas como um lar temporário para esses animais, mas também como uma porta de entrada para que eles encontrem famílias amorosas e tenham uma segunda chance na vida. Todo animal ao chegar no abrigo, necessita de uma identificação e tratamento digno enquanto estiver em vida.
 

### 3.MINI-MUNDO<br>

> Todo animal ao chegar no abrigo, necessita que um administrador o cadastre com algumas informações básicas para ser identificado, como a raça, nome, data que chegou ao abrigo, cor, pelagem e espécie (as espécies dos animais devem ser diferenciadas através de códigos). A espécie do animal se distingue por Gato ou Cachorro. Já a raça, informa a família do animal (exemplo: vira-lata, siamês, golden retriever...)
 
> Do sistema espera-se que seja possível que o administrador cadastre também os voluntários que tenham interesse para ajudar nas atividades do abrigo e no cuidado dos animais. Ao demonstrar interesse, esse voluntário se torna um funcionário do abrigo e pode contribuir de várias formas, caso tenha alguma formação na área animal (como um veterinário), poderá auxiliar em consultas, aplicação e dosagem de remédios. Caso não tenha, é alocado para manutenções gerais, limpeza, alimentação e banho. Deve ser possível inserir os dados dos funcionários do abrigo, colocando nome, cpf, telefone, email, endereço e ocupação (onde irá atuar no abrigo, qual tarefa…) para que assim seja possível controlar a entrada e saída de pessoas no abrigo e sua atuação.
Todos os funcionários devem estar vinculados a nenhum animal ou vários, pois pode ser possível que um voluntário queira ficar a disposição apenas para a limpeza do abrigo. O animal pode estar relacionado a um ou vários funcionários, pois pode existir a necessidade de ter um veterinário supervisionando e outro funcionário dando banho e comida. 
O sistema deve possibilitar que o administrador ou o voluntário gere uma ficha, ou histórico, do animal (caso requisitado pelo usuário), contendo todas as informações que foram cadastradas do mesmo, para facilidade de visualização e controle

> O sistema de adoção funciona da seguinte forma: O administrador poderá vincular o adotante ao animal, confirmando o processo de adoção. Para controle, antes do vinculo ocorrer, um cadastro do adotante deve ser feito no sistema com as informações: Nome, telefone, CPF, email e endereço. Dentro da tela individual do animal, deve ter a possibilidade de vincular o animal ao adotante, sendo que um voluntário também pode se tornar um adotante

### 4.PROTOTIPAÇÃO, PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS<br>

#### 4.1 RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>

> Menu e login

![Captura de tela 2023-05-31 102636](https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/assets/95357142/3c345d7a-b359-4c93-9806-3d53029db0bf)


> Menu principal e Edição de dados

![Captura de tela 2023-05-31 102707](https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/assets/95357142/3b2eb39c-4632-43a9-94d4-135a52772688)


> Informações do animal e dados médicos de cada

![Captura de tela 2023-05-31 102743](https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/assets/95357142/22398020-9125-4c7a-b781-c95fb1e93d0d)

 
> Cronograma de tratamentos e agendamentos

![Captura de tela 2023-05-31 102810](https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/assets/95357142/cc5b94c9-dee6-42ec-bb6d-1378a3dfd9ad)


> Cadastrar animal e voluntário

![Captura de tela 2023-05-31 102926](https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/assets/95357142/016d7c83-162f-4257-b317-8391200cf82c)

#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    
> A Empresa Amor&Patinhas precisa inicialmente dos seguintes relatórios:
* Relatório relativo ao animal, contendo informações como data de cheagada no abrigo, raça, pelagem, espécie, etc.
* Relatório que mostre o tipo de tratamento que o animal precisa.
* Relatório que mostre qual animal foi adotado e quem foi o responsável pela adoção. 
* Relatório relativo a quantidade de funcionários que atuam no abrigo e qual o papel estes desempenham.
* Relatório relativo às informações dos adotantes. 
 
#### 4.3 TABELA DE DADOS DO SISTEMA:

[DATABASE.xlsx](https://github.com/AmoreAPatinhas/Template_Trab_BD1/files/11630299/DATABASE.xlsx)
        
### 5.MODELO CONCEITUAL<br>

Principais entidades: Animal, Funcionário e Adotante

Relacionamentos Principais:

> Cuida (Funcionários/Animal):
1) Um funcionário cuida de um ou vários animais
2) Um animal é cuidado por um ou vários funcionários

> Adota (Interessado/Animal):
1) Um interessado adota um animal ou vários
2) Um animal pode ser adotado por apenas um adotante ou por ninguém


> Realiza (Necessitado/Castração):
1) Um necessitado realiza nenhuma ou apenas uma castração
2) Um código de castração está ligado (pode ser ligado) a um animal necessitad
    
![MODELO CONCEITUAL CERTO](https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/assets/95357142/cfb22bd0-dae1-4c19-b728-b1ea92bad290)
       
#### 5.1 Validação do Modelo Conceitual
#### [PathFinder]: Eduardo Próspero, Lucas Vieira, Mattheus Colares, Victor Oliveira Santos:
##### Considerações do grupo: 
> Pontos a serem ajustados:
> * Adicionar o atributo "idade" para a entidade "animal" no modelo conceitual.
> * Separar a entidade "administrador" do conceito geral de "funcionário" para refletir suas interações exclusivas.
> * Criar uma entidade para armazenar os tipos de funcionários, permitindo especificar suas funções.
> * Indicar a existência de mais de um administrador no sistema.
> * Considerar o endereço como entidade, seguindo a forma normal 1.
>
> No geral, o modelo é organizado e compreensível, com ajustes pontuais a serem feitos.
--------------------------------------
#### [CarCents]: Kailany Faustino, Lucas Codeco, Micaely Gusmão, Richard Lucas
##### Considerações do grupo: 
> O trabalho está muito bem estruturado, tendo em vista que avaliamos apenas a relação do mini mundo com o modelo conceitual. Talvez o procedimento devesse ter alguma relação com funcionário, mas isso vai do que foi definido pelo grupo. Muito bom!

#### 5.2 Descrição dos dados 

 * FUNCIONÁRIO: Identificação das informações do funcionário voluntário do abrigo para segurança e organização

 * ANIMAL: Identificação das informações de cada animal que chega no abrigo para controle da quantidade e de cad aum individualmente

 * ESPÉCIE: Identifica se o animal que chegou é Cachorro ou Gato

 * ENDEREÇO: Serve para identificarmos o endereço do funcionário e do adotante para segurança do abrigo

 * ADOTANTE: código do adotante, nome do adotante, cpf, email, endereço

 * ANIMAL ADOTANTE: código a adoção, código do adotante, código do animal, data da adoção

 * PROCEDIMENTO: código do procedimento, código do animal, descrição e data

 * TIPO DE TRATAMENTO: código de tratamento e descrição


### 6	MODELO LÓGICO<br>

![modelo logico](https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/assets/130158423/be605034-fd7c-4711-becd-6e3a3f547e57)

### 7	MODELO FÍSICO<br>

```
CREATE TABLE ANIMAL(
  ID_ANIMAL INT PRIMARY KEY,
  RACA VARCHAR(50),
  NOME VARCHAR(50),
  DATA_CHEGADA DATE,
  PELAGEM VARCHAR(100),
  CODIGO_ESPECIE INT, 
  CODIGO_FUNCIONARIO INT,
  FOREIGN KEY (CODIGO_FUNCIONARIO) REFERENCES FUNCIONARIO(CODIGO_FUNCIONARIOS),
  FOREIGN KEY (CODIGO_ESPECIE) REFERENCES ESPECIE(ID_ESPECIE)
);

CREATE TABLE ANIMAL_ADOTANTE(
 CODIGO_ADOCAO INT PRIMARY KEY,
 CODIGO_ADOTANTE INT,
 CODIGO_ANIMAL INT,
 DATA_ADOCAO DATE,
 FOREIGN KEY (CODIGO_ADOTANTE) REFERENCES ADOTANTE(CODIGO_ADOTANTE),
 FOREIGN KEY (CODIGO_ANIMAL) REFERENCES ANIMAL(ID_ANIMAL)
);

CREATE TABLE PROCEDIMENTO(
 ID_TRATAMENTO INT,
 ID_ANIMAL INT,
 DESCRICAO VARCHAR(100),
 DATA_HORA DATE,
 FOREIGN KEY (ID_ANIMAL) REFERENCES ANIMAL(ID_ANIMAL),
 FOREIGN KEY (ID_TRATAMENTO) REFERENCES TIPO_TRATAMENTO(ID_TRATAMENTO)
);

CREATE TABLE ADOTANTE(
 CODIGO_ADOTANTE INT PRIMARY KEY,
 NOME_ADOTANTE VARCHAR(50),
 TELEFONE_ADOTANTE VARCHAR(15),
 CPF_ADOTANTE VARCHAR (10),
 EMAIL_ADOTANTE VARCHAR(50),
 CODIGO_ENDERECO INT,
 FOREIGN KEY (CODIGO_ENDERECO) REFERENCES ENDERECO(CODIGO_ENDERECO)
);

CREATE TABLE ENDERECO(
 CODIGO_ENDERECO INT PRIMARY KEY,
 NOME_LOUGRADOURO VARCHAR(100),
 NUMERO INT,
 COMPLEMENTO INT,
 NOME_BAIRRO VARCHAR(100),
 NOME_MUNICIPIO VARCHAR(100)
);

CREATE TABLE TIPO_TRATAMENTO(
 ID_TRATAMENTO INT PRIMARY KEY,
 DESCRICAO VARCHAR(100)
);

CREATE TABLE ESPECIE(
 ID_ESPECIE INT PRIMARY KEY,
 TIPO_ESPECIE VARCHAR(100)
);

CREATE TABLE FUNCIONARIO (
 CODIGO_FUNCIONARIOS INT PRIMARY KEY,
 NOME_FUNCIONARIO VARCHAR(500),
 TELEFONE_FUNCIONARIO VARCHAR(15),
 EMAIL_FUNCIONARIO VARCHAR(50),
 OCUPACAO VARCHAR(50)
);

```
       
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>

```
INSERT INTO ANIMAL (id_animal, raca, nome, data_chegada, pelagem, codigo_especie, codigo_funcionario)
VALUES
  ('1', 'Vira-Lata', 'banana', '2022-04-29','Pelagem curta',  '1', 1),
  ('2', 'Golden Retriver', 'kika', '2023-03-31', 'Pelagem Longa', '1', 2),
  ('3', 'Angorá', 'floquinho', '2022-05-02', 'Pelagem média', '2', 2),
  ('4', 'Somali', 'rex', '2023-02-10', 'Pelagem Média', '2', 3),
  ('5', 'Border Collie', 'luci', '2023-03-04', 'Pelagem Longa', '1', 4),
  ('6', 'Britsh Longhair', 'amora', '2023-04-03', 'Pelagem Longa', '2', 5);

INSERT INTO ANIMAL_ADOTANTE(codigo_adocao, codigo_adotante, codigo_animal, data_adocao)
VALUES
 (1, 2, 1, '2022-10-12'),
 (2, 1, 2, '2023-05-14'),
 (3, 4, 5, '2023-03-01'),
 (4, 3, 4, '2022-11-25');

INSERT INTO PROCEDIMENTO (id_tratamento, id_animal, descricao, data_hora)
VALUES
 (3, 1, 'castracao agendada', '2023-04-24 13:00'),
 (1, 5, 'vaciana de tetano', '2023-05-10 13:00'),
 (2, 4, 'medicacao de dor', NULL),
 (3, 2, 'castracao agendada', '2023-08-03 13:00');

INSERT INTO ADOTANTE(codigo_adotante, nome_adotante, telefone_adotante, cpf_adotante, email_adotante, codigo_endereco)
VALUES
 (1, 'Andrea Cardoso', '27983293861', '286.464.205-07', 'andrea_card@gmail.com', 1),
 (2, 'Julia Teixeira de Castro', '27996997958', '530.949.381-67', 'juju_tex123@gmail.com', 3),
 (3, 'Luis Edson', '27999893304', '342.586.906-00', 'luisEd@yahoo.com.br', 1),
 (4, 'Elza Costa', '27999402349', '734.251.972-31', 'elza12344@gmail.com', 3);

INSERT INTO ENDERECO VALUES(3,'Rua Loureiro Nunes',444, 204,'Mata da Praia','Vitória');

INSERT INTO TIPO_TRATAMENTO(id_tratamento, descricao)
VALUES
 ('1', 'vacinacao'),
 ('2', 'remedio'),
 ('3', 'castracao');


INSERT INTO ESPECIES values (1,'Cachorro');
INSERT INTO ESPECIES values (2,'Gato');

INSERT INTO FUNCIONARIO (codigo_funcionarios, nome_funcionario, telefone_funcionario, email_funcionario, ocupacao)
VALUES
  (1, 'Isabel E.', '2799444756', 'isabelly123@gmail.com', 'Médica Veterinária'),
  (2, 'Flávia M.', '2799291824', 'flaviaMS47@hotmail.com', 'Atendente'),
  (3, 'Breno G.', '2798599222', 'breno_guigui@yahoo.com.br', 'Atendente');
  
INSERT INTO FUNCIONARIO (codigo_funcionarios, nome_funcionario, telefone_funcionario, email_funcionario, ocupacao)
VALUES
  (4, 'Igor Daniel.', '27999495478', 'igor_sales@ifes.edu.br', 'Técnico de TI'),
  (5, 'Antônia Sebastiana', '27994614738', 'antoniaSebas23@gmail.com', 'Cirugiã Veterinária'),
  (6, 'Maitê Sara', '27983414394', 'maitêSaf@outlook.com', 'Técnica');
 
```

### 9	TABELAS E PRINCIPAIS CONSULTAS<br>

#### Link do Colab: https://colab.research.google.com/drive/1Xa8sNnJWlX7lkmoH0PHXi7EGnG9m5GUN?usp=sharing

#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>

![arte 1](https://github.com/AmoreAPatinhas/Template_Trab_BD1/assets/71940799/e861c29a-f43d-4b3a-a62d-b8a84c46ff4c)
--------------------------------------
![arte 2](https://github.com/AmoreAPatinhas/Template_Trab_BD1/assets/71940799/f77a01bf-129b-44ad-bee6-4014f215abc2)
--------------------------------------
![arte 3](https://github.com/AmoreAPatinhas/Template_Trab_BD1/assets/71940799/56fc1328-4b98-4b4a-a217-bf0aa67a663a)
--------------------------------------
![arte 4](https://github.com/AmoreAPatinhas/Template_Trab_BD1/assets/71940799/15a3a05f-1918-4f79-b57a-0e9de792e83c)
--------------------------------------
![arte 5](https://github.com/AmoreAPatinhas/Template_Trab_BD1/assets/71940799/d715393c-d87f-4289-8b25-6c3d9170d010)

># Marco de Entrega 01: Do item 1 até o item 9.1<br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
    a) Criar minimo 3 de exclusão
    b) Criar minimo 3 de atualização

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
    a) Criar minimo 2 envolvendo algum tipo de junção

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
    a) Criar minimo 1 de cada tipo

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
     a) Criar minimo 1 envolvendo GROUP BY
     b) Criar minimo 1 envolvendo algum tipo de junção

># Marco de Entrega 02: Do item 9.2 até o ítem 9.10<br>

### 10 RELATÓRIOS E GRÁFICOS

#### a) análises e resultados provenientes do banco de dados desenvolvido (usar modelo disponível)
#### b) link com exemplo de relatórios será disponiblizado pelo professor no AVA
#### OBS: Esta é uma atividade de grande relevância no contexto do trabalho. Mantenha o foco nos 5 principais relatórios/resultados visando obter o melhor resultado possível.

    

### 11	AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
#### b) Tempo de apresentação 6:40 

># Marco de Entrega 03: Itens 10 e 11<br>
<br>
<br>




### 12 FORMATACAO NO GIT:<br> 
https://help.github.com/articles/basic-writing-and-formatting-syntax/
<comentario no git>
    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
    
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/
#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

    
### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. <strong>Caso existam arquivos com conteúdos sigilosos<strong>, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário do git "profmoisesomena", para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://www.sis4.com/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


