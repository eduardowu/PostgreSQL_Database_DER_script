/* Criando a tabela Partido */

CREATE TABLE PARTIDO (
ID INTEGER PRIMARY KEY,
NOME VARCHAR (60),
SIGLA VARCHAR (10)
);

/* Criando a tabela Candidato */

CREATE TABLE CANDIDATO (
ID INTEGER PRIMARY KEY,
NOME VARCHAR (60),
ID_PARTIDO INTEGER,
FOREIGN KEY (ID_PARTIDO) REFERENCES PARTIDO (ID)
);

/* Criando a tabela Votação */

CREATE TABLE VOTACAO (
ID INTEGER PRIMARY KEY,
DATA DATE,
ID_CANDIDATO INTEGER,
VOTOS INTEGER,
UF VARCHAR (2),
FOREIGN KEY (ID_CANDIDATO) REFERENCES CANDIDATO (ID)
);

/* Inserindo Registros na tabela Partido*/

INSERT INTO PARTIDO (ID, NOME, SIGLA) VALUES (1, ‘Partido 1’, ‘P1’);

INSERT INTO PARTIDO (ID, NOME, SIGLA) VALUES (2, ‘Partido 2’, ‘P2’);

INSERT INTO PARTIDO (ID, NOME, SIGLA) VALUES (3, ‘Partido 3’, ‘P3’);

INSERT INTO PARTIDO (ID, NOME, SIGLA) VALUES (4, ‘Partido 4’, ‘P4’);

INSERT INTO PARTIDO (ID, NOME, SIGLA) VALUES (5, ‘Partido 5’, ‘P5’);

/* Inserindo Registros na tabela Candidato*/

INSERT INTO CANDIDATO (ID, NOME, ID_PARTIDO) VALUES (1, ‘Candidato 1’, ‘1’);

INSERT INTO CANDIDATO (ID, NOME, ID_PARTIDO) VALUES (2, ‘Candidato 2’, ‘1’);

INSERT INTO CANDIDATO (ID, NOME, ID_PARTIDO) VALUES (3, ‘Candidato 3’, ‘2’);

INSERT INTO CANDIDATO (ID, NOME, ID_PARTIDO) VALUES (4, ‘Candidato 4’, ‘3’);

INSERT INTO CANDIDATO (ID, NOME, ID_PARTIDO) VALUES (5, ‘Candidato 5’, ‘4’);

/* Inserindo Registros na tabela Votação*/

INSERT INTO VOTACAO (ID, DATA, ID_CANDIDATO, VOTOS, UF) VALUES (1, ‘2018-10-07‘, ‘1’, 12345, ‘SP’);

INSERT INTO VOTACAO (ID, DATA, ID_CANDIDATO, VOTOS, UF) VALUES (2, ‘2018-10-07‘, ‘1’, 98323, ‘PR’);

INSERT INTO VOTACAO (ID, DATA, ID_CANDIDATO, VOTOS, UF) VALUES (3, ‘2018-10-07‘, ‘2’, 1726453, ‘SP’);

INSERT INTO VOTACAO (ID, DATA, ID_CANDIDATO, VOTOS, UF) VALUES (4, ‘2018-10-07‘, ‘2’, 16253, ‘PR’);

INSERT INTO VOTACAO (ID, DATA, ID_CANDIDATO, VOTOS, UF) VALUES (5, ‘2018-10-07‘, ‘3’, 293845, ‘SP’);

INSERT INTO VOTACAO (ID, DATA, ID_CANDIDATO, VOTOS, UF) VALUES (6, ‘2018-10-07‘, ‘3’, 98372, ‘PR’);

INSERT INTO VOTACAO (ID, DATA, ID_CANDIDATO, VOTOS, UF) VALUES (7, ‘2018-10-07‘, ‘4’, 46837, ‘SP’);

INSERT INTO VOTACAO (ID, DATA, ID_CANDIDATO, VOTOS, UF) VALUES (8, ‘2018-10-07‘, ‘4’, 327264, ‘PR’);
