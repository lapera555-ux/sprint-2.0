# Sompo Risk Intelligence Platform — Sprint 2

## Identificação

**Aluno:** Pedro Vinicius Gomes dos Santos  
**RM:** 571446  
**Turma:** 1TIAOB-2026  
**Challenge:** Sompo Seguros  
**Sprint:** 2  

---

## Objetivo

Desenvolver uma solução integrada para identificar fatores que aumentam a probabilidade de sinistros em operações agrícolas, conectando dados simulados de sensores e telemetria, banco SQL, modelos preditivos em Python, validação estatística, dashboard e alertas preventivos.

---

## Fluxo da Solução

```text
Sensores e Telemetria
        ↓
Dataset Simulado
        ↓
Ingestão Python
        ↓
Banco SQL
        ↓
Machine Learning
        ↓
Score de Risco
        ↓
Dashboard
        ↓
Alertas Preventivos
```

---

## Estrutura do Projeto

```text
data/
dashboard/
docs/
models/
prints/
python/
reports/
sql/

README.md
requirements.txt
01_instalar_dependencias.bat
02_testar_scripts_python.bat
03_abrir_dashboard_rapido.bat
04_verificar_banco_sql.bat
sompo_risk_max.db
```

---

## Banco de Dados SQL

O projeto utiliza banco SQL local para armazenar dados de telemetria e predições de risco.

Tabelas principais:

- `leituras_telemetria`
- `predicoes_risco`

### Criação das tabelas

![Criação das tabelas SQL](prints/01_create_tables_sql.png)

### Consultas SQL

![Consultas SQL](prints/02_consultas_sql.png)

---

## Execução do Projeto

### Execução dos scripts Python

![Execução dos scripts Python](prints/03_execucao_scripts_python.png)

### Dashboard em execução

![Dashboard em execução](prints/04_dashboard_execucao.png)

---

## Modelagem Preditiva

Foram avaliados cinco modelos supervisionados:

- Logistic Regression
- Decision Tree
- Random Forest
- KNN
- Gradient Boosting

As métricas utilizadas foram:

- Accuracy
- Precision
- Recall
- F1-Score
- Matriz de Confusão
- Correlação das variáveis

### Matriz de Confusão

![Matriz de Confusão](prints/05_matriz_confusao.png)

### Matriz de Correlação

![Matriz de Correlação](prints/06_matriz_correlacao.png)

### Importância das Variáveis

![Importância das Variáveis](prints/07_importancia_variaveis.png)

### Comparação dos Modelos

![Comparação dos Modelos](prints/08_comparacao_modelos.png)

---

## Dashboard Analítico

O dashboard possui visões por persona:

- Operador
- Gestor de Frota
- Analista Sompo
- Banco SQL

### Top Eventos Críticos

![Top Eventos Críticos](prints/09_dashboard_top_eventos.png)

### Score Médio por Região

![Score Médio por Região](prints/10_score_medio_regiao.png)

### Impacto Financeiro

![Impacto Financeiro](prints/11_impacto_financeiro.png)

### Sinistros por Região

![Sinistros por Região](prints/12_sinistros_regiao.png)

---

## Variáveis Monitoradas

O dataset contempla variáveis ambientais, geográficas, operacionais e de telemetria, como:

- umidade do solo;
- declividade;
- distância de corpos d'água;
- chuva nas últimas 24 horas;
- chuva acumulada em 7 dias;
- temperatura;
- visibilidade;
- nível de lama;
- RPM do motor;
- temperatura do motor;
- pressão dos pneus;
- vibração do motor;
- horas de operação;
- dias desde a última manutenção;
- falhas históricas.

---

## Score de Risco

| Score | Classe | Ação |
|---|---|---|
| 0–25 | Baixo | Monitoramento padrão |
| 26–50 | Médio | Atenção operacional |
| 51–75 | Alto | Operação com restrição |
| 76–100 | Crítico | Suspender ou reavaliar operação |

---

## Segurança e Governança

A solução considera:

- separação entre dados de telemetria e predições;
- histórico auditável no banco SQL;
- rastreabilidade por evento;
- validação de dados de entrada;
- visão por perfil: operador, gestor e analista Sompo.

---

## Como Executar

### Execução recomendada no Windows

Execute os arquivos abaixo nesta ordem:

```text
01_instalar_dependencias.bat
02_testar_scripts_python.bat
03_abrir_dashboard_rapido.bat
04_verificar_banco_sql.bat
```

### Execução manual

```bash
pip install -r requirements.txt
python python/ingestao_sql.py
python python/treinar_modelo.py
python python/score_risco.py
streamlit run dashboard/app.py
```

---

## Vídeo Demonstrativo

https://youtube.com/shorts/mzgnyyAf6jI?si=vXIoK7WXfBYdm4Wx

---

## Conclusão

A Sprint 2 apresenta uma solução funcional para prevenção de sinistros em equipamentos agrícolas segurados. O projeto integra dados simulados de sensores, banco SQL, modelos de Machine Learning, validação estatística e dashboard com alertas preventivos, apoiando a Sompo na transição de uma atuação reativa para uma atuação preventiva.
