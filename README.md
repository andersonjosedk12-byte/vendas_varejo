# 🛍️ Vendas no Varejo & Distribuição de Medidas (Data Visualization)

Este projeto reúne análises e visualizações com foco em **storytelling com dados** e boas práticas de **design de gráficos**. O notebook `vendas.ipynb` trabalha dois cenários distintos para exercitar **comparação** e **distribuição** de dados.

- **Cenário 1 (Varejo | 2016–2019):** análise de vendas e lucro de uma rede de lojas, com recortes por tempo, região, produto e logística.
- **Cenário 2 (Qualidade/Produção | 1000 amostras):** análise de distribuição, variabilidade e outliers em volumes e dimensões de produtos.

> Observação: as bases usadas no notebook são públicas e carregadas via URL.

## 🚀 Funcionalidades

- Comparação de **vendas anuais** com destaque do melhor período.
- Ranking de **produtos com maior lucro** (Top 7).
- Composição de vendas por **região** (colunas empilhadas).
- Comparação de **modo de envio** por perfil B2B/B2C (absoluto vs percentual).
- Séries temporais por **trimestre** (São Paulo e por região).
- Gráfico interativo (Plotly) com **customização de hover**.
- Distribuição de dados com **histograma**, **curva de densidade (KDE)** e **boxplot**.
- Exploração de padrões e inspeção de **regras de rejeição** para medidas (cenário de qualidade).

## 📈 Métricas / Perguntas respondidas (Cenário Varejo)

1. Qual o total de vendas por ano? Qual ano performou melhor?
2. Quais são os 7 produtos com maior lucro no período?
3. Como as vendas anuais se distribuem por região?
4. Qual modo de envio é mais utilizado? O padrão muda entre B2B e B2C?
5. Qual o total de vendas por trimestre no estado de São Paulo?
6. Qual o faturamento trimestral em cada região?

## 🧱 Pipeline do Notebook

### Seção 1 | Comparando dados (varejo)

1. **Carga e validação da base** – leitura do CSV de vendas e tipagem de datas.
2. **Vendas anuais** – gráfico de colunas com destaque do melhor ano.
3. **Lucro por produto** – ranking Top 7 com barras horizontais.
4. **Vendas por região** – colunas empilhadas para comparar total e composição.
5. **Logística (B2B vs B2C)** – barras empilhadas absoluto vs 100%.
6. **Sazonalidade** – vendas trimestrais em SP (linha com destaques).
7. **Tendência por região** – série temporal trimestral por região (Plotly).
8. **Refinos de interação** – personalização do texto informativo (hover).

### Aula 4 | Distribuindo dados (qualidade)

1. **Base 1 (Amaciante | 1000 amostras)** – leitura e estatística descritiva.
2. **Histograma** – distribuição do volume.
3. **Curva de densidade (KDE)** – visualização suave + linhas de média/mediana/moda.
4. **Boxplot** – quartis e identificação visual de outliers.

### Aula 5 | Explorando padrões (qualidade)

1. **Base 2 (Sabão em pó | 1000 amostras)** – dimensões (comprimento, altura, largura) por amostra.
2. **Violin plot** – distribuição por grupo/amostra.
3. **Regras de rejeição** – inspeção de itens fora de tolerância (10% acima/abaixo do alvo).

## 🛠️ Tecnologias Utilizadas

- Python 3.9+
- Pandas
- Matplotlib / Seaborn
- Plotly (interativo)
- Jupyter / Colab

## ▶️ Como Executar

1. **Instale dependências**:
   ```bash
   pip install pandas matplotlib seaborn plotly
   ```
2. **Abra o notebook**:
   ```bash
   jupyter notebook "vendas.ipynb"
   ```
3. **Execute as células em ordem** para reproduzir as análises e gráficos.

## 📁 Estrutura do Projeto

- `vendas.ipynb` – notebook com os dois cenários (varejo e qualidade).
- `README.md` – descrição e guia de execução.

> As bases são carregadas via URL dentro do notebook, portanto não precisam estar no repositório.

## 🔍 Principais Aprendizados

1. **Comparação vs composição**: colunas empilhadas ajudam a ver total e participação (ex.: regiões) no mesmo gráfico.
2. **Evitar conclusões por volume**: mostrar absoluto e percentual lado a lado (B2B vs B2C) reduz leituras erradas.
3. **Sazonalidade aparece com clareza** em séries temporais quando há marcações e anotações nos pontos-chave.
4. Para distribuição, **histograma/KDE/boxplot** se complementam: forma, tendência central e outliers.

## 📝 Licença

Projeto distribuído sob licença MIT.
