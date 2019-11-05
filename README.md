# Подготовка к хакатону

## Ардуино

Скачиваем программу Ардуино для работы с микроконтроллерами - [скачать](https://www.arduino.cc/download_handler.php).
Устанавливаем программу (не меняем параметры при установке).

[Датчик влажности DHT11](https://arduinomaster.ru/datchiki-arduino/datchiki-temperatury-i-vlazhnosti-dht11-dht22/)

[ИК-датчик обнаружения препятствий](http://coolcode.ru/arduino-infrakrasnyiy-datchik-obnaruzheniya-prepyatstviy-mh-series/)

[Ультразвуковой дальнометр](https://robotclass.ru/tutorials/arduino-sonic-hc-sr04/)

[Сервопривод](http://edurobots.ru/2014/04/arduino-servoprivod/)

[Датчик температуры](https://arduinomaster.ru/datchiki-arduino/arduino-ds18b20/)

## Подготовка среды для работы с нейронными сетями

1. Устанавливаваем Anaconda с флешки.
2. Открываем Anaconda prompt -> `conda install python=3.6` (при установке нас спросят подверждаем ли мы сие действие, вводим `y` и нажимаем Enter.
3. В этом же окне прописываем `conda create --name PythonCPU`, затем `conda activate PythonCPU`.
4. Далее `conda install -c anaconda keras`
5. `conda install -c anaconda pandas`
6. `conda install -c anaconda matplotlib`

### Код для проверки наличия всех библиотек

```
import numpy as np # Для быстрых математических вычислений и работы с матрицами
# import matplotlib.pyplot as plt # Для создания графиков
import pandas as pd # Объединение, преобразование и абстрагирование данных
import tensorflow # Импорт tensorflow
import keras # Импорт keras
from keras.utils import to_categorical
from keras import models
from keras import layers

aNP = np.array([
    [1, 2, 3, 4],
    [5, 6, 7, 8]
])
print(aNP)

my_series = pd.Series([5, 6, 7, 8, 9, 10])
print(my_series)
```

## Полезные ссылки 

### Нейронные сети

[Нейронные сети для начинающих. Часть 1](https://habr.com/ru/post/312450/)

[Как работает нейронная сеть: алгоритмы, обучение, функции активации и потери](https://neurohive.io/ru/osnovy-data-science/osnovy-nejronnyh-setej-algoritmy-obuchenie-funkcii-aktivacii-i-poteri/)

[Пример с созданием нейронной сети на питоне (Keras, Pandas, NumPy)](https://www.kaggle.com/arihant0497/try-shallow-before-going-deep)

[TenserFlow - однослойный персептрон](https://andreyex.ru/tensorflow-mashinnoe-obuchenie/tensorflow-odnoslojnyj-perseptron/)

[Применение нейронных сетей с ПИД-регуляторами](https://cyberleninka.ru/article/v/primenenie-neyrosetevyh-regulyatorov-v-sistemah-upravleniya-elektroprivodami)

[Андрей Созыкин. Нейронные сети, учебные курсы](https://www.asozykin.ru/)

### Python и все, что с ним связано

[Введение в pandas](https://khashtamov.com/ru/pandas-introduction/)

[Подготовка среды (Anaconda, NumPy, Pandas, Matplotlib, Keras](https://towardsdatascience.com/installing-keras-tensorflow-using-anaconda-for-machine-learning-44ab28ff39cb)
