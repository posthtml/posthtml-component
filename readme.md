# Component PostHTML Plugin <img align="right" width="220" height="200" title="PostHTML logo" src="http://posthtml.github.io/posthtml/logo.svg">

[![NPM][npm]][npm-url]
[![Deps][deps]][deps-url]
[![Build][build]][build-badge]
[![Coverage][cover]][cover-badge]
[![Standard Code Style][style]][style-url]
[![Chat][chat]][chat-badge]

Before:
``` html
<!--my-button.html-->
<my-button tag="a" class="big-button">
    <content></content>
</my-button>

<!--navigation.html -->
<navigation>
  ...
</navigation>

<!--index.html -->
<import src="my-button.html" tag="my-button">
<import src="navigation.html" tag="navigation" as="nav">

<header>
    <nav class="header__nav"></nav>
    <my-button href="#" class="header__btn">Click</my-button>
</header>
```

After:
``` html
<header>
    <div class="navigation header__nav">
        ...
    </div>
    <a href="#" class="my-button big-button header__btn">Click</a>
</header>
```

## Install

> npm i posthtml-component

## Usage

``` js
const fs = require('fs');
const posthtml = require('posthtml');
const posthtmlcomponent = require('posthtml-component');

posthtml()
    .use(posthtmlcomponent({ /* options */ }))
    .process(html/*, options */)
    .then(result => fs.writeFileSync('./after.html', result.html));
```

### Contributing

See [contribution guide](CONTRIBUTING.md).

### License [MIT](LICENSE)

[npm]: https://img.shields.io/npm/v/posthtml-component.svg
[npm-url]: https://npmjs.com/package/posthtml-component

[deps]: https://david-dm.org/scrum/posthtml-component.svg
[deps-url]: https://david-dm.org/scrum/posthtml-component

[style]: https://img.shields.io/badge/code%20style-standard-yellow.svg
[style-url]: http://standardjs.com/

[build]: https://travis-ci.org/scrum/posthtml-component.svg?branch=master
[build-badge]: https://travis-ci.org/scrum/posthtml-component?branch=master

[cover]: https://coveralls.io/repos/scrum/posthtml-component/badge.svg?branch=master
[cover-badge]: https://coveralls.io/r/scrum/posthtml-component?branch=master


[chat]: https://badges.gitter.im/posthtml/posthtml.svg
[chat-badge]: https://gitter.im/posthtml/posthtml?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge"
