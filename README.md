<<<<<<< HEAD
# Projeto 8: Análise de Multas Ambientais 🌳💰
=======
# Projeto 7: Análise de Multas Ambientais 🌳💰
>>>>>>> 1f9f127 (atualização)
---
## O Cenário 👨‍💼

Você foi contratado(a) como analista de dados júnior em uma agência de transparência governamental. Sua primeira tarefa é analisar um grande conjunto de dados sobre arrecadações de multas ambientais aplicadas pelo IBAMA.

Um gestor sênior precisa de um relatório visual para uma audiência pública sobre a efetividade das multas. Ele pediu uma análise que destaque os "casos extremos": as multas de maior e menor valor.

Sua missão é usar seus superpoderes em Python para transformar esses dados brutos em um gráfico claro e impactante, mostrando quem são os responsáveis pelas maiores e menores parcelas de multas ambientais.

### 💡 O que é um "Bem Tutelado"?
No contexto de fiscalização ambiental, quando ocorre um crime (como desmatamento ilegal), os fiscais podem apreender os equipamentos, veículos, madeira, ou qualquer outro item usado na infração. Esses itens são os **"bens"**. A partir do momento da apreensão, o Estado se torna o guardião legal (o **"tutor"**) desses bens até que o processo legal seja concluído. Portanto, "bens tutelados" são os itens apreendidos em crimes ambientais que estão sob a proteção e responsabilidade do governo.

## 📋 Sugestões e Requisitos da Missão

O gestor precisa de um visual direto para a apresentação. Ele não terá tempo de analisar planilhas ou códigos. Portanto, seu script deve atender aos seguintes requisitos:

1.  **Carregar os Dados:** Seu script deve ser capaz de ler os dados do arquivo `arrecadacao_de_bens_tutelados.csv`. Lembre-se que ele tem um formato especial!

2.  **Definir a Métrica:** O que define o "impacto" de uma multa? Para esta análise, use a coluna **'Valor Pago'** como principal indicador.

3.  **Identificar os Extremos:** O script deve encontrar:

      * As 10 entidades (Pessoa Física ou Empresa) com as **maiores** multas.
      * As 10 entidades com as **menores** multas.

4.  **Visualização de Dados:** Crie um único gráfico de barras usando `pandas`, `matplotlib` ou `seaborn` que mostre lado a lado os valores das multas desses 20 casos extremos (os 10 maiores e os 10 menores).

5.  **Resultado Final:** Ao executar o script, o resultado esperado é um gráfico salvo como imagem (ou exibido na tela) que seja claro, com títulos e rótulos, pronto para ser inserido na apresentação do seu gestor.

## 💡 Roteiro Sugerido para o Sucesso

Se não souber por onde começar, siga estes passos:

1.  **Importe as bibliotecas** `pandas` e `matplotlib.pyplot`. Elas serão suas principais ferramentas.
2.  **Carregue os dados** para um DataFrame. **Atenção:** Este arquivo usa `;` como separador e `,` como decimal. Dica: `pd.read_csv('arrecadacaobenstutelados.csv', sep=';', decimal=',')`.
3.  **Limpe os dados:** Verifique se a coluna `Valor Pago` foi carregada como um número. Se não, converta-a.
4.  **Ordene o DataFrame**: Use a função `.sort_values()` para ordenar os dados pela coluna 'Valor Pago'.
5.  **Selecione os extremos**: Crie dois novos DataFrames: um com os 10 primeiros da lista ordenada (os maiores valores, usando `.tail(10)`) e outro com os 10 primeiros (os menores valores, usando `.head(10)`).
6.  **Combine os dados**: Junte esses dois DataFrames em um único para facilitar a plotagem. A função `pd.concat()` é perfeita para isso.
7.  **Crie o gráfico**:
      * Use `plt.bar()` para gerar o gráfico de barras.
      * No eixo `x`, coloque o 'Nome ou Razão Social'; no eixo `y`, o 'Valor Pago'.
      * Use `plt.title()`, `plt.xlabel()` e `plt.ylabel()` para adicionar um título e rótulos claros.
8.  **Exiba ou salve o resultado**: Use `plt.show()` para vê-lo ou `plt.savefig('analise_multas.png')` para salvá-lo como um arquivo.

Boa sorte, analista! A transparência sobre a aplicação de multas ambientais no país depende da sua capacidade de transformar dados em uma história visual. 💪
