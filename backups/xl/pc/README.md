# 富文本编辑器选择

>1. 鉴于我们网站对浏览器版本兼容性的要求，大部分开源的库都可以使用。
>2. 受欢迎的库，都支持直接插入HTML，并且都支持基本的富文本操作（原生JS就已经支持）。
>3. 鉴于我们的技术栈是Vue，因此暂不考虑依赖jQuery或React的库（如：[slate](https://github.com/ianstormtaylor/slate)、[draft-js](https://github.com/facebook/draft-js)）。

选择富文本编辑器，尝试从三个方面考虑：

1. 引入文件的大小，性能问题，license。
2. 提供的功能和操作UI。
3. 是否方便扩展。

从github中找出以下几款比较适合我们网站的开源库，它们对比如下。

| library       | license | size (min+gzip) | 横向对比 | 试用 |
|---------------|-----------------|------------|--------|-----------|
| [pell](https://github.com/jaredreich/pell) | MIT | 1kB | 原生`document.execCommand`书写，只是一个简单框架，没有任何额外实现。方便原生扩展（或者说根本就是原生JS简单实现的富文本编辑器框架）。 | [demo](https://jaredreich.com/pell/) |
| [quill](https://github.com/quilljs/quill) | BSD-3-Clause | 46kB | 扩展性好。实现一套数据结构（Delta），可以不依赖DOM，需要了解一些概念。最"现代"的库。 | [demo](https://quilljs.com/playground/) |
| [trix](https://github.com/basecamp/trix) | MIT | 50kB | UI美观，支持插入各种文件。基本编辑功能很完整，意味着较差的可扩展性。 | [demo](https://trix-editor.org/) |
| [medium-editor](https://github.com/yabwe/medium-editor) | MIT | 27kB | 内嵌式编辑器，按照<https://medium.com/>的编辑功能来实现。编辑习惯与普通编辑器不同，不适合我们大部分场景。 | [demo](https://yabwe.github.io/medium-editor/demo.html) |
| [tinymce](https://github.com/tinymce/tinymce) | LGPL-2.1 | 151kB | 很重很大很全面，有很多插件可供选择。适合做公司内部编辑器，不适合我们大部分场景。 | [demo](https://www.tiny.cloud/) |
| [ckeditor5](https://github.com/ckeditor/ckeditor5) | GNU General Public License Version 2 or later | 146kB | 需要购买权限，很重很大很全面、甚至支持多人协作。不适合我们大部分场景。 | [demo](https://ckeditor.com/ckeditor-5/demo/) |

- 其他库备选

    1. [wangEditor](https://github.com/wangfupeng1988/wangEditor/)：国内个人开发者作品。不方便扩展。
    2. [tiptap](https://github.com/scrumpy/tiptap)：基于Vue。
    3. [Squire](https://github.com/neilj/Squire)
    4. [ory-editor](https://github.com/aeneasr/ory-editor)

> 2019.03.13 xx下载平台前端


>参考：
>
>1. <https://github.com/JefMari/awesome-wysiwyg>
>2. <https://github.com/xjh22222228/awesome-web-editor>
>3. <https://www.zhihu.com/topic/19595126/top-answers>
