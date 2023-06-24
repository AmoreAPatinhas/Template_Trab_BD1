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

> Abertura, login e Menu
<div>
  <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/Screenshot_20230620_131457_Samsung%20Internet.jpg?raw=true" alt="demo" height="425">
  <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/Screenshot_20230620_131502_Samsung%20Internet.jpg?raw=true" alt="demo" height="425">
  <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/Screenshot_20230620_131506_Samsung%20Internet.jpg?raw=true" alt="demo" height="425">

</div>

> CRUD - Visualizar animais

<div>
  <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/Screenshot_20230620_131513_Samsung%20Internet.jpg?raw=true" alt="demo" height="425">
  <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/Screenshot_20230620_131520_Samsung%20Internet.jpg?raw=true" alt="demo" height="425">
  <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/imagem_2023-06-21_105024680.png?raw=true" alt="demo" height="425">
  <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/imagem_2023-06-21_101300283.png?raw=true" alt="demo" height="425">
  <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/imagem_2023-06-21_104834464.png?raw=true" alt="demo" height="425">
  

</div>


> Dados médicos do animal
<div>
 <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/Screenshot_20230620_131544_Samsung%20Internet.jpg?raw=true" alt="demo" height="425">
 <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/Screenshot_20230620_131541_Samsung%20Internet.jpg?raw=true" alt="demo" height="425">
 <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/Screenshot_20230620_131548_Samsung%20Internet.jpg?raw=true" alt="demo" height="425">
</div>

 
> CRUD - Visualizar Voluntários

<div>
  <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/Screenshot_20230620_131645_Samsung%20Internet.jpg?raw=true" alt="demo" height="425">
  <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/Screenshot_20230620_131655_Samsung%20Internet.jpg?raw=true" alt="demo" height="425">
  <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/Screenshot_20230620_131754_Samsung%20Internet.jpg?raw=true" alt="demo" height="425">
  <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/Screenshot_20230620_133039_Samsung%20Internet.jpg?raw=true" alt="demo" height="425">
  <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/Screenshot_20230620_132958_Samsung%20Internet.jpg?raw=true" alt="demo" height="425">
  

</div>

> CRUD - Visualizar Adoções
<div>
  <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/Screenshot_20230620_132028_Samsung%20Internet.jpg?raw=true" alt="demo" height="425">
  <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/Screenshot_20230620_132033_Samsung%20Internet.jpg?raw=true" alt="demo" height="425">
  <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/Screenshot_20230620_132043_Samsung%20Internet.jpg?raw=true" alt="demo" height="425">
  <img src="https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/blob/main/imagens/imagem_2023-06-21_121919201.png?raw=true" alt="demo" height="425">
	
</div>

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
 
 * PESSOA: código da pessoa, nome da pessoa, telefone, cpf, email, código do animal
 
 * RAÇA: Identifica qual é a raça do animal
 
 * PELAGEM: Identifica o tipo de pelagem do animal

 * PROCEDIMENTO: código do procedimento, código do animal, descrição e data

 * TIPO DE TRATAMENTO: código de tratamento e descrição


### 6	MODELO LÓGICO<br>
![modelocerto!](https://github.com/AmoreAPatinhas/TrabalhoBancoDeDados/assets/95357142/ab6cbe5e-9ee5-4256-9e54-6152a3a95c14)


### 7	MODELO FÍSICO<br>

```
/* ModeloLogico_PatinhaseAmor: */

CREATE TABLE PESSOA (
    id_pessoa integer PRIMARY KEY,
    nome_pessoa varchar(100),
    telefone integer,
    cpf integer,
    email varchar(100),
    id_animal integer,
    FK_ENDERECO_id_endereco integer,
    FOREIGN KEY (FK_ENDERECO_id_endereco) REFERENCES ENDERECO(id_endereco)
);


CREATE TABLE FUNCIONARIO(
    id_funcionario integer PRIMARY KEY,
    FK_PESSOA_id_pessoa INT,
    ocupacao VARCHAR(50),
    FOREIGN KEY (FK_PESSOA_id_pessoa) REFERENCES PESSOA(id_pessoa)
		
    
  );
  
CREATE TABLE ANIMAL(
    id_animal integer PRIMARY KEY,
    nome varchar(100),
    data_chegada date,
    id_especie integer,
    porte varchar(100),
    FK_PESSOA_id_pessoa integer,
    id_especie integer,
    id_raca integer,
    id_pelagem integer,
    FOREIGN KEY (FK_PESSOA_id_pessoa) REFERENCES PESSOA(id_pessoa),
    FOREIGN KEY (id_especie) REFERENCES ESPECIE(id_especie),
    FOREIGN KEY (id_raca) REFERENCES RACA(id_raca),
    FOREIGN KEY (id_pelagem) REFERENCES PELAGEM(id_pelagem)
  );

  
CREATE TABLE ESPECIE(
    id_especie integer PRIMARY KEY,
    FK_ANIMAL_id_animal integer,
    tipo_especie text
      
);

CREATE TABLE TIPO_TRATAMENTO(
    descricao VARCHAR(100),
    id_tratamento integer PRIMARY KEY
    
);

CREATE TABLE PROCEDIMENTO(
    fk_ANIMAL_id_animal integer,
    fk_TIPO_TRATAMENTO_id_tratamento integer,
    descricao text,
    data_hora date,
    id_animal integer,
    id_tratamento integer
   FOREIGN KEY (fk_ANIMAL_id_animal) REFERENCES ANIMAL(id_animal),
   FOREIGN KEY (fk_TIPO_TRATAMENTO_id_tratamento) REFERENCES TIPO_TRATAMENTO(id_tipo_tratamento)
    
);

CREATE TABLE RACA (
    nome_raca text,
    id_raca integer PRIMARY KEY,
    id_especie integer
		
);

CREATE TABLE PELAGEM (
    tipo_pelagem text,
    id_pelagem integer PRIMARY KEY
);



CREATE TABLE ENDERECO(
    nome_rua VARCHAR(150),
    id_endereco integer PRIMARY KEY,
    bairro VARCHAR(150),
    cep integer,
    numero integer
		
  );


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

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>

#### Link do Colab: https://colab.research.google.com/drive/1Xa8sNnJWlX7lkmoH0PHXi7EGnG9m5GUN?usp=sharing

#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)

#### Link do Colab: https://colab.research.google.com/drive/1Xa8sNnJWlX7lkmoH0PHXi7EGnG9m5GUN?usp=sharing

```
SELECT p.nome_pessoa, p.cpf, a.porte
FROM PESSOA p
JOIN ANIMAL a ON p.id_animal = a.id_animal
WHERE p.cpf < 50000000000 AND a.porte = 'Pequeno'

SELECT nome, porte FROM ANIMAL
WHERE porte = 'Pequeno' OR porte = 'Médio'
    
SELECT nome_pessoa FROM PESSOA 
WHERE id_animal IS NOT NULL

SELECT nome, porte, data_chegada
FROM ANIMAL
WHERE porte = 'Pequeno' AND data_chegada > '2022-01-01'

SELECT nome, porte, data_chegada
FROM ANIMAL
WHERE porte = 'Pequeno' OR data_chegada < '2022-01-01'

SELECT * FROM ANIMAL WHERE id_animal > 5 AND id_animal <= 8;

SELECT a.* FROM ANIMAL a
JOIN PESSOA p ON a.FK_PESSOA_id_pessoa = p.id_pessoa
WHERE p.telefone % 2 = 0;

SELECT *
FROM ANIMAL
WHERE EXTRACT(YEAR FROM AGE(CURRENT_DATE, data_chegada)) > 0;

SELECT a.nome AS nome_animal, p.nome_pessoa AS responsavel
FROM ANIMAL a
JOIN PESSOA p ON a.FK_PESSOA_id_pessoa = p.id_pessoa;

SELECT e.nome_rua AS rua, e.numero AS numero_endereco
FROM ANIMAL a
JOIN PESSOA p ON a.FK_PESSOA_id_pessoa = p.id_pessoa
JOIN ENDERECO e ON p.FK_ENDERECO_id_endereco = e.id_endereco
WHERE p.cpf = 11111111111;

SELECT p.descricao AS tratamento, p.data_hora AS data
FROM Procedimento p;

```

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>

#### Link do Colab: https://colab.research.google.com/drive/1Xa8sNnJWlX7lkmoH0PHXi7EGnG9m5GUN?usp=sharing

```
SELECT * FROM PESSOA WHERE nome_pessoa LIKE 'J%';

SELECT * FROM ANIMAL WHERE nome LIKE '%o%';

SELECT * FROM RACA WHERE nome_raca LIKE '%Retriever%' AND id_especie = 1;

SELECT * FROM TIPO_TRATAMENTO WHERE descricao ILIKE '%vacina%';

SELECT * FROM PESSOA WHERE email LIKE '%@example.com';

SELECT * FROM ANIMAL WHERE data_chegada > '2022-06-01';

SELECT * FROM Procedimento WHERE data_hora < '2022-05-01';

SELECT * FROM PESSOA WHERE CAST(cpf AS TEXT) LIKE '11111111111%';

SELECT * FROM ANIMAL
WHERE id_animal IN (SELECT fk_ANIMAL_id_animal FROM Procedimento 
WHERE EXTRACT(MONTH FROM data_hora) = 3 AND EXTRACT(YEAR FROM data_hora) = 2022);

SELECT * FROM PROCEDIMENTO WHERE EXTRACT(DAY FROM data_hora) = 15;

SELECT * FROM PESSOA WHERE CAST(telefone as text) LIKE '%555%';

SELECT * FROM ANIMAL WHERE nome LIKE '%s';

```

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>

#### Link do Colab: https://colab.research.google.com/drive/1Xa8sNnJWlX7lkmoH0PHXi7EGnG9m5GUN?usp=sharing

```
delete from pelagem where tipo_pelagem = 'Curto'; 

delete from animal where fk_pessoa_id_pessoa in (select id_pessoa from pessoa 
where nome_pessoa = 'Michael Johnson');

delete from especie where id_especie = 2;

delete from procedimento where id_animal = 1;

update raca set nome_raca = 'Lhasa Apso' where nome_raca = 'Golden Retriever';

update endereco set numero = 3 where numero = 20;

update animal set id_especie = 3 where id_animal = 1;

update pessoa set nome_pessoa = 'Isabella S' where id_animal = 3;

```

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>

#### Link do Colab: https://colab.research.google.com/drive/1Xa8sNnJWlX7lkmoH0PHXi7EGnG9m5GUN?usp=sharing

```
SELECT A.*, PE.nome_pessoa,F.*, P.*, TP.*
FROM animal A
INNER JOIN pessoa PE ON A.fk_pessoa_id_pessoa = PE.id_pessoa
INNER JOIN funcionario F ON A.FK_PESSOA_id_pessoa = F.FK_PESSOA_id_pessoa
INNER JOIN procedimento P ON A.id_animal = P.id_animal
INNER JOIN tipo_tratamento TP ON P.fk_tipo_tratamento_id_tratamento = TP.id_tratamento
ORDER BY P.data_hora;


SELECT A.*, P.*, TP.*, PE.*, F.*, E.*, PEL.*, R.*, EN.*
FROM animal A 
INNER JOIN procedimento P ON A.id_animal = P.id_animal
INNER JOIN tipo_tratamento TP ON P.fk_tipo_tratamento_id_tratamento = TP.id_tratamento
INNER JOIN pessoa PE ON A.fk_pessoa_id_pessoa = PE.id_pessoa
INNER JOIN funcionario F ON PE.id_pessoa = F.id_pessoa
INNER JOIN especie E ON A.id_especie = E.id_especie
INNER JOIN pelagem PEL ON A.id_pelagem = PEL.id_pelagem
INNER JOIN raca R ON A.id_raca = R.id_raca
INNER JOIN endereco EN ON PE.fk_endereco_id_endereco = EN.id_endereco;

```

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>

#### Link do Colab: https://colab.research.google.com/drive/1Xa8sNnJWlX7lkmoH0PHXi7EGnG9m5GUN?usp=sharing

```
SELECT * FROM pessoa GROUP BY nome_pessoa

SELECT * FROM animal GROUP BY nome

SELECT * FROM endereco GROUP BY nome_rua

SELECT * FROM especie GROUP BY tipo_especie

SELECT * FROM funcionario GROUP BY ocupacao

SELECT * FROM pelagem GROUP BY tipo_pelagem

SELECT * FROM procedimento GROUP BY descricao

SELECT * FROM raca GROUP BY nome_raca

SELECT * FROM tipo_tratamento GROUP BY descricao
``` 

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>

#### Link do Colab: https://colab.research.google.com/drive/1Xa8sNnJWlX7lkmoH0PHXi7EGnG9m5GUN?usp=sharing

``` 
SELECT ADOTANTE.NOME_ADOTANTE, ANIMAL.NOME
FROM ADOTANTE
LEFT JOIN ANIMAL_ADOTANTE ON ADOTANTE.CODIGO_ADOTANTE = ANIMAL_ADOTANTE.CODIGO_ADOTANTE
LEFT JOIN ANIMAL ON ANIMAL_ADOTANTE.CODIGO_ANIMAL = ANIMAL.ID_ANIMAL;

SELECT ANIMAL.NOME, ANIMAL_ADOTANTE.CODIGO_ADOCAO
FROM ANIMAL
RIGHT JOIN ANIMAL_ADOTANTE ON ANIMAL.ID_ANIMAL = ANIMAL_ADOTANTE.CODIGO_ANIMAL;

SELECT ADOTANTE.NOME_ADOTANTE, ANIMAL.NOME
FROM ADOTANTE
FULL JOIN ANIMAL_ADOTANTE ON ADOTANTE.CODIGO_ADOTANTE = ANIMAL_ADOTANTE.CODIGO_ADOTANTE
FULL JOIN ANIMAL ON ANIMAL_ADOTANTE.CODIGO_ANIMAL = ANIMAL.ID_ANIMAL;

SELECT ANIMAL.NOME, ESPECIE.TIPO_ESPECIE, FUNCIONARIO.NOME_FUNCIONARIO
FROM ANIMAL
LEFT JOIN ESPECIE ON ANIMAL.CODIGO_ESPECIE = ESPECIE.ID_ESPECIE
LEFT JOIN FUNCIONARIO ON ANIMAL.CODIGO_FUNCIONARIO = FUNCIONARIO.CODIGO_FUNCIONARIOS;

```

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>

#### Link do Colab: https://colab.research.google.com/drive/1Xa8sNnJWlX7lkmoH0PHXi7EGnG9m5GUN?usp=sharing

```
create view funcionario_e_ocupacao as
select id_funcionario,ocupacao
from funcionario;

SELECT * FROM funcionario_e_ocupacao;

create view animal_e_porte as
select nome,porte
from animal
order by porte;

SELECT * FROM animal_e_porte;

create view funcionarios_por_ocupacao as
select f1.ocupacao, count(f2.id_funcionario) as quantidade_funcionarios
from funcionario f1
join funcionario f2 ON f1.ocupacao = f2.ocupacao
group by f1.ocupacao;

SELECT * FROM funcionarios_por_ocupacao;

SELECT e1.nome_rua, COUNT(e2.id_endereco) as quantidade_enderecos
FROM endereco e1
JOIN endereco e2 ON e1.nome_rua = e2.nome_rua
GROUP BY e1.nome_rua;

create view pessoas_mesmo_endereco as
select p1.nome_pessoa, p2.nome_pessoa as nome_pessoa_relacionada
from pessoa p1
join pessoa p2 on p1.fk_endereco_id_endereco = p2.fk_endereco_id_endereco
where p1.id_pessoa <> p2.id_pessoa;

SELECT * FROM pessoas_mesmo_endereco;

SELECT p1.id_animal, COUNT(p2.id_animal) as quantidade_procedimentos
FROM Procedimento p1
JOIN Procedimento p2 ON p1.fk_animal_id_animal = p2.fk_animal_id_animal
GROUP BY p1.id_animal;

```

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>

#### Link do Colab: https://colab.research.google.com/drive/1Xa8sNnJWlX7lkmoH0PHXi7EGnG9m5GUN?usp=sharing

```
SELECT *
FROM animal
WHERE fk_funcionario_id_funcionario NOT IN (
    SELECT DISTINCT fk_funcionario_id_funcionario
    FROM animal
    WHERE porte <> 'Pequeno'
);

SELECT *
FROM funcionario
WHERE id_funcionario IN (
    SELECT DISTINCT id_funcionario
    FROM funcionario
    WHERE ocupacao = 'Atendente'
);

SELECT *
FROM funcionario
WHERE ocupacao IN ('Atendente', 'Groomer');

SELECT id_animal, nome, porte, id_especie
FROM animal
WHERE id_especie IN (1);

```



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


