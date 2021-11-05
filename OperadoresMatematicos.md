--------------------------------------------------------------------------Operadores Matematicos --------------------------------------------------------------------------

-- SELECT * FROM senso

-- usando operador =
SELECT * FROM senso 
WHERE nome_mun = 'Dourado' 
AND cod_uf  = '35' 
AND ano= '2014';

-- usando o operador >
SELECT * FROM senso 
WHERE populacao > 100000
AND ano = '2014'
AND cod_uf ='35'

-- usando o operador <
SELECT * FROM senso 
WHERE populacao < 50000
AND ano = '2014'

-- usando o operador <>
SELECT * FROM senso 
WHERE (cod_uf <> '35'or cod_uf <> '14')
AND ano<>'2014';

--combinando operadores 
SELECT * FROM senso 
WHERE populacao <=100000
AND populacao >= 50000
AND cod_uf = '35'
AND nome_mun = 'Vinhedo'
AND ano= '2014'

-- operador + 
select  13+2 AS retorno;

-- operador *
select  13*2 AS retorno;

-- operador -
select  13-2 AS retorno;

SELECT  5-6 AS retorno;

-- operador /
SELECT  14/2 AS retorno;

-- operador %
SELECT  14%2 AS retorno;

-- combinando operadores 
SELECT ((1+4)*(3*3))/5 AS retorno;

-- script  projetando acrescimento de 10% populacao 
SELECT nome_mun, populacao,populacao*1.10 AS pop_projecao
FROM senso
WHERE ano = '2014';

-- script projetando acrescimo de 10% populacao
SELECT nome_mun,populacao,
	populacao*0.10 AS descrescimo,
	populacao - (populacao*0.10) projeto_pop
FROM senso 
WHERE ano = '2014'
