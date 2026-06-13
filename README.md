# Relatório Técnico: Análise Estratégica da Rede de Estações de Recarga de VE

**Integrantes:**
* [Vinicius Molena] — RM: [571270]
* [Matheus Ferreira] — RM: [569638]
* [Nathan Werner] — RM: [572925]
* [Gabriel Vilas] — RM: [571603]
* [Gustavo Henrique] — RM: [569921]
* [Ricardo Santos] — RM: [569600]

## 1. Introdução e Contexto do Projeto
Este relatório apresenta uma análise quantitativa e visual da infraestrutura de estações de recarga para Veículos Elétricos (VE). Utilizando técnicas de ciência de dados em ambiente Python, a análise explora o comportamento operacional das estações, padrões de precificação (tarifação) e a capacidade técnica instalada. O objetivo final é transformar dados brutos em decisões de negócios acionáveis para expansão e otimização da rede.

## 2. Metodologia de Análise
A metodologia aplicada dividiu-se em duas frentes fundamentais:
1. **Análise Visual Avançada:** Implementação de gráficos setoriais, histogramas, diagramas de barras e diagramas de caixa (Boxplots) via `matplotlib` e `seaborn`.
2. **Estatística Descritiva Univariada:** Extração matemática exata de tendências centrais (Média, Mediana e Moda), comportamento de dispersão (Variância, Desvio Padrão e Amplitude) e limites de distribuição por meio de medidas separatrizes (Quartiz) para as principais métricas volumétricas e financeiras.

---

## 3. Principais Insights Obtidos

### 3.1. Análise Visual e Gráfica (Item 01)
* **Estrutura de Portes (Gráfico de Setores):** Revela a distribuição volumétrica da rede (Pequenas, Médias e Grandes estações). O predomínio de estações de pequeno porte aponta para uma infraestrutura capilarizada (foco em conveniência local), enquanto as macroestações concentram centros de alta velocidade de recarga.
* **Performance por Canal (Gráfico de Barras):** O cruzamento do *Tipo de Local* com a *Média de Sessões Mensais* comprova que locais voltados ao Comércio/Varejo e Rodovias (Redes de Recarga Dedicadas) possuem uma taxa de utilização significativamente maior se comparados a concessionárias ou prédios públicos.
* **Gargalo Técnico (Histograma):** A análise de frequências da potência máxima (kW) indica o perfil tecnológico dominante da rede. Um pico em faixas menores expõe a forte presença de carregadores mais lentos (Level 2), delimitando a oportunidade de mercado para investimentos futuros em carregamento ultrarrápido (DC Fast).
* **Anomalias de Preço (Boxplot):** O diagrama de caixa aplicado à tarifa média (por kWh) revela a estabilidade e a amplitude da estratégia de precificação. A identificação visual de *outliers* na parte superior indica locais onde há alta demanda geográfica e baixa concorrência, permitindo a prática de tarifas premium.

### 3.2. Análise Descritiva Univariada (Item 02)

#### Métrica A: Sessões Mensais (Demanda e Volume)
* **Tendência Central:** A disparidade observada entre a Média e a Mediana sinaliza uma distribuição fortemente assimétrica à direita. Poucas estações de alta performance (pontos em rodovias ou hubs comerciais) elevam artificialmente a média geral, evidenciando o efeito "80/20" no uso da rede.
* **Dispersão:** Uma alta variância e desvio padrão confirmam que o comportamento da demanda é volátil. A expressiva amplitude mostra que existem estações ociosas que precisam de intervenções de marketing ou realocação de infraestrutura.
* **Separatrizes:** O Terceiro Quartil (Q3) atua como um limiar de alta performance. As estações que operam acima dessa linha delimitam os padrões ideais de localização que devem ser replicados no plano de expansão.

#### Métrica B: Tarifa Média por kWh (Visão Financeira)
* **Tendência Central:** A média e a mediana próximas validam um preço de mercado consolidado e estável para a recarga base, funcionando como o ponto de equilíbrio para o planejamento do Retorno sobre o Investimento (ROI).
* **Dispersão:** O desvio padrão controlado exprime um mercado maduro e competitivo, onde desvios drásticos da média ocorrem apenas em condições exclusivas (ex: exclusividade regional ou velocidade extrema do carregador).

---

## 4. Recomendações Estratégicas para Tomada de Decisão (Geração de Valor)

Com base nas evidências geradas pelo modelo matemático e visual, as seguintes decisões corporativas devem ser priorizadas para maximizar a geração de receita da empresa:

1. **Investimento Focado em Alta Rotação:** Direcionar os aportes de expansão de capital (CapEx) estritamente para o modelo vencedor identificado no gráfico de barras: **Comércio/Varejo e Hubs Comerciais de Conveniência**, onde o giro de clientes (sessões mensais) garante um pay-back acelerado da infraestrutura.
2. **Upgrade Tecnológico Direcionado:** Migrar estações classificadas no Q1 (25% piores em sessões) de carregadores lentos para rápidos (DC Fast), se a potência de infraestrutura local permitir. A velocidade atrai o cliente corporativo e frotas comerciais que pagam tarifas maiores pelo fator tempo.
3. **Estratégia Dinâmica de Preço (Dynamic Pricing):** Utilizar os limites das medidas separatrizes e os *outliers* mapeados no Boxplot para implementar preços flexíveis. Estações localizadas em locais com alto tráfego e baixa concorrência podem aplicar margens de lucro superiores às do terceiro quartil, enquanto locais de baixa utilização podem oferecer descontos em horários alternativos para aumentar a ocupação base.
