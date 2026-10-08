# Industrial Failure Analysis

Análise de falhas de equipamentos industriais com Python, regras semânticas e Machine Learning para auditoria, classificação e tratamento de dados.

## Visão geral

Este projeto apresenta um fluxo de análise e saneamento de dados de falhas de equipamentos industriais. A solução combina auditoria de qualidade, regras semânticas de alta confiança e Machine Learning para apoiar a revisão das classificações de modo e impacto de falha.

O foco do projeto é demonstrar uma abordagem auditável, conservadora e reproduzível para tratamento de dados técnicos.

## Principais resultados

- 10.000 registros analisados
- 6.412 registros sinalizados como incorretos ou tratados
- 882 registros envolvidos em duplicidades lógicas
- 441 pares de duplicidade identificados
- 192 ocorrências com problemas de data
- 10.000 IDs únicos preservados
- 0 valores ausentes na saída final

## Metodologia

O fluxo foi dividido em quatro etapas principais:

1. Auditoria inicial de qualidade dos dados
2. Aplicação de regras semânticas de alta confiança
3. Classificação por TF-IDF + Regressão Logística como fallback
4. Consolidação, validação e geração dos resultados finais

### Auditoria de dados

Foram avaliados:

- valores ausentes;
- datas inválidas;
- duplicidades lógicas;
- consistência dos domínios;
- descrições ambíguas;
- divergências entre descrições e classificações originais.

### Regras semânticas

Descrições com evidência textual clara foram classificadas por regras determinísticas para reduzir decisões automáticas sem fundamento.

### Machine Learning

Para casos não resolvidos diretamente pelas regras, foi utilizado um pipeline com:

- `TfidfVectorizer`
- `LogisticRegression`

O modelo atua como fallback, utilizando exemplos considerados internamente consistentes.

## Estrutura do repositório

```text
industrial-failure-analysis/
├── notebooks/
│   └── Brava_Analise_Final.ipynb
├── reports/
│   └── Relatorio_Executivo.pdf
├── dashboard/
│   └── Visualizacao_Resultados.html
├── README.md
├── requirements.txt
└── .gitignore
```

## Tecnologias utilizadas

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook
- HTML/CSS
- Git/GitHub

## Limitações

Não foi fornecido um conjunto completo de verdade-terreno validado por especialista para todas as ocorrências.

Por isso, a solução deve ser interpretada como um processo de saneamento analítico e apoio à revisão, e não como substituição de uma validação especializada de engenharia de manutenção.

## Privacidade dos dados

A base original e a planilha final de respostas não são disponibilizadas neste repositório. O objetivo é preservar os dados utilizados na análise.

## Autor

André Douglas Cruz  
AI Engineer | Machine Learning Engineer
