# Projeto 7: Análise de Desempenho de Clubes ⚽️
---
## O Cenário 👨‍💼

Você foi contratado(a) como analista de dados júnior em uma consultoria esportiva do seu time do coração. Sua primeira grande tarefa é analisar um conjunto de dados do campeonato de futebol e extrair informações valiosas.

Um jornalista esportivo pediu à sua empresa uma análise visual para uma matéria sobre "Os Opostos do Campeonato: Times de Maior e Menor Sucesso".

Sua missão é usar seus superpoderes em Python para criar um gráfico que mostre claramente os times com o melhor e o pior desempenho, com base nos dados fornecidos.

## 📋 Sugestões e Requisitos da Missão

O jornalista precisa de um visual claro e direto para a matéria. Ele não entende e nem sabe ler o resultado do terminal. Portanto, seu script deve atender aos seguintes requisitos:

1.  **Carregar os Dados:** Seu script deve ser capaz de ler os dados da tabela fornecida `Tabela_Clubes.csv`.

2.  **Definir Sucesso:** O que torna um time "bem-sucedido"? Para esta análise, você pode usar a coluna **'Vitorias'** como principal indicador. Times com mais vitórias são mais bem-sucedidos.

3.  **Identificar os Extremos:** O script deve encontrar:

      * Os 10 times com **mais** vitórias.
      * Os 10 times com **menos** vitórias.

4.  **Visualização de Dados:** Crie um gráfico de barras usando a biblioteca `seaborn` que mostre lado a lado o número de vitórias desses 10 times (os 5 melhores e os 5 piores).

5.  **Resultado Final:** Ao executar o script, o resultado esperado é um gráfico salvo como imagem (ou exibido na tela) que seja claro, com títulos e rótulos, pronto para ser enviado ao jornalista. Por exemplo:


## 💡 Roteiro Sugerido para o Sucesso

Se não souber por onde começar, siga estes passos:

1.  **Importe as bibliotecas** `pandas`, `seaborn` e `matplotlib.pyplot`. Elas serão suas principais ferramentas.
2.  **Carregue os dados** para um DataFrame do pandas. Dica: `pd.read_csv('Tabela_Clubes.csv')`.
3.  **Ordene o DataFrame**: Use a função `.sort_values()` para ordenar os clubes pelo número de 'Vitorias'.
4.  **Selecione os times**: Crie dois novos DataFrames: um com os 10 primeiros da lista ordenada (`.head(n)`) e outro com os 10 últimos (`.tail(n)`).
5.  **Combine os dados**: Junte esses dois DataFrames em um único para facilitar a plotagem. A função `pd.concat()` é perfeita para isso.
6.  **Crie o gráfico**:
      * Use `sns.barplot()` para gerar o gráfico de barras.
      * No eixo `x`, coloque o nome do 'Clubes'; no eixo `y`, o número de 'Vitorias'.
      * Use `plt.title()`, `plt.xlabel()` e `plt.ylabel()` para adicionar um título e rótulos claros.
      * Para garantir que os nomes dos clubes não fiquem sobrepostos, você pode usar `plt.xticks(rotation=45)`.
7.  **Exiba ou salve o resultado**: Use `plt.show()` para ver o gráfico ou `plt.savefig('analise_clubes.png')` para salvá-lo como um arquivo de imagem.

Boa sorte, analista\! A clareza da matéria do jornalista depende da sua capacidade de transformar dados em uma história visual. 💪