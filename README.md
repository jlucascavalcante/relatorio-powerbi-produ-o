# ⚙️ Engenharia de Produção — Prevendo a Produção Industrial com IA — Power BI

Dashboard de análise e previsão de produção industrial com foco em desempenho por faixa etária de funcionários e tendência temporal — combinando análise histórica (2018–2023) com projeção via forecast nativo do Power BI até 2028.

---

## 🎯 Problema de negócio

Gestores de produção industrial precisam não apenas monitorar o desempenho passado, mas antecipar tendências para planejar capacidade, alocação de turnos e gestão de força de trabalho. Este dashboard combina análise histórica com previsão automatizada para responder: qual faixa etária de funcionários é mais produtiva? A produção está em trajetória de crescimento ou queda? E onde ela estará nos próximos anos se a tendência atual se mantiver?

---

## 🔍 Principais insights

- **Média geral de 360,64 mil unidades produzidas**, com pico histórico de 1,01 Mi registrado em 2020 — o ano de maior produção do período analisado.
- **Funcionários de 25 a 34 anos lideram a produção total** (~70 Mi de unidades), seguidos pela faixa de 45 a 54 anos — sugerindo que tanto o grupo mais jovem-produtivo quanto o de maior experiência são os pilares da operação.
- **Funcionários de 16 a 19 anos têm o menor volume total**, o que é esperado dado o perfil de entrada no mercado de trabalho, mas levanta a questão sobre o papel desse grupo na operação.
- **Pico de produção em 2020 (437 Mil de média)** seguido de queda consistente até 2022 (237 Mil) — queda de ~46% em dois anos, padrão que merece atenção na análise de causas operacionais.
- **Previsão indica continuidade da queda até 2028** (projeção de ~209 Mil), com intervalo de confiança crescente — sinal de alerta para planejamento de capacidade produtiva a médio prazo.
- O gráfico de área por faixa etária revela que **todas as faixas seguem a mesma trajetória de queda a partir de 2020**, indicando que o declínio é sistêmico, não concentrado em um perfil específico de funcionário.

---

## 📄 Estrutura do dashboard

O relatório é composto por uma única página com os seguintes visuais:

| Visual | Descrição |
|---|---|
| **KPI — Média de Unidades Produzidas** | Média geral do período completo |
| **KPI — Pico de Unidades Produzidas** | Valor máximo registrado, configurado como agregação de máximo (2020) |
| **Total de Unidades Produzidas por Faixa de Idade** | Barras horizontais ordenadas por volume total por faixa etária |
| **Média de Unidades Produzidas por Ano** | Série temporal com previsão nativa (forecast) do Power BI até 2028 |
| **Total de Unidades Produzidas por Ano e Faixa de Idade** | Gráfico de área empilhada com séries por faixa etária (2018–2023) |

**Filtros disponíveis:** Turno e Idade dos Funcionários (por faixa etária).

---

## 🛠️ Stack técnica

- **Ferramenta:** Power BI Desktop
- **Transformação de dados (Power Query):** ajuste de tipos de dado, promoção de cabeçalhos e configuração da fonte
- **Visualizações:** gráfico de linha com previsão nativa (forecast automático do Power BI), gráfico de área empilhada por segmento, barras horizontais e cartões KPI com agregação de máximo
- **Sem medidas DAX** — todas as agregações utilizam as funções nativas do Power BI, incluindo a configuração de máximo no cartão de pico

---

## 📊 Fonte dos dados

Dataset de produção industrial com cobertura de 2018 a 2023, originalmente utilizado em curso de formação em dados. O dashboard, os visuais, a formatação e a estrutura analítica foram desenvolvidos de forma independente — incluindo a escolha dos gráficos, configuração do forecast, paleta, layout e cruzamentos exibidos.

---

## 🔗 Acesse o relatório

[Acesse o dashboard](https://app.powerbi.com/view?r=eyJrIjoiYzQ4MjkyYTktNjY0NS00NTc3LTkyNTEtYWU1YTJlNGViOTA0IiwidCI6ImIyZTE2Mjk3LTJlZDYtNDFiOC1iODIyLWE5NTRlOTViZDJmMCIsImMiOjR9)

---

## 📌 Limitações e próximos passos

- A **previsão é baseada exclusivamente na tendência histórica** do próprio Power BI — não incorpora variáveis externas como contratações planejadas, sazonalidade operacional ou mudanças de turno. O intervalo de confiança crescente a partir de 2024 reflete essa incerteza.
- Os totais por faixa etária refletem **volume acumulado**, não produtividade média por funcionário — uma faixa etária com mais funcionários naturalmente terá maior total. Normalizar por número de funcionários por faixa seria o próximo passo para comparação justa.
- O dashboard ainda não responde **por que a produção caiu após 2020** — cruzar com dados de absenteísmo, turnover ou capacidade instalada tornaria a análise acionável para gestores de operação.
