### Раздел заголовка

Раздел заголовка он же тег или _(элемент)_ `<head>`. Содержит в себе техническую информацию о странице, цель которой - помогать браузеру в работе с данными страницы. Содержимое тега _(элемента)_ `<head>` не отображается напрямую на веб-странице, за исключением тега _(элемента)_ `<title>`, он задаёт заголовок окна веб-страницы.

Внутри тега _(элемента)_ `<head>` допускается размещать следующие теги _(элементы)_: `<base>`, `<link>`, `<meta>`, `<script>`, `<style>`, `<title>`. 
 
 _Синтаксис:_
```html
<head>
  ...
</head>
```
 
 _Пример реализации:_
```html
<!DOCTYPE html>
<html>
  <head>
   ...
  </head>
  <body>
    ...
  </body>
</html>
```
 
### Раздел контента

Раздел контента он же тег _(элемент)_ `<body>`. Предназначен для хранения содержимого веб-страницы, это видимая часть документа и она отображается в окне браузера. Любую информацию которую следует выводить в документе, следует распологать именно внутри тега _(элемента)_ `<body>`.

_Синтаксис:_
```html
<body>
  ...
</body>
```

_Пример реализации:_
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Lorem ipsum dolor sit.</title>
  </head>
  <body>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum ultrices enim in felis
      ultrices, quis placerat est conguePraesent nec felis metus. Sed nec fermentum mauris, 
      nec venenatis neque. Etiam id ornare massa. Nulla pharetra eget tellus at mattis.
      Praesent a egestas purus, a aliquet libero. Nunc pharetra vulputate elementum. Vestibulum at tempor
      urna, rutrum suscipit mi. Aenean in scelerisque est.
    </p>
  </body>
</html>
```

> **Примечание:** К элементам располагаемым внутри тега _(элемента)_ `<body>` можно отнести текст, изображания, формы, таблицы скрипты и многое другое.
