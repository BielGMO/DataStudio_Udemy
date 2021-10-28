## Inserir o gráfico de linha por data que está no final da página visão geral na página expedientes

1. Antes de tudo precisamos aumentar o tamanho do nosso layout. Para isso vamos no menu "Página → Configurações da página atual".
![Gráficos](/Imagens/Guia/Guia1.png)

2. Na aba direita vamos em "Estilo → Tamanho de tela". Nessa opção selecionamos personalizado e inserimos o tamanho desejado.
![Gráficos](/Imagens/Guia/Guia2.png)

3. Fazendo esse ajuste vamos ajustar nossos planos de fundo e em seguida adicionar o gráfico como solicitado.
![Gráficos](/Imagens/Guia/Guia3.png)

4. Ao inserir o gráfico ele não virá configurado como queremos. Vamos começar configurando a dimensão em que será apresentado, nesse caso será por Mês/Ano.
![Gráficos](/Imagens/Guia/Guia5.png)

5. Ao inserir "Data de entrada" o Data Studio por padrão irá apresentar a dimensão por dia, mas como citado anteriormente queremos agrupar esses resultados em "Mês/Ano". Clique na edição do campo como na imagem:
![Gráficos](/Imagens/Guia/Guia6.png)

6. Agora vamos corrigir nossa métrica, pois a apresentada está como "dias_na_fila" mas nós queremos apresentar a "quantidade de petições". Para isso clique em alterar métrica como apresentado na imagem:
![Gráficos](/Imagens/Guia/Guia7.png)

7. Clique em edição do campo e altere o nome para "Quantidade de petições":
![Gráficos](/Imagens/Guia/Guia8.png)

8. Vamos agora classificar os dados da data mais recente para a mais antiga, para isso altere a variável no campo classificar para data de entrada:
![Gráficos](/Imagens/Guia/Guia9.png)

9. Vamos agora editar o estilo do gráfico para deixar mais fácil e limpa a visualização, podemos começar exibindo os pontos e deixando visivel o rótulo de dados:
![Gráficos](/Imagens/Guia/Guia10.png)

10. Vamos também retirar as linhas de grade e a legenda, deixando o visual mais limpo:
![Gráficos](/Imagens/Guia/Guia11.png)

11. Por fim teremos um resultado semelhante a esse:
![Gráficos](/Imagens/Guia/Guia4.png)

12. Por fim, vamos finalizar adicionando uma borda, dando destaque para o gráfico:
![Gráficos](/Imagens/Guia/Guia12.png)

13. O resultado final será esse:
![Gráficos](/Imagens/Guia/Guia13.png)

14. Para deixar o gráfico dinâmico (interagindo com os outros), precisamos ativar manualmente a opção "Cruzamento de filtros":
![Gráficos](/Imagens/Guia/Guia14.png)