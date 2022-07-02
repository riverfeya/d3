# D3: Data-Driven Documents

<a href="https://d3js.org"><img src="https://d3js.org/logo.svg" align="left" hspace="10" vspace="6"></a>

**D3** (или **D3.js**) это JavaScript библиотека для визуализации данных использующая веб-стандарты. D3 помогает оживить данные с помощью SVG, Canvas и HTML. D3 сочетает в себе мощные методы визуализации и взаимодействия с управляемым данными подходом к манипулированию DOM, предоставляя вам все возможности современных браузеров и свободу разработки правильного визуального интерфейса для ваших данных.

## Resources

* [введение](https://observablehq.com/@d3/learn-d3)
* [API Reference](https://github.com/d3/d3/blob/main/API.md)
* [Релизы](https://github.com/d3/d3/releases)
* [Примеры](https://observablehq.com/@d3/gallery)
* [Wiki](https://github.com/d3/d3/wiki)

## Установка

Если вы используете npm, `npm install d3`. Вы также можете скачать [последний релиз на GitHub](https://github.com/d3/d3/releases/latest). Для ванильного HTML в современных браузерах, импортируйте D3 через Skypack:

```html
<script type="module">

import * as d3 from "https://cdn.skypack.dev/d3@7";

const div = d3.selectAll("div");

</script>
```

Для устаревших сред, вы можете скачать D3’s UMD сборку с npm-based CDN таких как jsDelivr; экспортирующих `d3` глобально:

```html
<script src="https://cdn.jsdelivr.net/npm/d3@7"></script>
<script>

const div = d3.selectAll("div");

</script>
```

Вы также можете использовать автономные микробиблиотеки D3. Например, [d3-selection](https://github.com/d3/d3-selection):

```html
<script type="module">

import {selectAll} from "https://cdn.skypack.dev/d3-selection@3";

const div = selectAll("div");

</script>
```

D3 написан с использованием [ES2015 модулей](http://www.2ality.com/2014/09/es6-modules-final.html). Создайте собственный пакет с помощью Rollup, Webpack или предпочитаемого вами сборщика. Чтобы импортировать D3 в приложение ES2015, либо импортируйте определенные символы из определенных модулей D3:

```js
import {scaleLinear} from "d3-scale";
```

Или импортировать все в пространство имен (here, `d3`):

```js
import * as d3 from "d3";
```

Или с помощью динамического импорта:

```js
const d3 = await import("d3");
```

You can also import individual modules and combine them into a `d3` object using [Object.assign](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/assign):

```js
const d3 = await Promise.all([
  import("d3-format"),
  import("d3-geo"),
  import("d3-geo-projection")
]).then(d3 => Object.assign({}, ...d3));
```
