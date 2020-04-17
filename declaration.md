
## Декларация типа документа

**С чего начинается HTML-документ?**

Любой **HTML-документ**, обязан начинаться со строки дикларации **DOCTYPE** (от англ. **document type** — тип документа). Указание типа документа помогает браузеру определить, как правильно интерпритировать код полученной веб-страницы, поскольку **HTML** существует в нескольких версиях. Чтобы браузер _не путался_ и понимал, согласно какому стандарту необходимо отобразить веб-страницу, в самом начале **HTML-документа** нужно задать необходимый тип. В данном случае мы укажем тип наиболее актуальной версии **HTML** ее так же называют **HTML5**. Эта версия уже принята как стандарт и распространена почти везде, поэтому мы будем использовать именно ее.

```HTML
<!DOCTYPE html>
```

> Хотя слово DOCTYPE размещается в угловых скобках (< и >), оно не является тегом, это инструкция, предназначенная специально для браузеров, и восклицательный знак (!) в начале отличает ее от остального кода в HTML-документе.

**Что будет если не указывать дикларацию?**

Если не указывать дикларацию то браузер перейдет в **режим совместимости**. Этот режим предназначен для отображения веб-страницы подобно старым браузерам. В режиме совместимости игнорируются стандарты HTML и CSS, и поведение браузеров становится непредсказуемым. Для переключения в режим совместимости существует множество доктайпов, вот лишь некоторые из них.

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN">

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Frameset//EN">

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN">

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN">
```
_Подробнее про **режимы браузеров** и **дикларации** вы можете найти в интернете._ 