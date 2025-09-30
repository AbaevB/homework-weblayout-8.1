# homework-weblayout-8.1

Домашняя работа 1 к модулю 8 Веб-верстка

## Feature header

### Оптимизация контейнера

Огромные горизонтальные паддинги в 224px  для контейнера нецелесообразны. Логичней уменьшить максимальную ширину блока, оставив паддинг 20px для всех разрешений:

```css
.container {
  width: 100%;
  max-width: 1320px;
  margin: 0 auto;
  padding: 0 20px;
}

```

И для контейнера внутри хедера и футера:

```css
.header .container {
  max-width: 1668px;
}

.footer .container {
  max-width: 1668px;
}
```

## Pixel Perfect для хедера

- На разрешении 767px уменьшен правый марджин для блока *header__menu*

- На разрешении 1023px увеличен нижний паддинг для всего блока *header*


## Feature hero

### Разрешение 1728px

- Изменение нижнего отступа для *hero__heading*
- Изменение паддинга для *hero__link*

## Feature advantages

- Стили для видео
- Изменение структуры заголовков

## Feature governing

### Для десктопного разрешения

- Добавление в разметку адаптивных изображений
- Увеличение на 2px нижнего марджина для заголовка секции *Governing*

### Для планшетного разрешения

- Изменение размеров шрифта и нижнего марджина для заголовка секции *governing*

## Feature outro

Изменение свойства `background` на `background-image` для секции *outro*

```scss
.outro {
  background-image: url("../images/vacancy-bg.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  padding: 108px 0;
  position: relative;



  @media (min-resolution: 2dppx) {
    background-image: url("../images/vacancy-bg@2x.jpg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }

  @include vp-1023  {
    padding: 55px 0;
    background-image: url("../images/vacancy-bg-tablet.jpg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    @media (min-resolution: 2dppx)  {
      background-image: url("../images/vacancy-bg-tablet@2x.jpg");
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
    }
  }
}

```

## Feature footer

Приведение блока в соответствие с макетом PP на всех разрешениях