# Análise de Desempenho - Alura Store

## 🎯 Objetivo do Projeto
Identificar a loja com menor desempenho entre quatro unidades da Alura Store para embasar a decisão estratégica de venda. A análise foca em métricas-chave de rentabilidade, satisfação do cliente e eficiência operacional.

---

## 📊 Métricas Analisadas
1. Faturamento total por loja
2. Desempenho por categoria de produtos
3. Satisfação do cliente (avaliações)
4. Produtos mais/menos rentáveis
5. Custos logísticos (frete)

---

```
AluraStoreBr/
├── dados/                  # Arquivos de entrada (hipotéticos)
│   ├── loja_1.csv         # Dados históricos de vendas
│   ├── loja_2.csv         # (período 2020-2022)
│   ├── loja_3.csv
│   └── loja_4.csv
└── AluraStoreBr.ipynb     # Análise completa no Google Colab
```


---

## 🔍 Principais Resultados

### 1. Faturamento Total (2020-2022)
| Loja   | Faturamento (R$)   | Participação |
|--------|--------------------|--------------|
| Loja 1 | 1.534.509,12       | 26.1%        |
| Loja 2 | 1.488.459,06       | 25.4%        |
| Loja 3 | 1.464.025,03       | 24.9%        |
| **Loja 4** | **1.384.497,58** | **23.6%**    |

**Insight**: Loja 4 gera 12% menos que a líder (Loja 1).

![Participação por Loja](![image](https://github.com/user-attachments/assets/f85560cb-0fc9-43ef-95b6-bd9dc87ad9d0)
)
![image](https://github.com/user-attachments/assets/7f25f61f-c5e1-4680-9805-bcda89a0ee5c)

---

### 2. Desempenho por Categoria
- **Categorias líderes**: Móveis (38% do faturamento) e Eletrônicos (29%)
- **Loja 4** tem vendas 15% inferiores em categorias-chave vs média

![Vendas por Categoria](![image](https://github.com/user-attachments/assets/6d3e124e-f3f1-485e-9407-9d45cbe468a4)

)

---

### 3. Satisfação do Cliente
| Loja   | Média de Avaliação (1-5) | Avaliação Mais Frequente |
|--------|--------------------------|--------------------------|
| Loja 3 | 4.05                     | 5                        |
| Loja 2 | 4.04                     | 5                        |
| Loja 4 | 4.00                     | 5                        |
| Loja 1 | 3.98                     | 5                        |

**Insight**: Todas mantêm boa satisfação, mas Loja 4 está abaixo da média.
![image](https://github.com/user-attachments/assets/ca588e30-dcb6-44b4-aeb9-8e9a368f2dea)

---

### 4. Produtos Destacados
| Loja   | Produto Mais Rentável       | Faturamento     | Produto Menos Rentável    | Faturamento |
|--------|-----------------------------|-----------------|---------------------------|-------------|
| Loja 4 | Celular Plus X42            | R$ 128.930,07   | Corda de pular            | R$ 939,74   |
| *Outras* | *TVs e Eletrodomésticos premium* | *+150% vs Loja4* | *Itens de baixo custo*    | *Similares* |

![image](https://github.com/user-attachments/assets/7b267fed-fb76-4f11-9425-7400248c0d0f)

---

### 5. Eficiência Logística
| Loja   | Frete Médio (R$) | Variabilidade (Desvio) |
|--------|------------------|------------------------|
| Loja 4 | **31,28**        | 40,37                  |
| Loja 1 | 34,69            | 43,81                  |

**Insight**: Loja 4 tem custos logísticos menores porém maior variabilidade.
![image](https://github.com/user-attachments/assets/1e09d2b4-ca50-4862-97e5-38e476c014ec)

---

## 🚀 Recomendação Estratégica

**Loja Recomendada para Venda: Loja 4**

**Fatores Decisivos**:
1. 🔻 Menor faturamento geral (-12% vs líder)
2. 🔻 Desempenho inferior em categorias estratégicas
3. 🔻 Produto carro-chefe menos rentável
4. 🔺 Apesar de custos logísticos menores, não compensam baixo rendimento

**Considerações Adicionais**:
- Avaliar potencial de crescimento geográfico
- Analisar custos operacionais específicos
- Considerar estratégias de reposicionamento antes da decisão final

---

## ▶️ Como Reproduzir a Análise
1. **Abrir Notebook**: [AluraStoreBr.ipynb no Colab]([https://colab.research.google.com/drive/16hDDXhw1F-p3lswyn6oou-Ay4TDnAim](https://github.com/alviarezali/Alura_lojas/blob/main/AluraStoreBr.ipynb))
2. **Executar Tudo**: 
   ```python
   Runtime > Executar tudo (Ctrl+F9)
Requisitos:

Conexão com internet

Navegador moderno

Conta Google (para salvar resultados)

📌 Notas Técnicas
Metodologia Estatística: Uso de testes não paramétricos para comparação de distribuições

Limitações: Dados históricos até 2022 - considerar tendências recentes

Reprodutibilidade: 100% de código documentado e versionado

Elaborado por Daniel Alviarez - Especialista em Ciência de Dados

## 📌 Análise Final Conclusiva

### Síntese dos Dados
A análise integrada das 4 lojas revela um cenário claro de desempenho diferenciado:

| Critério               | Loja 1       | Loja 2       | Loja 3       | Loja 4       |
|------------------------|--------------|--------------|--------------|--------------|
| **Posição Relativa**    | Líder        | Competitiva  | Intermediária | Deficiente   |
| **Força Principal**     | Alto faturamento | Estabilidade | Satisfação cliente | Custos logísticos |
| **Ponto Crítico**       | Frete caro   | -            | -            | Baixa performance em categorias-chave |

### Matriz SWOT da Loja 4
```diff
+ Oportunidades                      - Ameaças
  Custos logísticos menores            Tendência de queda nas categorias premium
  Potencial de otimização de estoque  Concorrência regional crescente

+ Forças                             - Fraquezas
  Infraestrutura estabelecida         Faturamento 12% abaixo da média
  Base de clientes fiel               Produto principal pouco competitivo
