CREATE DATABASE IF NOT EXISTS PlanosSaude_DB;
USE PlanosSaude_DB;

SET lc_time_names = 'pt_BR';
SET lc_messages = 'pt_BR';

CREATE TABLE IF NOT EXISTS demonstrativos_contabeis (
    Data DATE,
    Reg_ANS INT,
    CD_Conta_Contabil VARCHAR(20),
    Descricao VARCHAR(255),
    VL_Saldo_Inicial DECIMAL(15,2),
    VL_Saldo_Final DECIMAL(15,2),
    PRIMARY KEY (Data, Reg_ANS, CD_Conta_Contabil)
);


CREATE TABLE IF NOT EXISTS operadoras_saude (
    Registro_Ans  VARCHAR(10) PRIMARY KEY, 
    CNPJ VARCHAR(18) UNIQUE NOT NULL, 
    Razao_Social VARCHAR(255) NOT NULL,
    Nome_Fantasia VARCHAR(255),
    Modalidade VARCHAR(100),
    Logradouro VARCHAR(255),
    Numero VARCHAR(20),
    Complemento VARCHAR(100),
    Bairro VARCHAR(100),
    Cidade VARCHAR(100),
    Uf CHAR(2),  
    CEP VARCHAR(8),  
    DDD VARCHAR(2),
    Telefone VARCHAR(20),
    Fax VARCHAR(20),
    Endereco_Eletronico VARCHAR(255),
    Representante VARCHAR(255),
    Cargo_Representante VARCHAR(100),
    Regiao_de_Comercializacao TEXT,
    Data_Registro_ANS DATE
);


SELECT *
FROM operadoras_saude;


LOAD DATA INFILE '1T2023.csv' /*Funfo*/
INTO TABLE demonstrativos_contabeis
CHARACTER SET utf8mb4
FIELDS TERMINATED BY ';'
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
IGNORE 1 ROWS
(Data, Reg_ANS, CD_Conta_Contabil, Descricao, @VL_Saldo_Inicial, @VL_Saldo_Final)
SET VL_Saldo_Inicial = REPLACE(@VL_Saldo_Inicial, ',', '.'), VL_Saldo_Final = REPLACE(@VL_Saldo_Final, ',', '.');
SET Data = STR_TO_DATE(TRIM(@Data), '%Y-%m-%d');


LOAD DATA INFILE '2T2023.csv' /*Funfo*/
INTO TABLE demonstrativos_contabeis
CHARACTER SET utf8mb4
FIELDS TERMINATED BY ';'
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
IGNORE 1 ROWS
(Data, Reg_ANS, CD_Conta_Contabil, Descricao, @VL_Saldo_Inicial, @VL_Saldo_Final)
SET VL_Saldo_Inicial = REPLACE(@VL_Saldo_Inicial, ',', '.'), VL_Saldo_Final = REPLACE(@VL_Saldo_Final, ',', '.');
SET Data = STR_TO_DATE(TRIM(@Data), '%Y-%m-%d');


LOAD DATA INFILE '3T2023.csv' /*Funfo*/
INTO TABLE demonstrativos_contabeis
CHARACTER SET utf8mb4
FIELDS TERMINATED BY ';'
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
IGNORE 1 ROWS
(Data, Reg_ANS, CD_Conta_Contabil, Descricao, @VL_Saldo_Inicial, @VL_Saldo_Final)
SET VL_Saldo_Inicial = REPLACE(@VL_Saldo_Inicial, ',', '.'), VL_Saldo_Final = REPLACE(@VL_Saldo_Final, ',', '.');
SET Data = STR_TO_DATE(TRIM(@Data), '%Y-%m-%d');


LOAD DATA INFILE '4T2023.csv' 
INTO TABLE demonstrativos_contabeis
CHARACTER SET utf8mb4
FIELDS TERMINATED BY ';'
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
IGNORE 1 ROWS
(Data, Reg_ANS, CD_Conta_Contabil, Descricao, @VL_Saldo_Inicial, @VL_Saldo_Final)
SET VL_Saldo_Inicial = REPLACE(@VL_Saldo_Inicial, ',', '.'), VL_Saldo_Final = REPLACE(@VL_Saldo_Final, ',', '.');
SET Data = STR_TO_DATE(TRIM(@Data), '%Y-%m-%d');



LOAD DATA INFILE '1T2024.csv' /*Funfo*/
INTO TABLE demonstrativos_contabeis
CHARACTER SET utf8mb4
FIELDS TERMINATED BY ';'
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
IGNORE 1 ROWS
(Data, Reg_ANS, CD_Conta_Contabil, Descricao, @VL_Saldo_Inicial, @VL_Saldo_Final)
SET VL_Saldo_Inicial = REPLACE(@VL_Saldo_Inicial, ',', '.'), VL_Saldo_Final = REPLACE(@VL_Saldo_Final, ',', '.');
SET Data = STR_TO_DATE(TRIM(@Data), '%Y-%m-%d');




LOAD DATA INFILE '2T2024.csv' /*Funfo*/
INTO TABLE demonstrativos_contabeis
CHARACTER SET utf8mb4
FIELDS TERMINATED BY ';'
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
IGNORE 1 ROWS
(Data, Reg_ANS, CD_Conta_Contabil, Descricao, @VL_Saldo_Inicial, @VL_Saldo_Final)
SET VL_Saldo_Inicial = REPLACE(@VL_Saldo_Inicial, ',', '.'), VL_Saldo_Final = REPLACE(@VL_Saldo_Final, ',', '.');
SET Data = STR_TO_DATE(TRIM(@Data), '%Y-%m-%d');


LOAD DATA INFILE '3T2024.csv' /*Funfo*/
INTO TABLE demonstrativos_contabeis
CHARACTER SET utf8mb4
FIELDS TERMINATED BY ';'
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
IGNORE 1 ROWS
(Data, Reg_ANS, CD_Conta_Contabil, Descricao, @VL_Saldo_Inicial, @VL_Saldo_Final)
SET VL_Saldo_Inicial = REPLACE(@VL_Saldo_Inicial, ',', '.'), VL_Saldo_Final = REPLACE(@VL_Saldo_Final, ',', '.');
SET Data = STR_TO_DATE(TRIM(@Data), '%Y-%m-%d');


LOAD DATA INFILE '4T2024.csv' /*Funfo*/
INTO TABLE demonstrativos_contabeis
CHARACTER SET utf8mb4
FIELDS TERMINATED BY ';'
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
IGNORE 1 ROWS
(Data, Reg_ANS, CD_Conta_Contabil, Descricao, @VL_Saldo_Inicial, @VL_Saldo_Final)
SET VL_Saldo_Inicial = REPLACE(@VL_Saldo_Inicial, ',', '.'), VL_Saldo_Final = REPLACE(@VL_Saldo_Final, ',', '.');
SET Data = STR_TO_DATE(TRIM(@Data), '%Y-%m-%d');

SELECT *
FROM demonstrativos_contabeis;
SELECT *
FROM operadoras_saude;


LOAD DATA INFILE 'Relatorio_cadop.csv' 
INTO TABLE operadoras_saude 
CHARACTER SET utf8mb4 
FIELDS TERMINATED BY ';' 
OPTIONALLY ENCLOSED BY '"' 
LINES TERMINATED BY '\n' 
IGNORE 1 ROWS 
(@Registro_Ans, @CNPJ, @Razao_Social, @Nome_Fantasia, @Modalidade, @Logradouro, @Numero, @Complemento, @Bairro, @Cidade, @Uf, @CEP, @DDD, @Telefone, @Fax, @Endereco_Eletronico, @Representante, @Cargo_Representante, @Regiao_de_Comercializacao, @Data_Registro_ANS) 
SET Data_Registro_ANS = STR_TO_DATE(TRIM(@Data_Registro_ANS), '%Y-%m-%d');

WITH despesas_trimestre AS (
    SELECT
        o.Registro_Ans,
        o.Razao_Social,
        SUM(d.VL_Saldo_Final - d.VL_Saldo_Inicial) AS total_despesas
    FROM
        demonstrativos_contabeis d
    JOIN
        operadoras_saude o ON d.Reg_ANS = o.Registro_Ans
    WHERE
        d.CD_Conta_Contabil = 'EVENTOS/ SINISTROS CONHECIDOS OU AVISADOS DE ASSISTÊNCIA A SAÚDE MEDICO HOSPITALAR'
        AND d.Data >= DATE_FORMAT(CURRENT_DATE - INTERVAL 3 MONTH, '%Y-%m-01')
        AND d.Data < DATE_FORMAT(CURRENT_DATE, '%Y-%m-01')
    GROUP BY
        o.Registro_Ans, o.Razao_Social
)
SELECT
    Registro_Ans,
    Razao_Social,
    total_despesas
FROM
    despesas_trimestre
ORDER BY
    total_despesas DESC
LIMIT 10;


WITH despesas_ultimo_ano AS (
    SELECT
        o.Registro_Ans,
        o.Razao_Social,
        SUM(d.VL_Saldo_Final - d.VL_Saldo_Inicial) AS total_despesas
    FROM
        demonstrativos_contabeis d
    JOIN
        operadoras_saude o ON d.Reg_ANS = o.Registro_Ans
    WHERE
        d.CD_Conta_Contabil = 'EVENTOS/ SINISTROS CONHECIDOS OU AVISADOS DE ASSISTÊNCIA A SAÚDE MEDICO HOSPITALAR'
        AND d.Data >= DATE_FORMAT(CURRENT_DATE - INTERVAL 1 YEAR, '%Y-%m-01')
        AND d.Data < DATE_FORMAT(CURRENT_DATE, '%Y-%m-01')
    GROUP BY
        o.Registro_Ans, o.Razao_Social
)
SELECT
    Registro_Ans,
    Razao_Social,
    total_despesas
FROM
    despesas_ultimo_ano
ORDER BY
    total_despesas DESC
LIMIT 10;


