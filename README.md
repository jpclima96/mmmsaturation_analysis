# MMM Saturation Analysis

## Visão Geral

Este repositório contém ferramentas e código para análise de saturação em Modelos de Marketing Mix (MMM). Ele foi projetado para ajudar profissionais de marketing e cientistas de dados a entender os efeitos de saturação em diferentes canais de mídia e investimentos de marketing.

## Principais Funcionalidades

- Avaliação de efeitos de saturação em diferentes canais de mídia
- Implementação de funções de transformação (Hill-Adstock, Adstock) para MMM
- Visualizações interativas dos efeitos de saturação 
- Funções para simulação e otimização de investimentos em marketing
- Análise ROI (Retorno sobre Investimento) por canal

## Tecnologias

- Python 3.8+
- NumPy/Pandas para manipulação de dados
- Matplotlib/Seaborn/Plotly para visualizações
- Scipy para modelagem estatística

## Começando

### Pré-requisitos

- Python 3.8 ou superior
- Pip (gerenciador de pacotes Python)

### Instalação

1. Clone o repositório:
```bash
git clone https://github.com/jpclima96/mmmsaturation_analysis.git
cd mmmsaturation_analysis
```

2. Crie e ative um ambiente virtual (opcional, mas recomendado):
```bash
python -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate
```

3. Instale as dependências:
```bash
pip install -r requirements.txt
```

## Como Usar

### Funções de Saturação

O projeto implementa diferentes modelos de saturação, incluindo:

- Modelo Hill-Adstock
- Adstock tradicional
- Funções de decaimento personalizáveis

Exemplo de uso:

```python
from src.saturation import apply_hill_adstock

# Aplicar transformação Hill-Adstock em dados de mídia
transformed_data = apply_hill_adstock(
    data=media_data,
    alpha=0.7,  # Parâmetro de decaimento
    gamma=0.5,  # Parâmetro de saturação
    theta=0.8   # Parâmetro de escala
)
```

### Visualizações

Para gerar visualizações de efeitos de saturação:

```python
from src.visualization import plot_saturation_curve

# Visualizar curva de saturação
plot_saturation_curve(
    spends=[1000, 2000, 3000, 4000, 5000],
    channel_name="TV",
    alpha=0.7,
    gamma=0.5
)
```

### Análise de ROI

```python
from src.roi_analysis import calculate_roi_by_channel

# Calcular ROI por canal
roi_results = calculate_roi_by_channel(
    model_results=mmm_results,
    spend_data=media_spend
)



