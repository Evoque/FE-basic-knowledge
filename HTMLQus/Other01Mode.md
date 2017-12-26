

## Quirks Mode and Standards Mode


- When the web standards were made at W3C, browsers could not just start using them, as doing so would break most existing sites on the web. 
    + 当W3C开始制作web标准，浏览器不能直接采用它们，因为如果直接采用会让现存的大部分站点崩溃。
    + 网站翻译: 当W3C创立网络标准后，为了不破坏当时既有的网站，浏览器不能直接采用这些标准。

- Browsers therefore introduced two modes to treat new standards compliant sites differently from old legacy sites.
    + 因此，浏览器厂商引入了两种模式来处理与旧逻辑站点差别很大的新web标准兼容性站点。
    + 网站翻译: 因此，浏览器采用了两种模式，用以把能符合新规范的网站和老旧网站区分开。

- There are now **three** modes used by the `layout engines` in web browsers: `quirks mode`, `almost standards mode`, and `full standards mode`.
    + `quirks mode`: layout emulates nonstandard behavior in Navigator 4 and IE 5. This is essential in order to support websites that were built before the widespread adoption of web standards.
    + `full standards mode`: the behavior is (hopefully) the behavior described by the HTML and CSS specifications.
    + `almost standards mode`: there are only a very small number of quirks implemented.


## How do browsers determine which mode to use?

For HTML documents, browsers use a DOCTYPE in the beginning of the document to decide whether to handle it in quirks mode or standards mode.

- full standards mode, has a `DOCTYPE` like this: 
``` HTML
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset=UTF-8>
            <title>Hello World!</title>
        </head>
        <body>
        </body>
    </html>
```
`<!DOCTYPE html>`, is the simplest possible, and the one recommended by HTML5. all existing browsers today will use full standards mode for this `DOCTYPE`, even the dated IE6.

If you do use another DOCTYPE, you may risk choosing one which triggers alomost standards mode or quirks mode.

如果你使用其他的DOCTYPE, 你可能会冒着触发接近标准模式或者怪异模式的风险。

确定把DOCTYPE正确地放在HTML文件的顶端。任何放在DOCTYPE前面的东西，比如批注或XML声明，都会令IE 9 或者更早期的浏览器触发怪异模式。

In HTML5, the only purpose of the DOCTYPE is to activate full standards mode. 
没有浏览器会将DOCTYPE用于怪异模式和标准模式之间互换以外的用途。


# [How do I see which mode is used?]()

# [What are the differences between the modes?]()
