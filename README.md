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

> Todo animal ao chegar no abrigo, necessita que um administrador o cadastre com algumas informações básicas para ser identificado, como a raça, nome, data que chegou ao abrigo, cor, pelagem, porte (pequeno, médo e grande) e espécie (as espécies dos animais devem ser diferenciadas através de códigos). A espécie do animal se distingue por Gato ou Cachorro. Já a raça, informa a família do animal (exemplo: vira-lata, siamês, golden retriever...). É possível posteriormente editar os dados de cadastro.
 
> Do sistema espera-se que seja possível que o administrador cadastre também os voluntários que tenham interesse para ajudar nas atividades do abrigo e no cuidado dos animais. Ao demonstrar interesse, esse voluntário se torna um funcionário do abrigo e pode contribuir de várias formas, caso tenha alguma formação na área animal (como um veterinário), poderá auxiliar em consultas, aplicação e dosagem de remédios. Caso não tenha, é alocado para manutenções gerais, limpeza, alimentação e banho. Deve ser possível inserir os dados dos funcionários do abrigo, colocando nome, cpf, telefone, email, endereço e ocupação (onde irá atuar no abrigo, qual tarefa…) para que assim seja possível controlar a entrada e saída de pessoas no abrigo e sua atuação. É possível posteriormente editar e excluir os dados de cadastro.
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
![usaresse](https://github.com/AmoreAPatinhas/Template_Trab_BD1/assets/95357142/87772cdb-2910-4561-b3f3-f4cbc537f243)

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
![Captura de tela 2023-06-08 193519](https://github.com/AmoreAPatinhas/Template_Trab_BD1/assets/95357142/049bdf2b-b4dc-4c57-bdb3-5782820fce0e)


### 7	MODELO FÍSICO<br>

```
/* ModeloLogico_PatinhaseAmor: */

CREATE TABLE ESPECIE (
    id_especie integer PRIMARY KEY,
    tipo_especie text
);

CREATE TABLE ANIMAL (
    id_animal integer PRIMARY KEY,
    nome text,
    data_chegada date,
    id_especie integer,
    porte text,
    FK_PESSOA_id_pessoa integer,
    FK_FUNCIONARIO_id_funcionario integer,
    FK_FUNCIONARIO_FK_PESSOA_id_pessoa integer
);


CREATE TABLE TIPO_TRATAMENTO (
    descricao text,
    id_tratamento integer PRIMARY KEY
);


CREATE TABLE FUNCIONARIO (
    id_funcionario integer,
    ocupacao varchar[50],
    FK_PESSOA_id_pessoa integer,
    PRIMARY KEY (id_funcionario, FK_PESSOA_id_pessoa)
);


CREATE TABLE ENDERECO (
    nome_rua text,
    id_endereco integer PRIMARY KEY,
    bairro text,
    cep integer,
    numero integer,
    id_pessoa integer
);

CREATE TABLE PESSOA (
    id_pessoa integer PRIMARY KEY,
    nome_pessoa text,
    telefone integer,
    cpf integer,
    email text,
    id_animal integer,
    FK_ENDERECO_id_endereco integer,
    CONSTRAINT FK_PESSOA_ENDERECO FOREIGN KEY (FK_ENDERECO_id_endereco)
    REFERENCES ENDERECO (id_endereco)
);


CREATE TABLE RACA (
    id_animal integer,
    nome_raca text,
    id_raca integer PRIMARY KEY,
    id_especie integer
);

CREATE TABLE PELAGEM (
    id_animal integer,
    tipo_pelagem text,
    id_pelagem integer PRIMARY KEY
);

CREATE TABLE Possui_ANIMAL_ESPECIE_RACA_PELAGEM (
    fk_ANIMAL_id_animal integer,
    fk_ESPECIE_id_especie integer,
    fk_RACA_id_raca integer,
    fk_PELAGEM_id_pelagem integer
);

CREATE TABLE Procedimento (
    fk_ANIMAL_id_animal integer,
    fk_TIPO_TRATAMENTO_id_tratamento integer,
    descricao text,
    data_hora date,
    id_animal integer,
    id_tratamento integer
);
 
ALTER TABLE ANIMAL ADD CONSTRAINT FK_ANIMAL_2
    FOREIGN KEY (FK_PESSOA_id_pessoa)
    REFERENCES PESSOA (id_pessoa)
    ON DELETE CASCADE;
 
ALTER TABLE ANIMAL ADD CONSTRAINT FK_ANIMAL_3
    FOREIGN KEY (FK_FUNCIONARIO_id_funcionario, FK_FUNCIONARIO_FK_PESSOA_id_pessoa)
    REFERENCES FUNCIONARIO (id_funcionario, FK_PESSOA_id_pessoa)
    ON DELETE RESTRICT;
 
ALTER TABLE FUNCIONARIO ADD CONSTRAINT FK_FUNCIONARIO_2
    FOREIGN KEY (FK_PESSOA_id_pessoa)
    REFERENCES PESSOA (id_pessoa)
    ON DELETE CASCADE;
 
ALTER TABLE ENDERECO ADD CONSTRAINT FK_ENDERECO_2
    FOREIGN KEY (id_pessoa???)
    REFERENCES ??? (???);
 
ALTER TABLE PESSOA ADD CONSTRAINT FK_PESSOA_2
    FOREIGN KEY (FK_ENDERECO_id_endereco)
    REFERENCES ENDERECO (id_endereco)
    ON DELETE RESTRICT;
 
ALTER TABLE Possui_ANIMAL_ESPECIE_RACA_PELAGEM ADD CONSTRAINT FK_Possui_ANIMAL_ESPECIE_RACA_PELAGEM_1
    FOREIGN KEY (fk_ANIMAL_id_animal)
    REFERENCES ANIMAL (id_animal)
    ON DELETE NO ACTION;
 
ALTER TABLE Possui_ANIMAL_ESPECIE_RACA_PELAGEM ADD CONSTRAINT FK_Possui_ANIMAL_ESPECIE_RACA_PELAGEM_2
    FOREIGN KEY (fk_ESPECIE_id_especie)
    REFERENCES ESPECIE (id_especie)
    ON DELETE RESTRICT;
 
ALTER TABLE Possui_ANIMAL_ESPECIE_RACA_PELAGEM ADD CONSTRAINT FK_Possui_ANIMAL_ESPECIE_RACA_PELAGEM_3
    FOREIGN KEY (fk_RACA_id_raca)
    REFERENCES RACA (id_raca)
    ON DELETE RESTRICT;
 
ALTER TABLE Possui_ANIMAL_ESPECIE_RACA_PELAGEM ADD CONSTRAINT FK_Possui_ANIMAL_ESPECIE_RACA_PELAGEM_4
    FOREIGN KEY (fk_PELAGEM_id_pelagem)
    REFERENCES PELAGEM (id_pelagem)
    ON DELETE RESTRICT;
 
ALTER TABLE Procedimento ADD CONSTRAINT FK_Procedimento_1
    FOREIGN KEY (fk_ANIMAL_id_animal)
    REFERENCES ANIMAL (id_animal)
    ON DELETE SET NULL;
 
ALTER TABLE Procedimento ADD CONSTRAINT FK_Procedimento_2
    FOREIGN KEY (fk_TIPO_TRATAMENTO_id_tratamento)
    REFERENCES TIPO_TRATAMENTO (id_tratamento)
    ON DELETE SET NULL;

```
       
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>

```
INSERT INTO ANIMAL (id_animal, nome, data_chegada, id_especie, porte, FK_PESSOA_id_pessoa, FK_FUNCIONARIO_id_funcionario, FK_FUNCIONARIO_FK_PESSOA_id_pessoa)
VALUES
    (1, 'Max', '2022-01-01', 1, 'Pequeno', 1, 1, 1),
    (2, 'Bella', '2022-02-01', 2, 'Pequeno', 2, 1, 1),
    (3, 'Charlie', '2022-03-01', 1, 'Médio', 3, 2, 2),
    (4, 'Lucy', '2022-04-01', 2, 'Pequeno', 4, 2, 2),
    (5, 'Rocky', '2022-05-01', 1, 'Grande', 5, 3, 3),
    (6, 'Luna', '2022-06-01', 2, 'Pequeno', 6, 3, 3),
    (7, 'Maximus', '2022-07-01', 1, 'Grande', 7, 4, 4),
    (8, 'Sophie', '2022-08-01', 2, 'Médio', 8, 4, 4),
    (9, 'Buddy', '2022-09-01', 1, 'Pequeno', 9, 5, 5),
    (10, 'Milo', '2022-10-01', 2, 'Médio', 10, 5, 5);

INSERT INTO TIPO_TRATAMENTO (descricao, id_tratamento)
VALUES
    ('Vacinação', 1),
    ('Cirurgia', 2),
    ('Exame de sangue', 3),
    ('Tratamento odontológico', 4),
    ('Fisioterapia', 5),
    ('Banho e tosa', 6),
    ('Desparasitação', 7),
    ('Consulta veterinária', 8),
    ('Corte de unhas', 9),
    ('Adestramento', 10);

INSERT INTO FUNCIONARIO (id_funcionario, ocupacao, FK_PESSOA_id_pessoa)
VALUES
    (1, 'Veterinário', 1),
    (2, 'Atendente', 2),
    (3, 'Auxiliar de veterinário', 3),
    (4, 'Recepcionista', 4),
    (5, 'Veterinário', 5),
    (6, 'Atendente', 6),
    (7, 'Auxiliar de veterinário', 7),
    (8, 'Veterinário', 8),
    (9 , 'Atendente', 9),
    (10, 'Groomer', 10);

INSERT INTO ENDERECO (nome_rua, id_endereco, bairro, cep, numero, id_pessoa)
VALUES    
    ('Rua A', 1, 'Centro', 12345, 10, 1),
    ('Rua B', 2, 'Bairro X', 54321, 20, 2),
    ('Rua C', 3, 'Bairro Y', 67890, 123, 3),
    ('Rua D', 4, 'Bairro Z', 78901, 456, 4),
    ('Rua E', 5, 'Bairro X', 89012, 789, 5),
    ('Rua F', 6, 'Bairro Y', 90123, 234, 6),
    ('Rua G', 7, 'Bairro Z', 12345, 567, 7),
    ('Rua H', 8, 'Bairro X', 23456, 890, 8),
    ('Rua I', 9, 'Bairro Y', 34567, 123, 9),
    ('Rua J', 10, 'Bairro Z', 45678, 456, 10);

INSERT INTO PESSOA (id_pessoa, nome_pessoa, telefone, cpf, email, id_animal, FK_ENDERECO_id_endereco)
VALUES
    (1, 'João', 123456789, 12345678900, 'joao@example.com', 1, 1),
    (2, 'Maria', 987654321, 98765432100, 'maria@example.com', 2, 2),
    (3, 'John Smith', 123456789, 11111111111, 'john@example.com', 3, 3),
    (4, 'Jane Doe', 987654321, 22222222222, 'jane@example.com', 4, 4),
    (5, 'Michael Johnson', 111222333, 33333333333, 'michael@example.com', 5, 5),
    (6, 'Emily Williams', 444555666, 44444444444, 'emily@example.com', 6, 6),
    (7, 'Christopher Brown', 777888999, 55555555555, 'christopher@example.com', 7, 7),
    (8, 'Jessica Davis', 222333444, 66666666666, 'jessica@example.com', 8, 8),
    (9, 'Daniel Wilson', 555666777, 77777777777, 'daniel@example.com', 9, 9),
    (10, 'Olivia Taylor', 888999000, 88888888888, 'olivia@example.com', 10, 10);

INSERT INTO RACA (id_animal, nome_raca, id_raca, id_especie)
VALUES
    (1, 'Poodle', 1, 1),
    (2, 'Sphynx', 2, 2),
    (3, 'Labrador Retriver', 1, 1),
    (4, 'Persa', 2, 2),
    (5, 'Pastor Alemão', 3, 1),
    (6, 'Siames', 4, 2),
    (7, 'Golden Retriever', 5, 1),
    (8, 'Maine Coon', 6, 2),
    (9, 'Bulldog', 7, 1),
    (10, 'Ragdoll', 8, 2);

INSERT INTO PELAGEM (id_animal, tipo_pelagem, id_pelagem)
VALUES
    
    (1, 'Crespa', 1),
    (2, 'Curta', 2),
    (3, 'Curto', 1),
    (4, 'Longo', 2),
    (5, 'Médio', 3),
    (6, 'Curto', 4),
    (7, 'Dourado', 5),
    (8, 'Branco', 6),
    (9, 'Tigrado', 7),
    (10, 'Laranja', 8);

INSERT INTO Possui_ANIMAL_ESPECIE_RACA_PELAGEM (fk_ANIMAL_id_animal, fk_ESPECIE_id_especie, fk_RACA_id_raca, fk_PELAGEM_id_pelagem)
VALUES
    (1, 1, 1, 1),
    (2, 2, 2, 2),
    (3, 1, 1, 1),
    (4, 2, 2, 2),
    (5, 1, 3, 3),
    (6, 2, 4, 4),
    (7, 1, 5, 5),
    (8, 2, 6, 6),
    (9, 1, 7, 7),
    (10, 2, 8, 8);

INSERT INTO Procedimento (fk_ANIMAL_id_animal, fk_TIPO_TRATAMENTO_id_tratamento, descricao, data_hora, id_animal, id_tratamento)
VALUES

    (1, 1, 'Vacinação anual', '2022-03-01', 1, 1),
    (2, 2, 'Cirurgia de esterilização', '2022-04-01', 2, 2),
    (3, 3, 'Vacinação anual', '2022-03-15', 3, 3),
    (4, 4, 'Esterilização', '2022-04-20', 4, 4),
    (5, 5, 'Hemograma completo', '2022-05-25', 5, 5),
    (6, 6, 'Limpeza dentária', '2022-06-30', 6, 6),
    (7, 7, 'Reabilitação pós-operatória', '2022-07-05', 7, 7),
    (8, 8, 'Banho e tosa', '2022-08-10', 8, 8),
    (9, 9, 'Desparasitação interna e externa', '2022-09-15', 9, 9),
    (10, 10, 'Consulta de rotina', '2022-10-20', 10, 10);
 
```

### 9	TABELAS E PRINCIPAIS CONSULTAS<br>

#### Link do Colab: https://colab.research.google.com/drive/1Xa8sNnJWlX7lkmoH0PHXi7EGnG9m5GUN?usp=sharing

#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>

![WhatsApp Image 2023-06-10 at 8 08 29 PM](https://github.com/AmoreAPatinhas/Template_Trab_BD1/assets/71940799/4cb68395-d7a3-4e39-a36a-be287c3a0fb6)
--------------------------------------
![WhatsApp Image 2023-06-10 at 8 08 29 PM (1)](https://github.com/AmoreAPatinhas/Template_Trab_BD1/assets/71940799/13399622-5933-4c6f-ab55-3c83b1da4652)
--------------------------------------
![WhatsApp Image 2023-06-10 at 8 08 29 PM (2)](https://github.com/AmoreAPatinhas/Template_Trab_BD1/assets/71940799/21285e27-a526-40fb-bdbf-650eae7f13e9)
--------------------------------------
![WhatsApp Image 2023-06-10 at 8 08 29 PM (3)](https://github.com/AmoreAPatinhas/Template_Trab_BD1/assets/71940799/a318a864-8617-43b4-8d16-6cbcb0fe47c1)
--------------------------------------
![WhatsApp Image 2023-06-10 at 8 08 29 PM (4)](https://github.com/AmoreAPatinhas/Template_Trab_BD1/assets/71940799/fb927fd0-df49-4af0-9bfa-7b890a387104)
--------------------------------------
![WhatsApp Image 2023-06-10 at 8 08 29 PM (5)](https://github.com/AmoreAPatinhas/Template_Trab_BD1/assets/71940799/c468ca47-b101-44a8-8e12-6b424e3bfd04)
--------------------------------------
![WhatsApp Image 2023-06-10 at 8 08 29 PM (6)](https://github.com/AmoreAPatinhas/Template_Trab_BD1/assets/71940799/a0328be8-a813-436a-a3b4-955743bc5fcb)
--------------------------------------
![WhatsApp Image 2023-06-10 at 8 08 29 PM (7)](https://github.com/AmoreAPatinhas/Template_Trab_BD1/assets/71940799/ba266365-925d-44ec-b1fa-57550b376a2b)
--------------------------------------
![WhatsApp Image 2023-06-10 at 8 08 29 PM (8)](https://github.com/AmoreAPatinhas/Template_Trab_BD1/assets/71940799/9a3893a2-6fae-4854-a15d-ff5d53c36eb2)
--------------------------------------
![WhatsApp Image 2023-06-10 at 8 08 29 PM (9)](https://github.com/AmoreAPatinhas/Template_Trab_BD1/assets/71940799/531b42b4-038d-44fe-a722-3680c5681db3)

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
    
    ```
    delete from pelagem where tipo_pelagem = 'Pelagem curta';
    delete from animal 
    where codigo_pessoa in (select id_pessoa 
                          from pessoa 
                          where nome_pessoa = 'Julia Teixeira de Castro');
   delete from especie where id_especie = 2;
   delete from funcionario where codigo_funcionario > 5;
   delete from procedimento where id_animal = 1;
    
    b) Criar minimo 3 de atualização
    update raca set nome_raca = 'Lhasa Apso' where nom_raca = 'Golden Retriver';
    update animal set id_especie = 3 where id_animal = 1;
    update animal_adotante set data_adocao = '2023-06-12' where codigo_adocao = 3;
    update endereco set id_endereco = 3;

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


