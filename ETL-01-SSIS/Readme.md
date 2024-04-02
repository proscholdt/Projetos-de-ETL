<h1> Projeto de ETL utilizando SSIS <h1>

<h2> A ideia é fazer um simples job de ETL utilizando Microsoft SQL Server Integration Services - SSIS, extrair os dados de uma tabela de um banco de dados do SQL SERVER e salvar em um arquivo .txt </h2>

**Ferramentas utilizadas:**  
SQL SERVER   
VIZUAL STUDIO 2019 

<hr>

**Etapa 01**

Criar uma conexão com o SQL SERVER 

Conectamos ao Banco de Dados desejado (neste caso usaremos a base de testes importCSV)

<img src="imagens/imagem_01.png" />

<img src="imagens/imagem_01_b.png" />

<hr>

**Etapa 02**

Criar uma tarefa de fluxo de dados, chamaremos de Tarefa 01.

Na Tarefa 01 vamos extrair os dados da tabela dbo.Produtos.

<img src="imagens/imagem_02.png" />


Configurar a Origem, chamaremos de Origem OLE DB.

Vamos escolher a tabela dbo.Produtos e visualizar os dados.

<img src="imagens/imagem_02_b.png" />

<img src="imagens/imagem_02_c.png" />

Definir o Destino, chamaremos de Saida de Dados

Conectamos a Origem ao Destino.

<img src="imagens/imagem_02_d.png" />

Configurando Destino:

Definir o nome do arquivo, chamaremos de SaidaArquivo e colocamos o tipo .txt

Marcamos a opção “nomes de coluna na primeira linha de dados”

Deixamos o formato como “delimitado”

<img src="imagens/imagem_03_A.png" />

Definir o Delimitador como virgula (,) de acordo como está na nossa base.

<img src="imagens/imagem_03_B.png" />

Em mapeamentos vamos verificar o relacionamento entre as colunas de entrada e destino

<img src="imagens/imagem_04.png" />

<hr>

**Etapa 03**

Executando o Job e conferir arquivo gerado na paste de destino.

<img src="imagens/imagem_05_a.png" />

<img src="imagens/imagem_06_A.png" />

<img src="imagens/Imagem_7_B.png" />







