# BD-da-escola- create table turmas ( 

ID_turmas integer PRIMARY KEY AUTOINCREMENT, 

CODIGO turmas varchar (4) UNIQUE, 

PROFESSORES turmas char (25) NULL, 

ALUNOS turmas char (25) NULL, 

NOTAS turmas int (5) NULL 

); 

 

CREATE TABLE professores ( 

ID_professores INTEGER PRIMARY KEY AUTOINCREMENT, 

CODIGO professore VARCHAR (4) UNIQUE, 

NOME professore CHAR (25) NOT NULL, 

TELEFONE professore CHAR (11) NOT NULL, 

RG INTEGER NOT NULL, 

ID_turmas INTEGER, 

FOREIGN KEY (ID_turmas) REFERENCES turmas (ID_turmas) 

); 

 

create table alunos ( 

ID_alunos integer PRIMARY KEY AUTOINCREMENT, 

CODIGO alunos varchar(4) UNIQUE, 

NOME alunos char (25) NOT NULL, 

TELEFONE alunos char (11) NOT NULL, 

RG alunos int (10) NOT NULL 

ID_turmas integer 

); 

ALTER TABLE alunos 

ADD CONSTRAINT FOREIGN KEY (ID_turmas) REFERENCES turmas (ID_turmas) 

 

create table notas ( 

ID_notas integer PRIMARY KEY AUTOINCREMENT, 

CODIGO notas varchar(4) UNIQUE, 

BIM1 notas char (25) NOT NULL, 

BIM2 notas char (11) NOT NULL, 

BIM3 notas int (7) NULL 

ID_turmas integer 

); 

ALTER TABLE notas 

ADD CONSTRAINT FOREIGN KEY (ID_turmas) REFERENCES turmas (ID_turmas) 

 

create table funcionarios ( 

ID_funcionarios integer PRIMARY KEY AUTOINCREMENT, 

CODIGO funcionarios varchar(4) UNIQUE, 

SECRETARIA funcionarios char (25) NULL, 

LIMPEZA funcionarios char (25) NULL, 

MANUTENÇÃO funcionarios int (5) NULL 

); 

 

create table secretaria ( 

ID_secretaria integer PRIMARY KEY AUTOINCREMENT, 

CODIGO secretaria varchar(4) UNIQUE, 

NOME secretaria char (25) NOT NULL, 

TELEFONE secretaria char (11) NOT NULL, 

RG secretaria int (10) NOT NULL 

ID_funcionarios integer 

  ); 

ALTER TABLE secretaria 

ADD CONSTRAINT FOREIGN KEY (ID_funcionarios) REFERENCES funcionarios (ID_funcionarios) 

 

create table limpeza ( 

ID_limpeza integer PRIMARY KEY AUTOINCREMENT, 

CODIGO limpeza varchar(4) UNIQUE, 

NOME limpeza char (25) NOT NULL, 

TELEFONE limpeza char (11) NOT NULL, 

RG limpeza int (10) NOT NULL 

ID_funcionarios integer 

 ); 

ALTER TABLE limpeza 

ADD CONSTRAINT FOREIGN KEY (ID_funcionarios) REFERENCES funcionarios (ID_funcionarios) 

 

create table manutencao ( 

 ID_manutencao integer PRIMARY KEY AUTOINCREMENT, 

CODIGO manutencao varchar(4) UNIQUE, 

NOME manutencao char (25) NOT NULL, 

TELEFONE manutencao char (11) NOT NULL, 

RG manutencao int (10) NOT NULL 

ID_funcionarios integer 

  ); 

 ALTER TABLE manutencao 

ADD CONSTRAINT FOREIGN KEY (ID_funcionarios) REFERENCES funcionarios (ID_funcionarios) 

 

create table pais ( 

ID_pais integer PRIMARY KEY AUTOINCREMENT, 

CODIGO pais varchar(4) UNIQUE, 

MAE pais char (25) NULL, 

PAI pais char (25) NULL 

  ); 

 

create table MAE ( 

ID_MAE integer PRIMARY KEY AUTOINCREMENT, 

CODIGO MAE varchar(4) UNIQUE, 

CPF MAE char (25) NOT NULL, 

TELEFONE MAE char (11) NOT NULL, 

RG MAE int (10) NOT NULL 

 ID_pais integer 

  ); 

ALTER TABLE MAE 

ADD CONSTRAINT FOREIGN KEY (ID_pais) REFERENCES pais (ID_pais) 

 

create table PAI ( 

ID_PAI integer PRIMARY KEY AUTOINCREMENT, 

CODIGO PAI varchar(4) UNIQUE, 

CPF PAI char (25) NOT NULL, 

TELEFONE PAI char (11) NOT NULL, 

RG PAI int (10) NOT NULL 

ID_pais 

  ); 

ALTER TABLE PAI 

ADD CONSTRAINT FOREIGN KEY (ID_pais) REFERENCES pais (ID_pais) 

 

create table login ( 

ID_login integer PRIMARY KEY AUTOINCREMENT, 

CODIGO login varchar(4) UNIQUE, 

SENHA login int (4) UNIQUE, 

EMAIL login char (50) NULL 

  );	 

 

INSERT INTO `alunos` (`CODIGO`, `NOME`, `TELEFONE`, `RG`) VALUES 

(31, 'Pedro', '1192345781', '92187215060'), 

(32, 'maria', '11985637857', '69504731820'), 

(33, 'carlo', '11962332417', '28451679043'), 

(35, 'filipa', '11985614756', '80921345726'), 

(36, 'Vitor', '11947652093', '50692134789'), 

(37, 'Lara', '11984562130', '42716983051'), 

(38, 'Ricardo', '11936128575', '14982650739'), 

(39, 'Joana', '11994567829', '27394810615'), 

(391, 'Diego', '11963287541', '64283051974'), 

(396, 'Aline', '11958743629', '50921683742'), 

(395, 'Renato', '11930287516', '13897046251'), 

(394, 'Luiza', '11946712358', '69248135070'), 

(393, 'Gustavo', '11985471230', '37591420862'), 

(392, 'Mariana', '11993624751', '82014637915'), 

(397, 'Rodrigo', '11985462301', '19457863201') 

 

INSERT INTO `notas` (`CODIGO`, `BIM1`, `BIM2`, `BIM3`) VALUES 

(40, '5', '8', '7'), 

(41, '8', '2', '5'), 

(42, '9', '8', '9'), 

(43, '1', '4', '3'), 

(44, '2', '6', '6'), 

(46, '5', '6', '4'), 

(47, '9', '1', '2'), 

(48, '1', '7', '0'), 

(49, '1', '3', '5'), 

(496, '0', '4', '8'), 

(495, '5', '7', '1'), 

(494, '3', '6', '9'), 

(493,'8', '4', '3'), 

(492, '7', '7', '0'), 

(491, '4', '5', '2') 

 

INSERT INTO `secretaria` (`CODIGO`, `NOME`, `TELEFONE`, `RG`) VALUES 

(5, 'LARA', '11940808333', '698523654'), 

(6, 'ARTHUR', '11987521463', '784521698'), 

(7, 'KEYLA', '11963214587', '985632147'), 

(8, 'LUCAS', '11928573621', '587142695'), 

(9, 'ANA', '11940808214', '693214785'), 

(10, 'MARCOS', '11987541328', '452136987'), 

(11, 'SOFIA', '11963214587', '784521698'), 

(12, 'FERNANDO', '11974563289', '596874213'), 

(13, 'VANESSA', '11963214587', '369741258'), 

(14, 'ANDRE', '11940808214', '785214695'), 

(15, 'CAROLINA', '11987541328', '658932147'), 

(16, 'RENATO', '11940808214', '321456987'), 

(17, 'LARISSA', '11987541328', '789654123'), 

(18, 'PEDRO', '11963214587', '456789132'), 

(19, 'CARLA', '11974563289', '159263748'), 

(4, 'MIGUEL', '11963214587', '753951852') 

 

INSERT INTO `limpeza` (`CODIGO`, `NOME`, `TELEFONE`, `RG`) VALUES 

(50, 'MIGUEL', '11963214587', '753951852'), 

(51, 'LEONARDO', '11940808333', '698523654'), 

(52, 'GABRIELA', '11987521463', '784521698'), 

(53, 'ANA BEATRIZ', '11963214587', '985632147'), 

(54, 'LUCIA', '11928573621', '587142695'), 

(55, 'PEDRO HENRIQUE', '11940808214', '693214785'), 

(56, 'MARIA', '11987541328', '452136987'), 

(57, 'LUCAS', '11963214587', '784521698'), 

(58, 'GIOVANA', '11974563289', '596874213'), 

(59, 'FELIPE', '11963214587', '369741258'), 

(591, 'VITOR', '11940808214', '785214695'), 

(592, 'GUSTA', '11987541328', '658932147'), 

(593, 'KAROL', '11984562891', '145236987'), 

(594, 'GISELE', '11981258964', '698523586'), 

(595, 'THIAGO', '11947512384', '214520036') 

 

INSERT INTO `manutencao` (`CODIGO`, `NOME`, `TELEFONE`, `RG`) VALUES 

(60, 'CARLOS', '11963214586', '753951853'), 

(61, 'LEON', '11940808334', '698523655'), 

(62, 'ISABELLA', '11987521464', '784521699'), 

(63, 'ANA LUIZA', '11963214588', '985632148'), 

(64, 'FERNANDA', '11928573622', '587142696'), 

(65, 'BRUNO', '11940808215', '693214786'), 

(66, 'MARIANA', '11987541329', '452136988'), 

(67, 'RAFAEL', '11963214588', '784521699'), 

(68, 'MARIANA', '11974563288', '596874214'), 

(69, 'ANDRÉ', '11963214588', '369741259'), 

(691, 'VIVIAN', '11940808215', '785214696'), 

(692, 'GABRIEL', '11987541329', '658932148'), 

(693, 'CAROLINA', '11984562890', '145236988'), 

(694, 'GUILHERME', '11981258963', '698523587'), 

(695, 'LARISSA', '11947512385', '214520037') 

 

INSERT INTO `MAE` (`CODIGO`, `CPF`, `TELEFONE`, `RG`) VALUES 

(70, '369582471', '11940808666', '5095483337'), 

(71, '45678901234', '11959745216', '5095483326'), 

(72, '98765432109', '11980808667', '5095483338'), 

(73, '12345678901', '11959745217', '5095483327'), 

(74, '11111111111', '11990808668', '5095483339'), 

(75, '22222222222', '11959745218', '5095483328'), 

(76, '33333333333', '11940808669', '5095483340'), 

(77, '39674445745', '11959745219', '5095483329') 

 

INSERT INTO `responsavel` (`CODIGO`, `CPF`, `TELEFONE`, `RG`) VALUES 

(84, 'FERNANDA', '11928573622', '587142696'), 

(85, 'BRUNO', '11940808215', '693214786'), 

(86, 'MARIANA', '11987541329', '452136988'), 

(87, 'RAFAEL', '11963214588', '784521699'), 

(88, 'MARIANA', '11974563288', '596874214') 

 

INSERT INTO `professores` (`CODIGO`, `NOME`, `TELEFONE`, `RG`) VALUES 

(1, 'carla', '11928571430', '24038917651'), 

(2, 'rodrigo', '11967291087', '57420913865'), 

(3, 'lucas', '11981946275', '92183475060'), 

(4, 'rafael', '11937689502', '73615984204'), 

(5, 'sara', '11924567183', '89520473161'), 

(6, 'fabio', '11957681209', '40729583621'), 

(7, 'bruna', '11973256791', '61524970382'), 

(8, 'felipe', '11918476390', '74051268935'), 

(9, 'marina', '11967254901', '52193647084'), 

(43, 'Luiza', '11946712358', '69248135070'), 

(44, 'Gustavo', '11985471230', '37591420862'), 

(45, 'Mariana', '11993624751', '82014637915'), 

(13, 'VANESSA', '11963214587', '369741258'), 

(14, 'ANDRE', '11940808214', '785214695') 

 

Select * from professores 

Select * from alunos 

Select * from notas 

Select * from secretaria 

Select * from limpeza 

Select * from manutencao 

Select * from MAE 

Select * from PAI 

SELECT BIM3 FROM notas where bim3 < 5 

SELECT BIM3 FROM notas where bim3 > 5 
