 📊 Superstore — Dashboard de Análise de Vendas e Investigação de Prejuízos

 🎯 Sobre o projeto

Este projeto apresenta um dashboard de Business Intelligence construído no 
**Google Data Studio (Looker Studio)**, utilizando o dataset público **Superstore** 
(9.994 registros de vendas de varejo). O relatório é dividido em duas páginas, 
cada uma com um objetivo diferente:

- **Página 1 — Visão Geral de Vendas:** KPIs principais e desempenho por região 
  e categoria de produto
- **Página 2 — Investigação de Prejuízos:** análise investigativa para responder 
  à pergunta *"Por que estamos perdendo dinheiro em certos pedidos?"*

 🔗 Acesse o dashboard

👉 [Clique aqui para abrir o relatório interativo](https://datastudio.google.com/reporting/9fd404a2-7880-4369-8339-5ffddaa4163f)

*O relatório abre na Página 1. Use as setas de navegação (lado esquerdo) para 
acessar a Página 2 — Investigação de Prejuízos.*

 🛠️ Ferramentas utilizadas

- **Google Data Studio (Looker Studio)** — construção do dashboard
- **Python (Pandas)** — exploração de dados e validação de hipóteses
- **Google Colab** — ambiente de desenvolvimento da análise

---

 📄 Página 1 — Visão Geral de Vendas

Dashboard executivo com os principais indicadores do negócio:

- **KPIs:** Total de Vendas, Total de Lucro, Ticket Médio, Quantidade de Pedidos
- **Vendas por Região:** comparação de desempenho entre West, East, Central e South
- **Lucro por Categoria:** Furniture, Office Supplies e Technology
- **Série temporal de vendas:** evolução das vendas ao longo do período analisado
- **Filtro interativo de Região:** permite explorar os dados por região específica

![Visão Geral de Vendas - Parte 1](screenshots/pagina1-visao-geral-parte1.png)
![Visão Geral de Vendas - Parte 2](screenshots/pagina1-visao-geral-parte2.png)

---

 🔍 Página 2 — Investigação de Prejuízos

 Pergunta de negócio
*"Por que estamos perdendo dinheiro em certos pedidos?"*

 Metodologia
1. Identifiquei que **18,72%** dos pedidos (1.871 de 9.994) resultam em prejuízo
2. Segreguei o prejuízo por Categoria e Sub-Categoria, isolando os "vilões": 
   **Tables**, Bookcases e Supplies
3. Testei a hipótese de que o desconto excessivo seria a causa raiz
4. Validei a correlação entre Discount e Profit especificamente em Tables

 Principais descobertas

- **Tables** concentra o maior prejuízo entre todas as sub-categorias 
  (-R$ 17.725,48)
- O desconto médio em Tables é de **26,1%** — quase o dobro da média geral 
  do catálogo (15,6%)
- Existe uma correlação negativa forte (**-0,67**) entre desconto e lucro 
  em Tables
- A partir de **21% de desconto**, cada venda de Tables já passa a dar 
  prejuízo

| Faixa de Desconto | Profit Médio |
|---|---|
| 0% | R$ 184,39 |
| 1-20% | -R$ 4,28 |
| 21-40% | -R$ 151,86 |
| 41%+ | -R$ 236,35 |

 ✅ Recomendação de negócio

Limitar o desconto máximo aplicado em Tables a 15-20% recuperaria a 
lucratividade da sub-categoria sem comprometer significativamente o 
volume de vendas.

![Investigação de Prejuízos - Parte 1](screenshots/pagina2-investigacao-parte1.png)
![Investigação de Prejuízos - Parte 2](screenshots/pagina2-investigacao-parte2.png)

---

## 📁 Arquivos neste repositório

- `notebook-analise-prejuizo.ipynb` — código Python com toda a análise 
  exploratória e validação das hipóteses
- `screenshots/` — capturas de tela das duas páginas do dashboard

 👤 Autor: Moacir Nascimento
[LinkedIn](https://www.linkedin.com/in/moacir-nascimento2003) | [GitHub](https://github.com/moacirnascimento439)




**Moacir Nascimento**
[LinkedIn](SEU_LINK_LINKEDIN) | [GitHub](https://github.com/moacirnascimento439)
