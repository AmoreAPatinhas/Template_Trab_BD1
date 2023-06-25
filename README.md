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
    id_tipo_tratamento integer PRIMARY KEY
    
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
INSERT INTO ESPECIE (id_especie, FK_ANIMAL_id_animal, tipo_especie)
VALUES
(1, 1, 'Cachorro'),
(2, 2, 'Gato')

INSERT INTO RACA (nome_raca, id_raca, id_especie)
VALUES
('Poodle', 1, 1),
('Bulldog', 2, 1),
('Labrador', 3, 1),
('Golden Retriever', 4, 1),
('Chihuahua', 5, 1),
('Beagle', 6, 1),
('Boxer', 7, 1),
('Dalmatian', 8, 1),
('Rottweiler', 9, 1),
('Schnauzer', 10, 1),
('Doberman', 11, 1),
('German Shepherd', 12, 1),
('Cocker Spaniel', 13, 1),
('Yorkshire Terrier', 14, 1),
('Great Dane', 15, 1),
('Shih Tzu', 16, 1),
('Maltese', 17, 1),
('Border Collie', 18, 1),
('Australian Shepherd', 19, 1),
('Siberian Husky', 20, 1),
('Pomeranian', 21, 1),
('Bichon Frise', 22, 1),
('English Bulldog', 23, 1),
('French Bulldog', 24, 1),
('Basset Hound', 25, 1),
('Bloodhound', 26, 1),
('Saint Bernard', 27, 1),
('Dachshund', 28, 1),
('Pug', 29, 1),
('Akita', 30, 1),
('Bull Terrier', 31, 1),
('Shiba Inu', 32, 1),
('Collie', 33, 1),
('Borzoi', 34, 1),
('Whippet', 35, 1),
('Papillon', 36, 1),
('Bullmastiff', 37, 1),
('Chinese Crested', 38, 1),
('Basenji', 39, 1),
('English Setter', 40, 1),
('Irish Setter', 41, 1),
('Weimaraner', 42, 1),
('Rhodesian Ridgeback', 43, 1),
('Pekingese', 44, 1),
('Dalmatian', 45, 1),
('Chow Chow', 46, 1),
('Corgi', 47, 1),
('Shetland Sheepdog', 48, 1),
('Bernese Mountain Dog', 49, 1),
('Newfoundland', 50, 1);

INSERT INTO PELAGEM (tipo_pelagem, id_pelagem)
VALUES
('Curto', 1),
('Longo', 2),
('Médio', 3),
('Cacheado', 4),
('Sem pelo', 5),
('Rajado', 6),
('Encaracolado', 7),
('Ondulado', 8),
('Liso', 9),
('Crespo', 10),
('Espesso', 11),
('Fino', 12),
('Duro', 13),
('Macio', 14),
('Peludo', 15),
('Pelo curto e denso', 16),
('Pelo longo e sedoso', 17),
('Pelo médio e ondulado', 18),
('Pelo encaracolado', 19),
('Pelo liso e brilhante', 20),
('Pelo crespo e macio', 21),
('Pelo espesso e denso', 22),
('Pelo fino e sedoso', 23),
('Pelo duro e áspero', 24),
('Pelo macio e aveludado', 25),
('Pelo peludo e abundante', 26),
('Pelo liso e curto', 27),
('Pelo longo e grosso', 28),
('Pelo médio e encaracolado', 29),
('Pelo encaracolado e sedoso', 30),
('Pelo liso e sedoso', 31),
('Pelo encaracolado e macio', 32),
('Pelo liso e espesso', 33),
('Pelo crespo e fino', 34),
('Pelo espesso e duro', 35),
('Pelo macio e brilhante', 36),
('Pelo encaracolado e denso', 37),
('Pelo liso e fino', 38),
('Pelo encaracolado e sedoso', 39),
('Pelo liso e macio', 40),
('Pelo crespo e espesso', 41),
('Pelo espesso e áspero', 42),
('Pelo macio e aveludado', 43),
('Pelo peludo e abundante', 44),
('Pelo liso e curto', 45),
('Pelo longo e grosso', 46),
('Pelo médio e encaracolado', 47),
('Pelo encaracolado e sedoso', 48),
('Pelo liso e sedoso', 49),
('Pelo encaracolado e macio', 50);


INSERT INTO TIPO_TRATAMENTO (descricao, id_tipo_tratamento)
VALUES
('Vacinação', 1),
('Cirurgia', 2),
('Exame de sangue', 3),
('Limpeza dentária', 4),
('Tratamento dermatológico', 5),
('Fisioterapia', 6),
('Desparasitação', 7),
('Radiografia', 8),
('Oftalmologia', 9),
('Endoscopia', 10),
('Acupuntura', 11),
('Quimioterapia', 12),
('Odontologia', 13),
('Ultrassonografia', 14),
('Ortopedia', 15);

INSERT INTO PROCEDIMENTO (fk_ANIMAL_id_animal, fk_TIPO_TRATAMENTO_id_tratamento, descricao, data_hora)
VALUES
(1, 1, 'Vacinação anual', '2023-01-10'),
(2, 2, 'Esterilização', '2023-02-20'),
(3, 3, 'Exame de sangue de rotina', '2023-03-15'),
(4, 4, 'Limpeza dentária', '2023-04-25'),
(5, 5, 'Tratamento dermatológico', '2023-05-12'),
(6, 6, 'Sessão de fisioterapia', '2023-06-08'),
(7, 7, 'Desparasitação interna', '2023-07-03'),
(8, 8, 'Radiografia torácica', '2023-08-19'),
(9, 9, 'Consulta oftalmológica', '2023-09-27'),
(10, 10, 'Endoscopia gastrointestinal', '2023-10-22'),
(11, 11, 'Sessão de acupuntura', '2023-11-14'),
(12, 12, 'Sessão de quimioterapia', '2023-12-01'),
(13, 13, 'Odontologia preventiva', '2024-01-18'),
(14, 14, 'Ultrassonografia abdominal', '2024-02-27'),
(15, 15, 'Consulta ortopédica', '2024-03-22');

INSERT INTO ANIMAL (id_animal, nome, data_chegada, id_especie, porte, FK_PESSOA_id_pessoa, id_raca, id_pelagem)
VALUES
(1, 'Max', '2023-01-01', 1, 'Pequeno', 1, 1, 1),
(2, 'Luna', '2023-02-15', 2, 'Médio', 2, 2, 2),
(3, 'Charlie', '2023-03-10', 1, 'Pequeno', 3, 3, 3),
(4, 'Bella', '2023-04-05', 2, 'Grande', 4, 4, 4),
(5, 'Lucy', '2023-05-20', 1, 'Pequeno', 5, 5, 5),
(6, 'Cooper', '2023-06-18', 2, 'Médio', 6, 6, 6),
(7, 'Daisy', '2023-07-14', 1, 'Pequeno', 7, 7, 7),
(8, 'Rocky', '2023-08-09', 2, 'Grande', 8, 8, 8),
(9, 'Lola', '2023-09-25', 1, 'Pequeno', 9, 9, 9),
(10, 'Bailey', '2023-10-22', 2, 'Médio', 10, 10, 10),
(11, 'Sadie', '2023-11-17', 2, 'Grande', 11, 11, 11),
(12, 'Toby', '2023-12-13', 1, 'Pequeno', 12, 12, 12),
(13, 'Coco', '2024-01-08', 1, 'Médio', 13, 13, 13),
(14, 'Milo', '2024-02-03', 2, 'Pequeno', 14, 14, 14),
(15, 'Ruby', '2024-03-01', 2, 'Grande', 15, 15, 15),
(16, 'Leo', '2024-04-26', 1, 'Pequeno', 16, 16, 16),
(17, 'Molly', '2024-05-22', 1, 'Médio', 17, 17, 17),
(18, 'Maximus', '2024-06-18', 1, 'Grande', 18, 18, 18),
(19, 'Mia', '2024-07-14', 1, 'Pequeno', 19, 19, 19),
(20, 'Charlie', '2024-08-09', 2, 'Médio', 20, 20, 20),
(21, 'Lily', '2024-09-04', 2, 'Grande', 21, 21, 21),
(22, 'Oliver', '2024-10-01', 2, 'Pequeno', 22, 22, 22),
(23, 'Sophie', '2024-10-28', 1, 'Médio', 23, 23, 23),
(24, 'Bentley', '2024-11-24', 1, 'Grande', 24, 24, 24),
(25, 'Penny', '2024-12-20', 1, 'Pequeno', 25, 25, 25),
(26, 'Zeus', '2025-01-15', 2, 'Médio', 26, 26, 26),
(27, 'Daisy', '2025-02-10', 2, 'Grande', 27, 27, 27),
(28, 'Charlie', '2025-03-08', 1, 'Pequeno', 28, 28, 28),
(29, 'Luna', '2025-04-03', 1, 'Médio', 29, 29, 29),
(30, 'Cooper', '2025-04-30', 1, 'Grande', 30, 30, 30),
(31, 'Molly', '2025-05-27', 1, 'Pequeno', 31, 31, 31),
(32, 'Max', '2025-06-23', 2, 'Médio', 32, 32, 32),
(33, 'Lola', '2025-07-19', 2, 'Grande', 33, 33, 33),
(34, 'Bailey', '2025-08-15', 2, 'Pequeno', 34, 34, 34),
(35, 'Sadie', '2025-09-10', 1, 'Médio', 35, 35, 35),
(36, 'Toby', '2025-10-07', 1, 'Grande', 36, 36, 36),
(37, 'Coco', '2025-11-02', 1, 'Pequeno', 37, 37, 37),
(38, 'Milo', '2025-11-29', 2, 'Médio', 38, 38, 38),
(39, 'Ruby', '2025-12-26', 2, 'Grande', 39, 39, 39),
(40, 'Leo', '2026-01-21', 1, 'Pequeno', 40, 40, 40),
(41, 'Molly', '2026-02-17', 1, 'Médio', 41, 41, 41),
(42, 'Maximus', '2026-03-16', 1, 'Grande', 42, 42, 42),
(43, 'Mia', '2026-04-11', 1, 'Pequeno', 43, 43, 43),
(44, 'Charlie', '2026-05-08', 2, 'Médio', 44, 44, 44),
(45, 'Lily', '2026-06-04', 2, 'Grande', 45, 45, 45),
(46, 'Oliver', '2026-07-01', 2, 'Pequeno', 46, 46, 46),
(47, 'Sophie', '2026-07-29', 1, 'Médio', 47, 47, 47),
(48, 'Bentley', '2026-08-25', 1, 'Grande', 48, 48, 48),
(49, 'Penny', '2026-09-21', 1, 'Pequeno', 49, 49, 49),
(50, 'Zeus', '2026-10-18', 2, 'Médio', 50, 50, 50);

INSERT INTO FUNCIONARIO (id_funcionario, FK_PESSOA_id_pessoa, ocupacao)
VALUES
(1, 1, 'Veterinário'),
(2, 2, 'Recepcionista'),
(3, 3, 'Auxiliar de Limpeza'),
(4, 4, 'Veterinário'),
(5, 5, 'Recepcionista'),
(6, 6, 'Auxiliar de Limpeza'),
(7, 7, 'Veterinário'),
(8, 8, 'Recepcionista'),
(9, 9, 'Auxiliar de Limpeza'),
(10, 10, 'Veterinário'),
(11, 11, 'Recepcionista'),
(12, 12, 'Auxiliar de Limpeza'),
(13, 13, 'Veterinário'),
(14, 14, 'Recepcionista'),
(15, 15, 'Auxiliar de Limpeza'),
(16, 16, 'Veterinário'),
(17, 17, 'Recepcionista'),
(18, 18, 'Auxiliar de Limpeza'),
(19, 19, 'Veterinário'),
(20, 20, 'Recepcionista'),
(21, 21, 'Auxiliar de Limpeza'),
(22, 22, 'Veterinário'),
(23, 23, 'Recepcionista'),
(24, 24, 'Auxiliar de Limpeza'),
(25, 25, 'Veterinário'),
(26, 26, 'Recepcionista'),
(27, 27, 'Auxiliar de Limpeza'),
(28, 28, 'Veterinário'),
(29, 29, 'Recepcionista'),
(30, 30, 'Auxiliar de Limpeza'),
(31, 31, 'Veterinário'),
(32, 32, 'Recepcionista'),
(33, 33, 'Auxiliar de Limpeza'),
(34, 34, 'Veterinário'),
(35, 35, 'Recepcionista'),
(36, 36, 'Auxiliar de Limpeza'),
(37, 37, 'Veterinário'),
(38, 38, 'Recepcionista'),
(39, 39, 'Auxiliar de Limpeza'),
(40, 40, 'Veterinário'),
(41, 41, 'Recepcionista'),
(42, 42, 'Auxiliar de Limpeza'),
(43, 43, 'Veterinário'),
(44, 44, 'Recepcionista'),
(45, 45, 'Auxiliar de Limpeza'),
(46, 46, 'Veterinário'),
(47, 47, 'Recepcionista'),
(48, 48, 'Auxiliar de Limpeza'),
(49, 49, 'Veterinário'),
(50, 50, 'Recepcionista');
```

### 9 TABELAS E PRINCIPAIS CONSULTAS<br>

### Todas os códigos e tabelas se encontram no colab, link abaixo. 

#### Link do Colab: https://colab.research.google.com/drive/1Xa8sNnJWlX7lkmoH0PHXi7EGnG9m5GUN?usp=sharing

#### 9.1  SELECT DAS TABELAS

```

SELECT * FROM pessoa;

SELECT * FROM funcionario;

SELECT * FROM endereco;

SELECT * FROM animal;

SELECT * FROM  especie;

SELECT * FROM raca;

SELECT * FROM pelagem;

SELECT * FROM tipo_tratamento;

SELECT * FROM procedimento;

``` 

#### 9.2 CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)

```

SELECT * from pessoa WHERE nome_pessoa = 'Vanessa Souza';

SELECT * from animal a  where nome='Max';

SELECT * from endereco   where nome_rua='Rua A';

SELECT * from especie e  where tipo_especie ='Cachorro';

SELECT * from funcionario f where id_funcionario = 2;

SELECT * from pelagem p where tipo_pelagem ='Longo';

SELECT * from procedimento where descricao ='Esterilização';

SELECT * from raca where nome_raca = 'Persa';

SELECT * from tipo_tratamento where descricao = 'Cirurgia';


``` 

#### 9.3 CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)

```

SELECT p.nome_pessoa, p.cpf, a.porte FROM PESSOA p 
JOIN ANIMAL a ON p.id_animal = a.id_animal 
WHERE p.cpf < 50000000000 AND a.porte = 'Pequeno'

SELECT nome, porte FROM ANIMAL 
WHERE porte = 'Pequeno' OR porte = 'Médio'

SELECT nome_pessoa FROM PESSOA
WHERE id_animal IS NOT NULL

SELECT nome_pessoa FROM PESSOA
WHERE id_animal IS NOT NULL

SELECT nome, porte, data_chegada
FROM ANIMAL WHERE porte = 'Pequeno' OR data_chegada < '2022-01-01'

SELECT * FROM ANIMAL WHERE id_animal > 5 AND id_animal <= 8;

SELECT a.* FROM ANIMAL a
JOIN PESSOA p ON a.FK_PESSOA_id_pessoa = p.id_pessoa
WHERE p.telefone % 2 = 0;

SELECT * FROM ANIMAL
WHERE EXTRACT(YEAR FROM AGE(CURRENT_DATE, data_chegada)) >= 0;

SELECT a.nome AS nome_animal, p.nome_pessoa AS responsavel
FROM ANIMAL a
JOIN PESSOA p ON a.FK_PESSOA_id_pessoa = p.id_pessoa;

SELECT e.nome_rua AS rua, e.numero AS numero_endereco
FROM ANIMAL a
JOIN PESSOA p ON a.FK_PESSOA_id_pessoa = p.id_pessoa
JOIN ENDERECO e ON p.FK_ENDERECO_id_endereco = e.id_endereco
WHERE p.cpf = 12345678901;

SELECT p.descricao AS tratamento, p.data_hora AS data
FROM Procedimento p;

```

#### 9.4 CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>

```

SELECT * FROM PESSOA WHERE nome_pessoa LIKE 'V%';

SELECT * FROM ANIMAL WHERE nome LIKE '%o%';

SELECT * FROM RACA WHERE nome_raca LIKE '%Collie%' AND id_especie = 1; 

SELECT * FROM TIPO_TRATAMENTO WHERE descricao LIKE '%Vacinação%';

SELECT * FROM PESSOA WHERE email LIKE '%@example.com';

SELECT * FROM ANIMAL WHERE data_chegada > '2022-06-01';

SELECT * FROM Procedimento WHERE data_hora < '2022-05-01';

SELECT * FROM PESSOA WHERE CAST(telefone AS TEXT) LIKE '987654321%';

SELECT * FROM ANIMAL
WHERE id_animal IN (SELECT fk_ANIMAL_id_animal FROM Procedimento WHERE EXTRACT(DAY FROM data_hora) = 3 AND EXTRACT(YEAR FROM data_hora) <= 2022);

SELECT * FROM PROCEDIMENTO WHERE EXTRACT(DAY FROM data_hora) = 27;

SELECT * FROM PESSOA WHERE CAST(telefone as text) LIKE '%987654325%';

SELECT * FROM ANIMAL WHERE nome LIKE '%s';

```

#### 9.5 INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>

```

DELETE FROM pelagem WHERE tipo_pelagem = 'Curto';

DELETE from ANIMAL where fk_pessoa_id_pessoa IN (SELECT id_pessoa FROM pessoa
WHERE nome_pessoa = 'Vanessa Souza');

DELETE FROM especie WHERE id_especie = 1;

DELETE FROM procedimento WHERE id_animal = 1;

UPDATE raca SET nome_raca = 'Lhasa Apso' WHERE nome_raca = 'Golden Retriever';

UPDATE endereco SET numero = 3 WHERE numero = 20;

UPDATE animal SET id_especie = 3 WHERE id_animal = 1;

UPDATE pessoa SET nome_pessoa = 'Isabella S' WHERE id_animal = 3;

```

#### 9.6 CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>

```

SELECT A.*, PE.nome_pessoa, F.ocupacao,P.*, TP.*
FROM animal A
INNER JOIN pessoa PE ON A.FK_PESSOA_id_pessoa = PE.id_pessoa
INNER JOIN funcionario F ON A.FK_PESSOA_id_pessoa = F.FK_PESSOA_id_pessoa
INNER JOIN procedimento P ON A.id_animal = P.fk_ANIMAL_id_animal
INNER JOIN tipo_tratamento TP ON P.fk_tipo_tratamento_id_tratamento = TP.id_tipo_tratamento
ORDER BY P.data_hora;

SELECT A.*, P.*, TP.*, PE.*, F.*, E.*, PEL.*, R.*, EN.*
FROM animal A
INNER JOIN procedimento P ON A.id_animal = P.fk_ANIMAL_id_animal
INNER JOIN tipo_tratamento TP ON P. fk_TIPO_TRATAMENTO_id_tratamento = TP.id_tipo_tratamento
INNER JOIN pessoa PE ON A. FK_PESSOA_id_pessoa = PE.id_pessoa
INNER JOIN funcionario F ON PE.id_pessoa = F.FK_PESSOA_id_pessoa
INNER JOIN especie E ON A.id_especie = E.id_especie
INNER JOIN pelagem PEL ON A.id_pelagem = PEL.id_pelagem
INNER JOIN raca R ON A.id_raca = R.id_raca
INNER JOIN endereco EN ON PE. FK_ENDERECO_id_endereco = EN.id_endereco
ORDER BY A.nome;

SELECT E.*,PE.*, A.*,R.nome_raca,P.tipo_pelagem,ES.tipo_especie 
FROM animal A 
INNER JOIN pessoa PE ON PE.id_pessoa = A.FK_PESSOA_id_pessoa
INNER JOIN endereco E ON E.id_endereco = PE.FK_ENDERECO_id_endereco
INNER JOIN raca R ON R.id_raca = A.id_raca
INNER JOIN pelagem P ON P.id_pelagem = A.id_pelagem
INNER JOIN especie ES ON ES.id_especie = A.id_especie
ORDER BY A.data_chegada;

SELECT A.nome, E.tipo_especie
FROM animal A
INNER JOIN especie E ON A.id_especie = E.id_especie
ORDER BY id_animal;

SELECT E.*, P.*
FROM PESSOA P
INNER JOIN endereco E ON P.FK_ENDERECO_id_endereco = E.id_endereco
ORDER BY P.nome_pessoa;

SELECT A.nome, P.data_hora, TP.descricao
FROM procedimento P
INNER JOIN animal A ON  P.fk_ANIMAL_id_animal = A.id_animal
INNER JOIN tipo_tratamento TP ON P.fk_TIPO_TRATAMENTO_id_tratamento = TP.id_tipo_tratamento
ORDER BY P.data_hora;

```

#### 9.7 CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)

```

SELECT * FROM pessoa GROUP BY nome_pessoa, id_pessoa;

SELECT * FROM animal GROUP BY nome, id_animal;

SELECT * FROM endereco GROUP BY nome_rua, endereco.id_endereco;

SELECT * FROM especie GROUP BY especie.id_especie,tipo_especie;

SELECT id_funcionario, MAX(ocupacao) AS max_ocupacao
FROM funcionario
GROUP BY id_funcionario;

SELECT id_pelagem, tipo_pelagem
FROM pelagem
GROUP BY id_pelagem, tipo_pelagem;

SELECT fk_animal_id_animal, descricao
FROM procedimento
GROUP BY fk_animal_id_animal, descricao;

SELECT nome_raca, id_raca, id_especie
FROM raca
GROUP BY nome_raca, id_raca, id_especie;

SELECT id_tipo_tratamento, descricao
FROM tipo_tratamento
GROUP BY id_tipo_tratamento, descricao;

``` 

#### 9.8 CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)

```

SELECT PESSOA.id_pessoa, PESSOA.nome_pessoa, FUNCIONARIO.ocupacao
FROM PESSOA
LEFT JOIN FUNCIONARIO ON PESSOA.id_pessoa = FUNCIONARIO.FK_PESSOA_id_pessoa;

SELECT ANIMAL.nome, PESSOA.nome_pessoa
FROM ANIMAL
RIGHT JOIN PESSOA ON PESSOA.id_pessoa = ANIMAL.FK_PESSOA_id_pessoa;

SELECT PESSOA.id_pessoa, PESSOA.nome_pessoa, ANIMAL.nome AS nome_animal, ESPECIE.tipo_especie, RACA.nome_raca, PELAGEM.tipo_pelagem
FROM PESSOA
FULL JOIN ANIMAL ON PESSOA.id_pessoa = ANIMAL.FK_PESSOA_id_pessoa
FULL JOIN ESPECIE ON ANIMAL.id_especie = ESPECIE.id_especie
FULL JOIN RACA ON ANIMAL.id_raca = RACA.id_raca
FULL JOIN PELAGEM ON ANIMAL.id_pelagem = PELAGEM.id_pelagem;

SELECT PESSOA.id_pessoa, PESSOA.nome_pessoa, ANIMAL.nome AS nome_animal, ESPECIE.tipo_especie
FROM PESSOA
LEFT JOIN ANIMAL ON PESSOA.id_pessoa = ANIMAL.FK_PESSOA_id_pessoa
LEFT JOIN ESPECIE ON ANIMAL.id_especie = ESPECIE.id_especie;

SELECT ANIMAL.nome, TRATAMENTO.descricao
FROM ANIMAL
LEFT JOIN PROCEDIMENTO ON ANIMAL.id_animal = PROCEDIMENTO.fk_ANIMAL_id_animal
LEFT JOIN TIPO_TRATAMENTO TRATAMENTO ON PROCEDIMENTO.fk_TIPO_TRATAMENTO_id_tratamento = TRATAMENTO.id_tipo_tratamento
LIMIT 20;

```

#### 9.9 CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>

```

CREATE VIEW funcionario_e_ocupacao AS
SELECT id_funcionario,ocupacao
FROM funcionario;

SELECT * FROM funcionario_e_ocupacao;

CREATE VIEW quantd_funcionarios_por_ocupacao AS
SELECT f.ocupacao, COUNT(DISTINCT f.id_funcionario) AS quantidade_funcionarios
FROM funcionario f
GROUP BY f.ocupacao;

SELECT * FROM quantd_funcionarios_por_ocupacao;

CREATE VIEW animal_e_porte AS SELECT nome, porte
FROM animal
ORDER BY porte;

SELECT * FROM animal_e_porte;

SELECT e1.nome_rua, COUNT(e2.id_endereco) as quantidade_enderecos
FROM endereco e1
JOIN endereco e2 ON e1.nome_rua = e2.nome_rua
GROUP BY e1.nome_rua;

CREATE VIEW pessoas_mesmo_endereco AS
SELECT p1.nome_pessoa, p2.nome_pessoa AS nome_pessoa_relacionada
FROM pessoa p1
JOIN pessoa p2 on p1.fk_endereco_id_endereco = p2.fk_endereco_id_endereco
WHERE p1.id_pessoa <> p2.id_pessoa;

SELECT * FROM pessoas_mesmo_endereco;

SELECT p1.id_animal, COUNT(p2.id_animal) as quantidade_procedimentos
FROM Procedimento p1
JOIN Procedimento p2 ON p1.fk_animal_id_animal = p2.fk_animal_id_animal
GROUP BY p1.id_animal;

```

#### 9.10 SUBCONSULTAS (Mínimo 4)<br>

```

SELECT * FROM animal
WHERE fk_pessoa_id_pessoa NOT IN (
    SELECT DISTINCT fk_pessoa_id_pessoa
    FROM animal
    WHERE porte <> 'Pequeno'
);

SELECT * FROM funcionario
WHERE id_funcionario IN (
    SELECT DISTINCT id_funcionario
    FROM funcionario
    WHERE ocupacao = 'Veterinário'
);

SELECT * FROM funcionario
WHERE ocupacao IN ('Veterinário', 'Recepcionista');

SELECT id_animal, nome, porte, id_especie FROM animal
WHERE id_especie IN (1);

SELECT id_animal, nome, porte, id_especie FROM animal
WHERE id_especie IN (2);

```

### 10 RELATÓRIOS E GRÁFICOS

### Todas os relatórios e gráficos se encontram no colab, link abaixo. 

#### Link do Colab: https://colab.research.google.com/drive/1Xa8sNnJWlX7lkmoH0PHXi7EGnG9m5GUN?usp=sharing

### 11	AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)
#### b) Tempo de apresentação 6:40 
