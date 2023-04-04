# Маршрут путешествия в поэме И. П. Мятлева «Сенсации и замечания госпожи Курдюковой за границею, дан л'этранже»

## Обзор данных

Датасет представляет геоданные о маршруте персонажа поэмы И. П. Мятлева «Сенсации и замечания госпожи Курдюковой за границею, дан л'этранже» (1840). Сюжетная мотивировка позволяет автору развернуть перед читателем картину современной Европы, данную глазами русского путешественника. Госпожа Курдюкова прибывает на север Германии на пароходе и затем осматривает города нескольких европейских стран. Датасет воспроизводит ее маршрут, фиксируя населенные пункты, в которые заезжает путешественница, и наиболее вероятные пути перемещения между ними. В ряде случаев эти пути воспроизводятся гипотетически на основе современных транспортных путей. Перемещения персонажа внутри городов при осмотре достопримечательностей в данных не отражены.

## Формат данных

Данные представлены в формате geojson. Помимо необходимых для формата сведений о типе геометрического объекта (главным образом, это точки) и координатах, для большинства объектов в данные включены также дополнительные поля: `init` и `fin`, в которых помещаются строки, с которых начинается и которыми заканчивается соответствующий объекту эпизод.

Например, 

```

    {
      "type": "Feature",
      "properties": {
        "marker-color": "#7e7e7e",
        "marker-size": "medium",
        "marker-symbol": "city",
        "title": "Мюнстер",
        "init": "В Мюнстере мне показали,",
        "fin": "Что в ней тридевять земель.",
        "seg": 17
      },
      "geometry": {
        "type": "Point",
        "coordinates": [
          7.631134,
          51.963737
        ]
      }
    },
    
```

В этом фрагменте данных отражен эпизод посещения персонажем города Мюнстер. Координаты Мюнстера даны в поле `coordinates` (7.631134, 51.963737), а поле `init` содержит первую строку соотвествующего эпизода:

```
В Мюнстере мне показали, 
Что послы употребляли, 
Заключая славный мир, ―
Экритуары, тирелир, 
Деньги клал куда виновный, 
По интриге кто любовной, 
Иль затем, что долго спал, 
К заседанью опоздал. 

...

В кирке Мюнстера есть тоже
Редкости, но не похоже: 
Там железные висят
Клетки три, и говорят, 
Что в них сжарены гуситы, 
Тех времен, знать, езуиты, 
Аферисты, энтриган, 
Сплетники, де мове жан. 

```

Весь этот эпизод соответствует точке Мюнстера на карте. Упомянутая в стихотворном фрагменте церковь (кирка) Мюнстера отдельной точки в наших данных не имеет.

## Источник данных

Текст воспроизводится по изданию *Мятлев И. П.* Стихотворения. Сенсации и замечания госпожи Курдюковой. Л.: Советский писатель, 1969.
