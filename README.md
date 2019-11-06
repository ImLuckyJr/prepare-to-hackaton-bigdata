# Большие данные и машинное обучение (БДиМО). 

Здесь размещены различные ссылки для самоподготовки и помощи в использовании, порядок установки необходимых инструметов для работы с нейронными сетями и решение возможных проблем.

## Знакомство с ардуино, полезные ссылки

Скачиваем программу Ардуино для работы с микроконтроллерами - [скачать](https://www.arduino.cc/download_handler.php).
Устанавливаем программу (не меняем параметры при установке).

> В ссылках ниже по датчикам присутствуют примеры кода для работы с датчиками. В примерах могут подключаться различные библиотеки. Для их подключения и установки смотрите пункт ***Подключение сторонних библиотек для датчиков Arduino***.

[Датчик влажности DHT11](https://arduinomaster.ru/datchiki-arduino/datchiki-temperatury-i-vlazhnosti-dht11-dht22/)

[ИК-датчик обнаружения препятствий](http://coolcode.ru/arduino-infrakrasnyiy-datchik-obnaruzheniya-prepyatstviy-mh-series/)

[Ультразвуковой дальнометр](https://robotclass.ru/tutorials/arduino-sonic-hc-sr04/)

[Сервопривод](http://edurobots.ru/2014/04/arduino-servoprivod/)

[Датчик температуры DS18B20](https://arduinomaster.ru/datchiki-arduino/arduino-ds18b20/)

### Подключение сторонних библиотек для датчиков Arduino

Для работы с вышеперечисленными датчиками может потребоваться установка дополнительных библиотек. Для этого необходимо в ***Arduino*** перейти во вкладку *Скетч* -> *Подключить библиотеку* -> *Управление библиотеками*. В данном окне можно искать необходимые библиотеки и устанавливать их.

- Датчик влажности DHT11 (Библиотека **DHT Sensor library**. Может быть так, что при компиляции кода будет возникать ошибка, связанная с данной библиотекой и библиотекой **Adafruit**. Тогда необходимо найти библиотеку **Adafruit Unified Sensor by Adafruit** и установить);
- Датчик температуры DS18B20 (Библиотека **OneWire**).

## Подготовка среды для работы с нейронными сетями

1. Устанавливаваем Anaconda с флешки.
2. Открываем консоль ***Anaconda prompt*** -> `conda install python=3.6` (при установке нас спросят подверждаем ли мы сие действие, вводим `y` и нажимаем Enter.
3. В этом же окне прописываем `conda create --name PythonCPU`, затем `conda activate PythonCPU`.
4. Далее `conda install -c anaconda keras`.
5. `conda install -c anaconda pandas`.
6. `conda install -c anaconda matplotlib`.
7. Открываем Anaconda.
8. Переходим во вкладку **Environment** (слева). Выбираем **PuthonCPU**. 
9. Затем возвращаемся на вкладку **Home**. Находим **Jupyter Notebook**. Если не установлено, устанавливаем и после нажимаем **Launch**. После должен открыться браузер с новой вкладкой и адресом `localhost:8888`.
> *Если браузер не открылся автоматически на нужной вкладке, перейдите ниже к пункту **Открытие Jupyter Notebook вручную**.*

> *Для проверки всех библиотек необходимо воспользоваться кодом, расположенным ниже.*

### Открытие Jupyter Notebook вручную

Для того чтобы вручную открыть Jupyter нам необходимо в адресной строке браузера ввести `localhost:8888`. На открывшейся странице вам необходимо ввести пароль или токен доступа. Вам необходимо получить токен следующим образом:
1. Открыть консоль ***Anaconda Prompt***.
2. Выполнить команду `jupyter notebook list` (будут выведены строки вида `http://localhost:8888/?token=c724fccbdb62a8006c9abb40a508dc0bda037b01fb910aaa :: C:\Путь`).
3. Необходимо скопировать строку после `/?token=` и до конца, затем скопированное значение вставить в окне браузера, где запрашивался токен, нажать **ВВОД** и пользоваться.

### Код для проверки наличия всех библиотек
> *Если код выполняется без каких-либо ошибок, на экран выводятся заданные значения, то это значит, что все необходимые библиотеки установлены. Этот код необходим только для проверки наличия всех нужных библиотек.*
```
import numpy as np # Для быстрых математических вычислений и работы с матрицами
import matplotlib.pyplot as plt # Для создания графиков
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

[Библиотеки для глубокого обучения: Keras](https://habr.com/ru/company/ods/blog/325432/)

[Cоздание нейросети c Keras](https://neurohive.io/ru/tutorial/nejronnaya-set-keras-python/)

### Python и все, что с ним связано

[NumPy, часть 1: начало работы](https://pythonworld.ru/numpy/1.html)

[NumPy, часть 2: базовые операции над массивами](https://pythonworld.ru/numpy/2.html)

[Задание по NumPy](http://www.machinelearning.ru/wiki/images/5/58/MMP_Practicum_317_2015_1.pdf)

[Задания по NumPy (все на англ.)](https://www.w3resource.com/python-exercises/numpy/index.php)

[Подготовка среды (Anaconda, NumPy, Pandas, Matplotlib, Keras)](https://towardsdatascience.com/installing-keras-tensorflow-using-anaconda-for-machine-learning-44ab28ff39cb)

[Введение в pandas](https://khashtamov.com/ru/pandas-introduction/)

[Руководство по использованию pandas для анализа больших наборов данных](https://habr.com/ru/company/ruvds/blog/442516/)

[Изучаем pandas. Урок 1. Введение в pandas и его установка (Есть несколько уроков, которые могут быть полезными)](https://devpractice.ru/pandas-series-and-dataframe-part2/)

[10 трюков библиотеки Python Pandas, которые вам нужны](https://proglib.io/p/pandas-tricks/)
