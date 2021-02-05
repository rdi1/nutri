# nutri
ANALISE ESTATISTICO da CAMPANHA de AVALIAÇÃO NUTRICIONAL POPULACIONAL
README							
Raw data File=	Mcseed.cvs			Author =	RDI		
Separator =	“ : ”			Source =	FSF		
Records =	 286 rows per 33 columns  			Copyright´s	Reserved to FSF, write to the author to ask for permission jwnutri1@gmail.com		
							
COLUMN´s NAMES							
Id = number							
Sexo = gender 1→  boy     2→ girl							
IMC_Avi = BMI caculated at i interview → number x.yyyy 							
idade_Avi = age calculated at i interview → in months as INT number 							
Zscore_Avi = Nutricional Evaluation at i interview, according to WHO,s criteria → INT number 1-6							
NOTE: Column -> Nome = child´s first name was "anonymized" by removig it from the raw data column and creating a file copy from the received file.							
							
MAIN STATISTICS							
|# KPI| COLUMNS | FUNCTION | FILTER | TITLE | X AXIS | Y AXIS | GRAPH | DESCRIPTION |
|---|---|---|---|---|---|---|---|---|							
|1|Sexo|Count|1 / 2|TOTAL Gender´s frequency|||Text|Population Gender´s frequency|
|2|idade_Avi|Boxplot (idade_Avi/12=years)|i 1_10||||Boxplot|Ages Overview|
|3|IMC_Avi|Count|	1 / 2 + i 1_10|Participation|Avi|INT / Sexo|Histogram|Presence at each Nutricional Evaluation|
|4|IMC_Avi|Count|	1 / 2 + i 1&10+w/o NaN|Completed Participation|||Text|Presence at ALL Nutricional Evaluations|
|5|Zscore_Avi|Count/Percentage|	i 1_10|Zscore Evolution|Avi|Zscore|Histogram|Overview at each Nutricional Evaluation|
|6|Zscore_Avi|Value|Id + i 1_10 +w/o NaN	|Patient Id´s Nutritional Progress|Avi|Zscore_Avi|Line|Patient´s nutritional assessment|
