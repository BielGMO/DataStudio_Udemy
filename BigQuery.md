## Definição
- É um serviço Google que tem como função ser um Data Warehouse (Armazem de dados).
- Ele é *Serverless*, ou seja, funciona na nuvem.
- Ele é rápido, pois foi pensado para o Big Data. Além disso é barato, tendo cotas grátis.
    - Os primeiros 10GB de armazenatmento por mês são gratuitos.
    - O primeiro 1TB de dados de consulta processado por mês é gratuito.
- Ele também apresenta conexão com as outras plataformas do Google.

## Criando conta no BigQuery
Siga o passo a passo para criar sua conta no BigQuery:
1- Vá para o site https://cloud.google.com/bigquery
2- Clique em "Teste o BigQuery gratuitamente" **ou** na parte superior em "Comece a usar gratuitamente", como na imagem abaixo:
![2º Passo](/Imagens/BigQuery1.png)
3- Insira seus dados de acordo com o que for solicitado.
> Na forma de pagamento não se preocupe, você **não** será cobrado.Só haverá cobrança quando você ativar o faturamento automático.
4- Ao finalizar seu cadastro, você será redirecionado para o Google Cloud Platform (GCP), responda as questões solicitadas e pronto, temos nossa conta para Big Query criada.

A esquerda podemos ver todos os produtos disponíveis da Google:
![GCP Produtos](/Imagens/GCP1.png)]

Vamos procurar em "BigData" o serviço *BigQuery* e seleciona-lo:
![GCP BigQuery](/Imagens/GCP2.png)]

## Visão Geral
Vamos agora entender a interface do Big Query no GCP.

![GCP BigQuery](/Imagens/GCP3.png)]

1- **Menu de serviços** do Google como visto anteriormente.

2- **Projetos** listados existentes no seu GCP.

3- **Aba de pesquisa** da plataforma Google, pode-se encontrar serviços, API'S, entre outros.

4- **Cloud Shell** para utilizarção de linhas de comando.

5- **Notificações** existentes no seu GCP.

6- **Atalhos** possiveis na utilização do BigQuery no GCP.

7- **Consultas programadas** possibilita fazer a configuração de atualizações automáticas.

8- **Editor de Consultas** do BigQuery.

9- **Explorador de Projetos** onde ficam listados seus projetos de maneira mais detalhada.

### Entendendo as bases de dados

Vamos iniciar adicionando os dados públicos do BigQuery. Para isso clique no menu de Explorer como mostra a imagem e em seguida "Adicionar dados".

![GCP Explorer](/Imagens/GCP4.png)]

Fazendo esse passo siga com: *Fixar um projeto -> Digite o nome do projeto*. Na caixa de texto digite "bigquery-public-data".

Repare que um novo projeto foi fixado no seu explorador de projetos. 
![GCP Explorer](/Imagens/GCP5.png)]

Nesse projeto temos variadas bases de dados fornecidas pelo Google para que possamos treinar ou fazer projetos de teste.

Ao clicarmos em uma dessas bases podemos ver com mais detalhes sobre todos seus campos, observe a imagem abaixo a aba **Esquema** com o exemplo de **"new_york_citibike"->"citibiky_stations"**:
![GCP Explorer](/Imagens/GCP6.png)]

> Se for necessário podemos adicionar novas colunas por meio do botão **"Editar Esquema"** na parte inferior desta tela.

Na aba **Detalhes** podemos ver algumas informações sobre a tabela de modo geral, como tamanho, número de linhas, datas de criação e última modificação e entre outros.
![GCP Explorer](/Imagens/GCP7.png)]

Já na aba **Visualizar** temos os dados apresentados em forma de tabela.
![GCP Explorer](/Imagens/GCP8.png)]

### Criando gráfico através de consulta SQL

Para exemplificar como contruir visualizações de maneira rápida e simples entre o BigQuery e o DataStudio vamos utilizar a base de dados "Baseball" e a tabela "Schedule".

Para abrir a aba de consulta selecione a opção consulta com a tabela já selecionada no Explorer como na imagem abaixo:
![GCP Explorer](/Imagens/GCP9.png)]

Ao fazer isso um novo editor será aberto para que seja inserido o script SQL de consulta. Vamos começar calculando a **média de duração dos jogos (em minutos) por ano**.
```SQL
select
    avg(duration_minutes) as media_minutos_jogo,
    year
from `bigquery-public-data.baseball.schedules`
group by year
order by year;
```

Note que ao inserir o script temos um validador na parte superior, já indicando se teremos problemas ao executar esse script. Como resultado dessa consulta temos a informação que os jogos ocorreram em 2016 e a média de jogo em minutos foi de 184,65 minutos:
![GCP Explorer](/Imagens/GCP10.png)]

A partir dessa consulta podemos agora de maneira simples incluir o resultado em uma dahboard do Data Studio, basta selecionar a opção explorar dados e já será redirecionado ao Data Studio:
![GCP Explorer](/Imagens/GCP11.png)]