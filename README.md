# Классификация зданий по архитектурным стилям с использованием сверточной нейронной сети (CNN)

## Датасет

В работе бал использован датасет [architectural-styles-dataset](https://www.kaggle.com/datasets/dumitrux/architectural-styles-dataset/data?select=architectural-styles-dataset), собранный из изображений,  взятых с Google Images, и набора данных из статьи "*Architectural Style Classification using Multinomial Latent Logistic Regression (ECCV2014)*". Всего датасет содержит 10113 изображений зданий в формате '*.jpg*', каждое из которых относится к одному из 25 класоов, характеризующих различные архитектурный стили.

![Пример изображения](/plots_for_report/Augmentation4.png)

*Рисунок 1. Пример изображения*

## Модели

В работе были расмотрены 2 арихитектуры предобученых сверточных нейронных сетей: Residual neural network (ResNet), EfficientNet-B0

*Таблица 1. Результат валидации моделей:*

| №  |      model      | parameters | test loss |  train loss | test accuracy | train accuracy | precision | recall | f1-score |
|----|-----------------|------------|-----------|-------------|---------------|----------------|-----------|--------|----------|
| 1  |     ResNet      |  20213273  |  0.2224   |    0.0951   |    0.6678     |    0.7842      |   0.68    |  0.67  |   0.67   |
| 2  | EfficientNet-B0 |   3825461  |  0.2110   |    0.0978   |    0.6209     |    0.7658      |   0.65    |  0.62  |   0.61   |

Лучший результат F1-score: 0.6664. [google.colab](https://colab.research.google.com/drive/1jQ8l0TXhCvSlo6gkKL9u91oHW0kL91sz?usp=sharing)
