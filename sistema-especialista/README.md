# Orientador de Distribuições de Probabilidade

Sistema especialista com aprendizado supervisionado. Atividade da Aula 13 de Inteligência Artificial e LFA (UDF).

## O que faz
Recebe uma frase que descreve uma situação do dia a dia e recomenda qual distribuição discreta usar: Poisson, Geométrica, Pascal, Hipergeométrica, Bernoulli ou Binomial.

## Como funciona
- Modelo (aprende com dados): CountVectorizer + DecisionTreeClassifier, treinado com 30 frases simuladas. Prevê o tipo da situação: contagem em intervalo, repete até uma meta ou n fixo.
- Sistema especialista (regras humanas): 6 regras SE-ENTÃO que usam o tipo previsto e três fatos informados na consulta (sem reposição, n = 1, r = 1).
- A previsão do modelo vira um fato usado pelas regras.

## Arquivos
- distribuicoes_sistema_especialista.ipynb: notebook (rodar no Google Colab ou Jupyter, de cima para baixo)
- datasetdistribuicoes.csv: dataset simulado (30 frases, 10 por classe)
- requirements.txt: bibliotecas necessárias

## Resultados
Acurácia de 87,5% em 8 frases de teste. O teste é muito pequeno e os dados são simulados, então esse número não demonstra eficácia real.

## Limitações
- O modelo aprende palavras, não significado: frases com vocabulário novo podem ser classificadas errado, e as regras repetem esse erro com aparência de confiança.
- As frases foram escritas por uma só autoria e não representam como pessoas reais descrevem problemas.
- O sistema não verifica as premissas das distribuições, como independência e probabilidade constante.

Dados simulados exclusivamente para aprendizagem.
