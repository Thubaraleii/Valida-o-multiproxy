# Validação Multiproxy – MOD1 (LSL)

Este repositório contém o notebook **MOD1 (LSL)**, utilizado para visualização gráfica dos dados geoquímicos (por exemplo, razões isotópicas como U/Th) ao longo de subníveis (profundidade). O objetivo é facilitar a análise multiproxy de perfis geológicos, aplicando gráficos de linha que relacionam teores com profundidade.

---

## 📊 Funcionalidades

- Geração de gráficos de linha com:
  - **Eixo X = Subnível (profundidade)**
  - **Eixo Y = Teores (ex: U/Th)**
- Categorização por fontes ou classes de dados (coluna "Fonte")
- Inversão do eixo de profundidade para visualização geológica tradicional
- Suporte a múltiplos proxies geoquímicos

---

## 🧠 Imputação de Dados com Deep Learning

O projeto também utiliza redes neurais para **preencher automaticamente valores ausentes** nas colunas de dados geoquímicos, como teores de elementos ou razões isotópicas.

O modelo é treinado com os dados disponíveis para **aprender padrões multivariados** e prever os valores faltantes com base nas variáveis correlacionadas (por exemplo, profundidade, espessura, razão U/Th, etc.).

### 🔍 Etapas do processo:
1. **Pré-processamento** dos dados com tratamento de valores ausentes, normalização e codificação de categorias.
2. **Treinamento de um modelo neural** (rede densa totalmente conectada) para prever as variáveis faltantes.
3. **Validação cruzada** e comparação dos valores estimados com observações reais (se disponíveis).
4. **Preenchimento dos dados ausentes** no conjunto final, que é então usado nos gráficos e análises subsequentes.

Essa abordagem garante maior consistência e qualidade nos perfis multiproxy, principalmente em registros geológicos incompletos.

---

## 🛠️ Tecnologias Utilizadas

- Python 3.x
- Pandas
- Matplotlib
- Seaborn
- TensorFlow / Keras
- Jupyter Notebook

---

## 🚀 Como Usar

1. Clone o repositório:

   ```bash
   git clone https://github.com/Thubaraleii/Valida-o-multiproxy.git

2. Acesse o notebook:
   /Valida-o-multiproxy/MOD1 (LSL).ipynb
   
4. Estrutura do Projeto
Valida-o-multiproxy/
├── MOD1 (LSL).ipynb       # Gráfico de linha: profundidade vs teores
├── README.md              # Este arquivo
└── ...                    # Outros notebooks ou scripts
