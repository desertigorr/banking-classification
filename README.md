## Классификация запросов в техподдержку ХЗ-Банка

### Датасет / Dataset :
[``Kaggle Datasets Link``](https://www.kaggle.com/datasets/desertigor/banking-requests)

Датасет представляет собой набор обращений в техподдержку воображаемого банка и состоит из коротких сообщений от пользователей в стиле, приближенном к реальному (свободный стиль текста, частичное отсутствие знаков препинания, жаргон)

*Синтезирован при помощи GPT-5 Thinking*

Датасет распространяется по лицензии ``CC0 1.0 Universal``, права принадлежат общественности, так что любой желающий может использовать этот датасет для своих учебных/практических целей.

The dataset is a set of requests to the technical support of an imaginary bank and consists of short messages from users in a style close to real (free text style, partial absence of punctuation marks, jargon)

*Synthesized using GPT-5 Thinking*

The dataset is distributed under the ``CC0 1.0 Universal`` license, the rights belong to the public, so anyone can use this dataset for their educational/practical purposes.

#### Формат / Format:

``ID:TEXT:LABEL``

#### Содержит 1000 запросов разного рода / Includes 1000 requests of various kinds

**Классы / Classes:**
- ``PAYMENT_OUT_FAIL``   
- ``INCOMING_DELAY``   
- ``APP_LOGIN``         
- ``CARD_ISSUE``        
- ``ACCOUNT_SEIZED``
- ``FRAUD_SUSPECTED``    
- ``KYC_VERIFICATION``  
- ``APP_TECH``

### Задачи:

- проанализировать содержимое датасета
- обучить модель классифицировать обращения по их типу
- сохранить эксперимент вместе с моделью, метриками и графиками при помощи ``MLflow``

### Использовал:

- ``TF-IDF vectorizer``
- ``RandomForestClassifier``
- ``MLflow``
- ``Jupyter Notebook``
- ``GPT-5 Thinking`` для синтеза искусственных данных

### Итоги:

```Accuracy: 0.935
                  precision    recall  f1-score   support

  ACCOUNT_SEIZED       1.00      0.96      0.98        28
       APP_LOGIN       0.88      0.91      0.89        23
        APP_TECH       1.00      1.00      1.00        18
      CARD_ISSUE       0.94      1.00      0.97        32
 FRAUD_SUSPECTED       0.96      0.88      0.92        25
  INCOMING_DELAY       0.89      0.89      0.89        28
KYC_VERIFICATION       0.96      0.90      0.93        29
PAYMENT_OUT_FAIL       0.84      0.94      0.89        17
        accuracy                           0.94       200
       macro avg       0.93      0.94      0.93       200
    weighted avg       0.94      0.94      0.94       200
```
