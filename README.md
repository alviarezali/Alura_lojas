# Análise de Desempenho - Alura Store

## Propósito da Análise

Este projeto tem como objetivo realizar uma análise de dados das vendas e do desempenho de quatro lojas da rede Alura Store. O Sr. João, proprietário da rede, deseja vender uma das lojas para obter capital e investir em um novo negócio. Fomos contratados como analistas de dados para identificar qual das quatro lojas apresenta o menor desempenho comparativo, fornecendo assim uma recomendação embasada em dados para auxiliar na decisão do Sr. João.

As métricas chave analisadas para determinar o desempenho de cada loja foram:
* Faturamento total
* Categorias de produtos mais populares
* Média de avaliação dos clientes
* Produtos mais e menos vendidos (em termos de faturamento)
* Custo médio do frete

## Estrutura do Projeto e Organização dos Arquivos

O projeto utiliza dados de quatro lojas distintas, cada uma representada por um arquivo CSV. A análise completa foi realizada utilizando um notebook Google Colab (`AluraStoreBr.ipynb`), que centraliza a importação dos dados, o processamento, a análise das métricas e a geração das visualizações.

* **`/base-de-dados-challenge-1/`**: Pasta (hipotética, conforme mencionado no desafio) contendo os 4 arquivos CSV, um para cada loja.
    * `loja_1.csv` (Exemplo de nome)
    * `loja_2.csv` (Exemplo de nome)
    * `loja_3.csv` (Exemplo de nome)
    * `loja_4.csv` (Exemplo de nome)
* **`AluraStoreBr.ipynb`**: Notebook Google Colab contendo todo o código Python para a análise, desde a importação dos dados até a geração dos gráficos e do relatório final.

## Análise Detalhada e Resultados

A análise foi conduzida passo a passo, avaliando cada métrica para as quatro lojas.

### 1. Análise do Faturamento

* **Objetivo:** Comparar o faturamento total (soma dos preços dos produtos vendidos) entre as lojas.
* **Metodologia:** Calculou-se a soma da coluna `Preço` para cada loja[cite: 65]. Foram gerados histogramas e boxplots para visualizar a distribuição dos preços[cite: 64, 65], um gráfico de barras comparando o faturamento total [cite: 65] e um gráfico de pizza mostrando a participação percentual de cada loja no faturamento total[cite: 66].
* **Resultados:**
    * Loja 1: R$ 1.534.509,12 (26.1%) [cite: 65, 66]
    * Loja 2: R$ 1.488.459,06 (25.4%) [cite: 65, 66]
    * Loja 3: R$ 1.464.025,03 (24.9%) [cite: 65, 66]
    * Loja 4: R$ 1.384.497,58 (23.6%) [cite: 65, 66]
* **Insight:** A Loja 4 apresentou o menor faturamento total, enquanto a Loja 1 teve o maior[cite: 66]. A distribuição de preços (visualizada nos histogramas e boxplots) mostrou uma concentração de vendas em produtos de menor valor em todas as lojas, com alguns outliers de alto valor[cite: 64, 65].

### 2. Vendas por Categoria

* **Objetivo:** Identificar as categorias de produtos mais relevantes em termos de faturamento para cada loja.
* **Metodologia:** Agrupamento dos dados por `Categoria do Produto` e soma da coluna `Preço`[cite: 67]. Geração de gráficos de barras para cada loja mostrando o faturamento por categoria[cite: 67, 68, 28].
* **Resultados:**
    * A categoria "móveis" foi a de maior faturamento em todas as lojas, seguida por "eletrônicos"[cite: 68, 28].
    * Categorias como "livros", "instrumentos musicais" e "brinquedos" apresentaram os menores faturamentos[cite: 68, 28].
    * Embora o padrão fosse similar, a Loja 4 registrou valores absolutos menores nas categorias principais em comparação com as outras[cite: 68, 28].
* **Insight:** O perfil de consumo por categoria é semelhante entre as lojas, mas a Loja 4 demonstra menor volume de vendas nas categorias mais rentáveis[cite: 68, 28].

### 3. Média de Avaliação das Lojas

* **Objetivo:** Comparar a satisfação do cliente entre as lojas através da média das avaliações.
* **Metodologia:** Cálculo da média, moda e desvio padrão da coluna `Avaliação da compra` para cada loja[cite: 69]. Geração de um gráfico de barras comparativo[cite: 69, 70].
* **Resultados (Médias):**
    * Loja 3: ~4.05 [cite: 70]
    * Loja 2: ~4.04 [cite: 70]
    * Loja 4: ~4.00 [cite: 70]
    * Loja 1: ~3.98 [cite: 70]
    * A moda (avaliação mais frequente) foi 5 em todas as lojas[cite: 70].
* **Insight:** As avaliações são muito próximas, com a Loja 1 apresentando a menor média e a Loja 3 a maior[cite: 70]. A Loja 4 ficou ligeiramente abaixo das Lojas 2 e 3[cite: 70]. Apesar das médias próximas a 4, a nota mais comum (moda) é a máxima (5), indicando uma polarização nas avaliações ou um grande número de clientes muito satisfeitos[cite: 70].

### 4. Produtos Mais e Menos Vendidos

* **Objetivo:** Identificar os produtos com maior e menor faturamento total em cada loja.
* **Metodologia:** Agrupamento por `Produto`, soma da coluna `Preço` e identificação dos produtos com valor máximo e mínimo[cite: 71, 75]. Geração de um gráfico de barras comparativo com escala logarítmica para visualizar os extremos[cite: 76, 78].
* **Resultados:**
    * **Mais Vendidos (Faturamento):** Loja 1 (TV Led UHD 4K: R$ 189.534,28), Loja 2 (Celular Plus X42: R$ 150.967,83), Loja 3 (Geladeira: R$ 133.185,99), Loja 4 (Celular Plus X42: R$ 128.930,07)[cite: 73, 78].
    * **Menos Vendidos (Faturamento):** Loja 1 (Corda de pular: R$ 870,89), Loja 2 (Cubo mágico 8x8: R$ 858,22), Loja 3 (Cubo mágico 8x8: R$ 853,81), Loja 4 (Corda de pular: R$ 939,74)[cite: 73, 78].
* **Insight:** O produto de maior faturamento da Loja 4, embora seja um item popular (Celular Plus X42), gerou significativamente menos receita do que os produtos de topo das outras lojas[cite: 73, 78]. Os produtos de menor faturamento geraram valores abaixo de R$ 1.000,00 em todas as lojas[cite: 73, 78].

### 5. Frete Médio por Loja

* **Objetivo:** Comparar o custo médio do frete entre as lojas.
* **Metodologia:** Cálculo da média, máximo e desvio padrão da coluna `Frete` para cada loja[cite: 78]. Geração de um gráfico de barras comparativo[cite: 78, 80].
* **Resultados (Médias):**
    * Loja 1: R$ 34,69 [cite: 44, 80]
    * Loja 2: R$ 33,62 [cite: 53, 80]
    * Loja 3: R$ 33,07 [cite: 55, 80]
    * Loja 4: R$ 31,28 [cite: 60, 80]
* **Insight:** A Loja 4 possui o menor custo médio de frete, enquanto a Loja 1 tem o maior[cite: 80]. A Loja 1 também apresenta a maior variabilidade nos custos de frete (maior desvio padrão)[cite: 44, 80].

## Exemplos de Gráficos e Insights Obtidos

Diversos gráficos foram gerados para facilitar a compreensão dos dados:

* **Gráfico de Pizza (Faturamento %):** Mostrou visualmente a participação de cada loja no faturamento total, destacando a menor contribuição da Loja 4 (23.6%)[cite: 66].
* **Gráficos de Barras (Faturamento por Categoria):** Permitiram comparar o desempenho das categorias entre as lojas, evidenciando a liderança de "móveis" e "eletrônicos" e o desempenho inferior da Loja 4 nessas categorias-chave[cite: 68, 28].
* **Gráfico de Barras Agrupado (Avaliação Média, Moda, Desvio Padrão):** Facilitou a comparação direta das métricas de avaliação, mostrando a proximidade dos resultados, mas com a Loja 1 ligeiramente atrás na média[cite: 70].
* **Gráfico de Barras com Escala Log (Produtos Extremos):** Essencial para visualizar produtos com faturamentos tão distintos (máximos e mínimos), confirmando o menor faturamento do produto de topo da Loja 4[cite: 78].
* **Gráfico de Barras Agrupado (Métricas de Frete):** Comparou o custo máximo, médio e o desvio padrão do frete, indicando a Loja 4 como a mais econômica em média e a Loja 1 como a mais cara e variável[cite: 80].

## Instruções para Executar o Notebook

Para reproduzir esta análise, siga os passos abaixo:

1.  **Obtenha o Notebook:** Faça o download do arquivo `AluraStoreBr.ipynb` (ou clone o repositório, se aplicável).
2.  **Prepare os Dados:** Certifique-se de ter os 4 arquivos CSV com os dados das lojas. O notebook original carrega os dados diretamente de URLs do GitHub[cite: 41]. Se estiver usando arquivos locais, ajuste os caminhos no código de importação (`pd.read_csv()`).
3.  **Ambiente:** Utilize o Google Colab. Faça o upload do notebook para o seu Google Drive.
4.  **Abra no Colab:** Clique com o botão direito no arquivo no Google Drive e selecione "Abrir com" -> "Google Colaboratory".
5.  **Execute o Código:** No menu do Colab, vá em "Ambiente de execução" e clique em "Executar tudo". Isso instalará as bibliotecas necessárias, importará os dados e realizará todas as análises e visualizações sequencialmente.
6.  **Resultados:** As tabelas de resumo, gráficos e o relatório final serão exibidos diretamente no notebook.

## Análise Final e Considerações

A análise comparativa das quatro lojas da Alura Store, utilizando as métricas definidas, aponta para a **Loja 4** como a unidade com o desempenho mais fraco.

**Pontos Chave:**

* **Faturamento:** A Loja 4 possui o menor faturamento total, representando apenas 23.6% do total da rede[cite: 66].
* **Categorias:** Embora venda as mesmas categorias populares que as outras, fatura menos com elas[cite: 68, 28].
* **Produtos:** O produto de maior faturamento da Loja 4 gera significativamente menos receita que os produtos de topo das outras lojas[cite: 73, 78].
* **Avaliação:** Sua avaliação média é ligeiramente inferior à das Lojas 2 e 3, embora superior à da Loja 1[cite: 70].
* **Frete:** Possui o frete médio mais baixo, o que é positivo, mas não compensa o baixo desempenho em receita[cite: 80].

**Considerações:**

* A Loja 1, apesar do maior faturamento[cite: 66], tem a pior avaliação média e o frete mais caro[cite: 70, 80], indicando possíveis problemas de satisfação do cliente ou logística que podem impactar a longo prazo.
* As Lojas 2 e 3 apresentam desempenho intermediário e muito similar em diversas métricas[cite: 66, 68, 28, 70].

**Recomendação:**

Com base na análise puramente quantitativa focada em identificar o menor desempenho atual para venda, a **Loja 4** é a candidata recomendada. Seu baixo faturamento em comparação com as demais a torna a opção mais lógica para desinvestimento visando levantar capital.

Recomenda-se, no entanto, que o Sr. João considere também fatores qualitativos ou estratégicos não abordados nesta análise (potencial de crescimento local, custos operacionais específicos, etc.) antes de tomar a decisão final.
