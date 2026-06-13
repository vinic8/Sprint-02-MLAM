# Relatório Técnico: Análise Exploratória de Dados e Estatística Descritiva

[Vinicius Molena] — RM: [571270]
[Matheus Ferreira] — RM: [569638]
[Nathan Werner] — RM: [572925]
[Gabriel Vilas] — RM: [571603]
[Gustavo Henrique] — RM: [569921]
[Ricardo Santos] — RM: [569600]

## 1. Visão Geral do Projeto
Este relatório apresenta os resultados de uma Análise Exploratória de Dados (EDA) realizada na base de dados corporativa. O objetivo principal deste estudo é extrair padrões comportamentais e financeiros do quadro de funcionários, utilizando visualização de dados e estatística descritiva (análise univariada) através da linguagem Python. 

## 2. Metodologia Aplicada
A análise foi construída utilizando a linguagem **Python**, apoiada pelas bibliotecas `pandas` para manipulação dos dados, e `matplotlib` e `seaborn` para a construção das análises gráficas. O processo foi dividido em duas etapas:
1. **Análise Visual:** Geração de gráficos de setores, barras, histogramas e boxplots para visualização de distribuições e comparações de categorias.
2. **Análise Estatística (Univariada):** Cálculo de medidas de tendência central, dispersão e separatrizes para variáveis contínuas cruciais (Salário e Idade).

---

## 3. Principais Insights e Resultados (Atividades 01 e 02)

### 3.1. Análises Gráficas (Comportamento Visual)
* **Distribuição Departamental (Gráfico de Setores):** O gráfico evidenciou a proporção da força de trabalho alocada em cada departamento. Observar essas fatias permite entender onde está concentrado o maior custo operacional (Headcount).
* **Remuneração vs. Desempenho (Gráfico de Barras):** Ao cruzar a média salarial com as avaliações de desempenho, conseguimos visualizar se a política de meritocracia da empresa está sendo aplicada de forma eficaz na folha de pagamento.
* **Perfil Etário (Histograma):** A distribuição das idades dos funcionários demonstrou a concentração (pico do sino/curva) da faixa etária da empresa, revelando se a força de trabalho é majoritariamente júnior, plena ou sênior em tempo de vida.
* **Detecção de Anomalias Salariais (Boxplot):** O boxplot identificou claramente a mediana salarial, o intervalo onde a maioria dos salários está concentrada (caixa central) e permitiu a fácil identificação de *outliers* (pontos fora da curva superior ou inferior) na folha de pagamento.

### 3.2. Análise Estatística Univariada
Ao aplicarmos a estatística descritiva nas variáveis de Salário e Idade, destacam-se:
* **Tendência Central:** A média e a mediana próximas indicam uma distribuição relativamente simétrica (pouca distorção por salários de diretoria altíssimos). A moda revelou o valor salarial e a idade mais comuns na corporação.
* **Dispersão:** O cálculo do Desvio Padrão em relação à média de salários indicou a volatilidade da folha de pagamento. Uma alta amplitude confirmou a distância expressiva entre o menor e o maior salário/idade da empresa.
* **Separatrizes (Quartis):** A análise demonstrou os "degraus" financeiros e etários da base. O Q1 indicou que 25% da base recebe até `[Inserir Valor do Script]`, enquanto o Q3 revelou a margem que separa o seleto grupo dos 25% mais bem pagos.

---

## 4. Geração de Valor e Tomada de Decisão (Conclusão)

Os dados levantados neste estudo deixam de ser apenas números e se tornam inteligência de negócios. A partir dos insights extraídos, sugerem-se as seguintes tomadas de decisão para a empresa:

1. **Revisão da Política de Cargos e Salários:** O reconhecimento de *outliers* no Boxplot permite ao RH investigar se funcionários exercendo a mesma função possuem salários absurdamente distantes (risco passivo-trabalhista) ou justificados.
2. **Direcionamento de Treinamento e Cultura:** Compreender a distribuição de idade (Histograma) e o volume de pessoas em cada departamento (Gráfico de Setores) permite que o setor de Marketing Interno ajuste a comunicação e os benefícios para adequar-se à demografia real da companhia, aumentando a retenção de talentos.
3. **Validação da Meritocracia:** Se o Gráfico de Barras comprova que as melhores avaliações recebem, de fato, as maiores remunerações médias, o relatório fornece dados concretos para validar que as políticas de incentivo da empresa estão funcionando corretamente, gerando engajamento sustentável.
