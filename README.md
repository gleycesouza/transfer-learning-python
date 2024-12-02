# Treinamento de Redes Neurais com Transfer Learning

Este projeto consiste no treinamento de redes neurais utilizando Transfer Learning, baseado no modelo **VGG16**. Ele foi desenvolvido como parte da formação **BairesDev - Machine Learning Practitioner**, oferecida pela **DIO**.

---

## Objetivo

Demonstrar o uso de Transfer Learning em um problema de classificação de imagens, aplicando ajustes em um modelo pré-treinado para adequá-lo ao conjunto de dados utilizado.

---

## Etapas do Projeto

1. **Preparação dos Dados**  
   - Utilização do dataset *Cats vs Dogs* fornecido pelo TensorFlow Datasets (TFDS).  
   - Preprocessamento das imagens:
     - Redimensionamento para 64x64 pixels.
     - Normalização dos valores dos pixels.
     - Conversão de rótulos para formato *one-hot*.

2. **Divisão do Dataset**  
   - Separação dos dados em conjuntos de treino, validação e teste (70%, 15%, 15% respectivamente).  
   - Organização em lotes para otimização do treinamento.

3. **Modelo Utilizado**  
   - Base: **VGG16** pré-treinada no ImageNet.  
   - Ajustes:
     - Camada de saída personalizada para número de classes do dataset.
     - Camadas convolucionais congeladas para preservar os pesos pré-treinados.
     - Treinamento focado na nova camada de classificação.

4. **Treinamento do Modelo**  
   - Configuração:
     - Função de perda: *categorical_crossentropy*.  
     - Otimizador: Adam.  
     - Métrica: acurácia.
   - Treinamento em 10 épocas com *batch size* de 128.  
   - Avaliação em dados de validação.

5. **Avaliação e Resultados**  
   - Análise das métricas de desempenho (perda e acurácia) em gráficos para entender o comportamento do modelo ao longo das épocas.

---

## Tecnologias e Ferramentas

- **Linguagem**: Python  
- **Bibliotecas**:  
  - TensorFlow  
  - NumPy  
  - Matplotlib  
- **Dataset**: TensorFlow Datasets (*Cats vs Dogs*)

---

