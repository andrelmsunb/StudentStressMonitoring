# MVP - Student Stress Monitoring

**Universidade de Brasília (UnB)**  
**Instituto de Ciencias Matematicas e de Computação - (USP)**  
**Professor:** Dr. Andre Luiz Marques Serrano  


## 📋 Resumo Executivo

Este projeto desenvolveu um **Produto Mínimo Viável (MVP)** de Machine Learning para classificação de tipos de estresse em estudantes universitários. O modelo final alcançou uma **acurácia de 88.64%** no conjunto de teste, demonstrando excelente capacidade de generalização.

## 🎯 Objetivos Alcançados

✅ **Análise exploratória completa** do dataset Student Stress Monitoring  
✅ **Preparação robusta dos dados** com engenharia de features  
✅ **Treinamento e comparação** de 7 algoritmos diferentes  
✅ **Otimização de hiperparâmetros** para os melhores modelos  
✅ **Criação de modelo ensemble** para melhor performance  
✅ **Avaliação rigorosa** no conjunto de teste  
✅ **Notebook completo** seguindo todos os requisitos da prova

## 📊 Principais Resultados

### Dataset
- **1100 instâncias** de estudantes universitários (18-21 anos)
- **47 features** após engenharia de atributos
- **3 classes balanceadas**: No Stress, Distress, Eustress
- **5 categorias científicas**: Psicológica, Fisiológica, Ambiental, Acadêmica, Social

### Melhor Modelo: Regressão Logística
- **Acurácia:** 88.64%
- **Precisão:** 88.86%
- **Recall:** 88.64%
- **F1-Score:** 88.57%
- **AUC-ROC médio:** 97.65%

### Features Mais Importantes
1. **blood_pressure** (Pressão arterial)
2. **social_support** (Suporte social)
3. **academic_performance_high** (Alta performance acadêmica)
4. **teacher_student_relationship_high** (Bom relacionamento professor-aluno)
5. **living_conditions_high** (Boas condições de vida)

## 📁 Estrutura do Projeto

```
student_stress_mvp/
├── data/                          # Dados processados
│   ├── StressLevelDataset.csv     # Dataset original
│   ├── train_data_scaled.csv      # Dados de treino normalizados
│   ├── val_data_scaled.csv        # Dados de validação
│   └── test_data_scaled.csv       # Dados de teste
├── models/                        # Modelos treinados
│   ├── best_individual_model.pkl  # Melhor modelo individual
│   ├── ensemble_model.pkl         # Modelo ensemble
│   └── standard_scaler.pkl        # Scaler para normalização
├── notebooks/                     # Scripts e notebook
│   ├── MVP_Student_Stress_Monitoring.ipynb  # Notebook principal
│   ├── data_exploration.py        # Exploração de dados
│   ├── data_preparation.py        # Preparação dos dados
│   ├── modeling.py                # Modelagem e treinamento
│   └── model_evaluation.py        # Avaliação final
├── results/                       # Visualizações e relatórios
│   ├── final_report.md           # Relatório final detalhado
│   ├── model_comparison.png       # Comparação dos modelos
│   ├── confusion_matrix_*.png     # Matrizes de confusão
│   └── roc_curves_*.png          # Curvas ROC
└── docs/                         # Documentação
    ├── dataset_info.md           # Informações do dataset
    ├── exploratory_findings.md   # Achados da exploração
    └── requisitos_mvp.md         # Requisitos da prova
```

## 🚀 Como Executar

### 1. Ambiente
```bash
pip install pandas numpy scikit-learn matplotlib seaborn plotly kagglehub
```

### 2. Download dos Dados
```python
import kagglehub
path = kagglehub.dataset_download("mdsultanulislamovi/student-stress-monitoring-datasets")
```

### 3. Execução Completa
```bash
# Exploração de dados
python3 notebooks/data_exploration.py

# Preparação dos dados
python3 notebooks/data_preparation.py

# Modelagem
python3 notebooks/modeling.py

# Avaliação final
python3 notebooks/model_evaluation.py
```

### 4. Notebook Jupyter
Abra o arquivo `notebooks/MVP_Student_Stress_Monitoring.ipynb` no Google Colab ou Jupyter.

## 📈 Insights Principais

### Fatores de Maior Impacto no Estresse
1. **Fatores Fisiológicos:** Pressão arterial se mostrou o preditor mais forte
2. **Fatores Sociais:** Suporte social é crucial para o bem-estar
3. **Fatores Acadêmicos:** Performance e relacionamento com professores são determinantes
4. **Fatores Psicológicos:** Autoestima e ansiedade têm alta correlação com estresse

### Padrões Identificados
- **Estudantes sem estresse:** Maior suporte social e melhor qualidade do sono
- **Estudantes com distresse:** Maiores níveis de ansiedade e problemas de saúde
- **Estudantes com eustresse:** Boa performance acadêmica com preocupações controladas

## 🎓 Conformidade com Requisitos da Prova

### ✅ Checklist Completo
- [x] **Definição clara do problema** e objetivos
- [x] **Descrição detalhada do dataset** e suas características
- [x] **Preparação robusta dos dados** com divisão adequada
- [x] **Engenharia de features** para melhorar performance
- [x] **Múltiplos algoritmos testados** com justificativas
- [x] **Otimização de hiperparâmetros** documentada
- [x] **Validação cruzada** para robustez
- [x] **Avaliação no conjunto de teste** com métricas apropriadas
- [x] **Análise de overfitting** e generalização
- [x] **Comparação entre modelos** com visualizações
- [x] **Interpretabilidade** através de importância das features
- [x] **Notebook público** estruturado como relatório

## 🔬 Metodologia Científica

### Rigor Estatístico
- **Seed fixo (42)** para reprodutibilidade
- **Divisão estratificada** mantendo proporção das classes
- **Validação cruzada 5-fold** para robustez
- **Conjunto de teste isolado** para avaliação imparcial

### Boas Práticas de ML
- **Pipeline reproduzível** com scripts modulares
- **Normalização adequada** (StandardScaler)
- **Prevenção de data leakage** com fit apenas no treino
- **Múltiplas métricas** para avaliação completa
- **Análise de erros** por classe

## 📝 Próximos Passos

1. **Deploy em Produção:** Criar API REST para o modelo
2. **Monitoramento Contínuo:** Acompanhar performance com novos dados
3. **Interpretabilidade Avançada:** Implementar SHAP para explicações individuais
4. **Expansão do Dataset:** Incluir mais universidades e contextos
5. **Intervenções Personalizadas:** Desenvolver recomendações específicas

## 👥 Contribuições

Este projeto demonstra a aplicação prática de técnicas de Machine Learning em problemas reais de saúde mental estudantil.

## 📄 Licença

Este projeto é desenvolvido para fins acadêmicos. O dataset utilizado está sob licença Apache 2.0.

---

**Desenvolvido com 💙 para a saúde mental estudantil**

