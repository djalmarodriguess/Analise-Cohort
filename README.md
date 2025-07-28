# Projeto de Análise Cohort 
<img width="1920" height="384" alt="Análise de Cohort" src="https://github.com/user-attachments/assets/8a21f553-cde1-445b-bc61-eb576e0747ae" />


Este projeto tem como objetivo realizar uma análise de cohort aplicada a dados de faturamento e recorrência de clientes de uma empresa de telefonia. Utilizando um dataset fictício, porém com estrutura e valores realistas, a análise foca na segmentação por métodos de pagamento, identificando padrões de retenção e receita ao longo do tempo.

A análise visa responder perguntas cruciais para o negócio, como:
- Quais métodos de pagamento garantem maior fidelização?
- Qual canal gera maior receita média ao longo do meses?
- Quais cohorts (meses de entrada) apresentam os maiores índices de churn?

Além disso, foi desenvolvido um **dashboard interativo no Tableau** que permite a visualização dinâmica dos dados, facilitando a tomada de decisões estratégicas por parte das áreas de negócio, marketing e operações.

🔗 [Acesse o dashboard interativo no Tableau Public](https://public.tableau.com/views/AnlisedeCohort_Telefonia/Painel1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

## 🟡 SITUAÇÃO
Para viabilizar o estudo, foi desenvolvido um dataset fictício com valores reais de faturamento e transações, permitindo simular cenários autênticos e garantir a 
confiabilidade da análise.Empresas de serviços recorrentes, como operadoras de telefonia, enfrentam duas lacunas críticas:

1. **Visão fragmentada do cliente**: os relatórios mensais tradicionais escondem quedas de retenção e não mostram se os clientes de cada canal realmente permanecem ativos.  
2. **Incerteza sobre métodos de pagamento**: sem dados claros, não se sabe quais canais (Pix, Cartão, Boleto...) trazem maior fidelidade e geram fluxo de caixa mais estável.

Sem esses insights, decisões de marketing e produto são baseadas em médias que podem camuflar riscos e oportunidades.

---

## 🧩 TAREFA
Desenvolver uma **Plataforma Analítica de Cohort** que:

- **Segmenta clientes pelo mês de entrada** e método de pagamento.  
- **Monitora** mês a mês a **retenção** e o **faturamento** de cada cohort.  
- **Expõe** padrões de comportamento que orientam melhorias em aquisição, retenção e gestão de fluxo de caixa.  
- **Disponibiliza** um dashboard interativo em **Tableau** para que gestores visualizem facilmente os resultados.

---

## ⚙️ AÇÃO
1. **Preparação dos Dados**  
   - Seleção das colunas necessárias para a análise (via queries SQL) e limpeza dos dados no CSV de pagamentos.  
   - Cálculo de `cohort_month` (mês da 1ª fatura) e `period_number` (meses desde a entrada) desenvolvido campos calculados no próprio Tableau.  
   - Filtragem por método de pagamento.

2. **Cálculo das Métricas de Cohort**  
   - **Retenção mensal**: % de clientes ativos em cada período.  
   - **Receita acumulada** por cohort.  
   - **Comparação** entre Pix, Cartão, Boleto e outros Métodos de pagamentos.

3. **Construção do Dashboard**  
   - Heatmap de retenção para evolução da mensal da receita.  
   - Implementação do painel no **Tableau** para acesso e compartilhamento com os interessados.

4. **Validação e Refinamento**  
   - Apresentação dos primeiros achados para stakeholders.  
   - Ajustes de visualização e filtros conforme feedback.

---

## 📊 DASHBOARD INTERATIVO
Para facilitar a tomada de decisão, foi criado um **dashboard interativo** no Tableau, que consolida:

- **Seletores de Filtro Dinâmico**: escolha de método de pagamento (Pix, Cartão, Boleto ou Todos) e seleção de múltiplos meses para análise temporal.  
- **KPI Cards**: indicadores de **Total de Clientes**, **Receita Total** dos meses selecionados e **Retenção Média %** para visão imediata do desempenho global ou segmentado.  
- **Abas de Métricas**: navegação entre **Retenção**, **Churn** e **Receita R$**, permitindo foco em diferentes indicadores.  
- **Heatmap de Retenção** dos cohorts por método de pagamento, exibindo a evolução mês a mês ao longo de 12 ou mais períodos.  
- **Matriz Cohort Completa**: tabela detalhada com número de clientes e porcentagens de retenção de cada cohort.  
- **Análise de Churn**: visualização específica para entender o abandono de clientes ao longo do tempo.  

📌 Link de compartilhamento: [Acesse o dashboard no Tableau Public](https://public.tableau.com/views/AnlisedeCohort_Telefonia/Painel1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

---

## ✅ RESULTADO
# Insights Acionáveis a partir da Análise de Cohort

1. **Melhor canal de retenção: “Lotérica”**  
   - Retém mais de **30%** dos clientes no 1º mês, superando todos os demais métodos nos últimos 12 meses.  
   - **Ação**: priorizar incentivos (descontos ou campanhas de comunicação) para quem ainda não migrou para o pagamento eletrônico.

2. **Método Correspond. com maior churn inicial**  
   - Apresenta mais **70%** de churn no 1º mês — a taxa mais alta do portfólio.  
   - **Ação**: reavaliar a experiência de pagamento via Correspond. (por exemplo: simplificar o fluxo ou rever política de tarifas).

3. **Pix gera maior receita média por cliente**  
   - Cada grupo de clientes “iniciados” no Pix traz, em média mensalmente, **R\$530** de faturamento ao longo da cohort.  
   - **Ação**: reforçar campanhas de migração para Pix (por e‑mail, SMS ou bônus) para elevar o ticket médio.

4. **Cohort de junho/2025: faturamento estável, baixa retenção**  
   - Apesar receita mensal estável (R\$ 3.040), sua retenção no 1º mês foi apenas **70,2%** (a menor) levando em consideração todos os métodos.  
   - **Ação**: implementar um programa de “boas‑vindas” com engajamento extra nos primeiros 30 dias (ex: tutorial in‑app, atendimento dedicado).

6. **“Guichê” e “Lotérica” com alta retenção prolongada**  
   - Ambos mantêm cerca de **34–36%** de retenção média geral.  
   - **Ação**: estudar práticas desses canais para replicar incentivos (recorrência automática, lembretes de pagamento) nas demais modalidades.

7. **Identificar “meses críticos” de coorte**  
   - As cohorts de **maio/2025** (60,9% no 2º mês) e **maio/2024** apresentaram quedas acima da média.  
   - **Ação**: analisar campanhas e comunicação desses períodos para entender falhas de onboarding e ajustar cronogramas futuros.

---

## 🏁 CONCLUSÃO
Este projeto, da **concepção do dataset fictício** à **implementação do dashboard Tableau**, demonstrou como a **Análise de Cohort** fornece um motor de insights estratégicos:

- **Pix**: Migrar clientes para este método reduz custos de transação, acelera a liquidação e aumenta a receita média por mês (R$ 530), melhorando a rentabilidade e o fluxo de caixa.  
- **Lotérica & Guichê**: Canais de destaque em retenção (34–36% em média), cujas práticas de recorrência e lembretes devem ser adotadas em outros métodos.  
- **Correspondente**: Identificamos 70% de churn no 1º mês, indicando a necessidade urgente de simplificar a jornada de pagamento.  
- **Meses Críticos (maio/2025 e junho/2025)**: Quedas atípicas de retenção revelam falhas de onboarding; recomendam-se campanhas de engajamento e comunicação focadas nas primeiras semanas.  
- **Break‑even no 4º mês**: Este marco orienta o planejamento de CAC, alinhando investimentos de aquisição ao retorno financeiro esperado.

Com o **dashboard interativo**, gestores têm acesso em tempo real a heatmaps, KPIs e filtros dinâmicos, transformando dados em decisões ágeis. A Análise de Cohort, assim, deixa de ser um relatório estático e se torna um **instrumento de execução contínua**, impulsionando a retenção e maximizando o valor de cada cliente em cada etapa da jornada.  
