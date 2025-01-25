---
tags:
  - Markdown
---

# Markdown 扩展语法

* [Python Markdown](https://squidfunk.github.io/mkdocs-material/setup/extensions/python-markdown/) 提供了灵活的扩展机制。
* [PyMdown Extensions](https://squidfunk.github.io/mkdocs-material/setup/extensions/python-markdown-extensions/) 包是一个优秀的附加扩展集合，非常适合高级技术写作。

## 1. Abbreviations 缩写
[Abbreviations](https://python-markdown.github.io/extensions/abbreviations/) 缩写可以通过使用类似于URL和脚注的特殊语法来定义，以*开头，紧接着是方括号中要关联的术语或缩写：

``` markdown title="Text with abbreviations"
The HTML specification is maintained by the W3C.

*[HTML]: Hyper Text Markup Language
*[W3C]: World Wide Web Consortium
```

<div class="result" markdown>
The HTML specification is maintained by the W3C.

*[HTML]: Hyper Text Markup Language
*[W3C]: World Wide Web Consortium
</div>

## 2. Admonition 警告
[Admonition](https://squidfunk.github.io/mkdocs-material/reference/admonitions/) 扩展添加了对警告的支持，通常称为标注，可以使用简单的语法在 Markdown 中定义。

``` markdown title="Admonition"
!!! note "change title"
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.
```

<div class="result" markdown>
!!! note "change title"

    Lorem ipsum dolor sit amet, consectetur adipiscing elit.
</div>

**删除标题**

``` markdown title="Admonition without title"
!!! note ""
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.
```

<div class="result" markdown>
!!! note ""

    Lorem ipsum dolor sit amet, consectetur adipiscing elit.
</div>

**可折叠块**

``` markdown title="Admonition, collapsible"
??? note
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.
```

<div class="result" markdown>
??? note

    Lorem ipsum dolor sit amet, consectetur adipiscing elit.
</div>

在 `???` 后面添加 `+` 可折叠并自动展开

``` markdown title="Admonition, collapsible and initially expanded"
???+ note
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.
```

<div class="result" markdown>
???+ note
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.
</div>

**内联块**

Admonitions 警告也可以呈现为内联块（例如，对于侧边栏），使用 inline + end 修饰符将它们放置在右侧，或仅使用 inline 修饰符将它们放置在左侧

=== "inline end"

    !!! info inline end "Lorem ipsum"

        Lorem ipsum dolor sit amet

    ``` markdown
    !!! info inline end "Lorem ipsum"

        Lorem ipsum dolor sit amet
    ```

=== "inline"

    !!! info inline "Lorem ipsum"

        Lorem ipsum dolor sit amet
    
    ``` markdown
    !!! info inline "Lorem ipsum"

        Lorem ipsum dolor sit amet
    ```

**支持的类型**

!!! note
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.

!!! abstract
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.

!!! info
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.

!!! tip
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.

!!! success
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.

!!! question
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.

!!! warning
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.

!!! failure
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.

!!! danger
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.

!!! bug
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.

!!! example
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.

!!! quote
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.


## 3. Annotations 注释

[Annotations](https://squidfunk.github.io/mkdocs-material/reference/annotations/) 注释由两部分组成：标记和内容。

``` markdown title="Text with annotations"
Lorem ipsum dolor sit amet, (1) consectetur adipiscing elit.
{ .annotate }

1.  I'm an annotation!
```

<div class="result" markdown>
Lorem ipsum dolor sit amet, (1) consectetur adipiscing elit.
{ .annotate }

1.  I'm an annotation!
</div>



## 4. Buttons 按钮
[Buttons](https://squidfunk.github.io/mkdocs-material/reference/buttons/ "官方文档") 将链接呈现为按钮。


``` markdown title="Button"
[Subscribe to our newsletter](#){ .md-button }

[Subscribe to our newsletter](#){ .md-button .md-button--primary }
```


<div class="result" markdown>

[Subscribe to our newsletter](#){ .md-button }

[Subscribe to our newsletter](#){ .md-button .md-button--primary }

</div>


## 5. Definition Lists 定义列表
[Definition Lists](https://squidfunk.github.io/mkdocs-material/reference/lists/) 可以在文本中插入词汇定义列表，相对于脚注和缩写会更加直接明了。

``` markdown title="Definition list"
`Lorem ipsum dolor sit amet`

:   Sed sagittis eleifend rutrum. Donec vitae suscipit est.

`Cras arcu libero`

:   Aliquam metus eros, pretium sed nulla venenatis, faucibus auctor ex.
```

<div class="result" markdown>

`Lorem ipsum dolor sit amet`

:   Sed sagittis eleifend rutrum. Donec vitae suscipit est.

`Cras arcu libero`

:   Aliquam metus eros, pretium sed nulla venenatis, faucibus auctor ex.

</div>


## 6. Footnotes 脚注
[Footnotes](https://squidfunk.github.io/mkdocs-material/reference/footnotes/) 脚注是在不中断文档流程的情况下为特定单词、短语或句子添加补充或附加信息的好方法。


``` title="Text with footnote references"
Lorem ipsum[^1] dolor sit amet, consectetur adipiscing elit.[^2]

[^1]: Lorem ipsum dolor sit amet, consectetur adipiscing elit.
[^2]:
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.
```

<div class="result" markdown>

Lorem ipsum[^1] dolor sit amet, consectetur adipiscing elit.[^2]

[^1]: Lorem ipsum dolor sit amet, consectetur adipiscing elit.
[^2]:
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

</div>



## 7. Grids 网格
[Grids](https://squidfunk.github.io/mkdocs-material/reference/grids) 网格非常适合构建索引页面，显示文档大部分内容的简要概述。


## 8. Tables 表格
[Tables](https://squidfunk.github.io/mkdocs-material/reference/data-tables/) 可以在文本中插入数据表格，用于展示数据。通过添加自定义的 CSS 样式和 JS 脚本，可以实现排序、对齐等多种增强功能。



## 9. Tooltips 工具提示
[Tooltips](https://squidfunk.github.io/mkdocs-material/reference/tooltips) 为每个链接指定一个标题，当启用改进的工具提示时，该标题将呈现为漂亮的工具提示。


``` markdown title="Link with tooltip, inline syntax"
[Hover me](https://example.com "I'm a tooltip!")
```

<div class="result" markdown>

[Hover me](https://example.com "I'm a tooltip!")

</div>

还可以将工具提示添加到链接引用中

``` markdown title="Link with tooltip, reference syntax"
[Hover me][example]

  [example]: https://example.com "I'm a tooltip!"
```

<div class="result" markdown>

[Hover me](https://example.com "I'm a tooltip!")

</div>


## 10. Arithmatex 算术软件
[Arithmatex](https://facelessuser.github.io/pymdown-extensions/extensions/arithmatex/) 扩展允许渲染块和内联块方程，并与 MathJax（数学排版库）无缝集成。  
MathJax 和 KaTeX 是两个流行的库，用于在浏览器中显示数学内容。

## 11. Caret, Mark & Tilde 下划线, 高亮 & 删除线

[Caret](https://facelessuser.github.io/pymdown-extensions/extensions/caret/)、[Mark](https://facelessuser.github.io/pymdown-extensions/extensions/mark/) 和 [Tilde](https://facelessuser.github.io/pymdown-extensions/extensions/tilde/) 扩展添加了使用简单语法突出显示文本并定义下标和上标的功能。

``` markdown title="Caret, Mark & Tilde"
^^下划线^^
==马克高亮==
~~删除线~~
```

<div class="result" markdown>

^^下划线^^  
==马克高亮==  
~~删除线~~  

</div>


## 12. Critic 评论
[Critic](https://facelessuser.github.io/pymdown-extensions/extensions/critic/) 扩展允许使用 Critic 标记来突出显示文档中添加、删除或更新的部分，即用于跟踪 Markdown 语法的更改。


## 13. Code blocks 代码块
[Code blocks](https://squidfunk.github.io/mkdocs-material/reference/code-blocks/) 在基本语法的基础上增加了大量的特性，可以支持标题、行号、高亮、复制、注释等多种功能。

**特定行高亮**

=== "Lines"

    ```` markdown title="Code block with highlighted lines"
    ``` py hl_lines="2 4"
    def bubble_sort(items):
        for i in range(len(items)):
            for j in range(len(items) - 1 - i):
                if items[j] > items[j + 1]:
                    items[j], items[j + 1] = items[j + 1], items[j]
    ```
    ````

    <div class="result" markdown>

    ``` py linenums="1" hl_lines="2 4"
    def bubble_sort(items):
        for i in range(len(items)):
            for j in range(len(items) - 1 - i):
                if items[j] > items[j + 1]:
                    items[j], items[j + 1] = items[j + 1], items[j]
    ```

    </div>

=== "Line ranges"

    ```` markdown title="Code block with highlighted line range"
    ``` py hl_lines="3-5"
    def bubble_sort(items):
        for i in range(len(items)):
            for j in range(len(items) - 1 - i):
                if items[j] > items[j + 1]:
                    items[j], items[j + 1] = items[j + 1], items[j]
    ```
    ````

    <div class="result" markdown>

    ``` py linenums="1" hl_lines="3-5"
    def bubble_sort(items):
        for i in range(len(items)):
            for j in range(len(items) - 1 - i):
                if items[j] > items[j + 1]:
                    items[j], items[j + 1] = items[j + 1], items[j]
    ```

    </div>


**内联代码块显示高亮**
``` markdown title="Inline code block"
The `#!python range()` function is used to generate a sequence of numbers.
```

<div class="result" markdown>

The `#!python range()` function is used to generate a sequence of numbers.

</div>


## 14. Content tabs 内容选项卡
[Content tabs](https://squidfunk.github.io/mkdocs-material/reference/content-tabs/) 可以在文本中插入用标签切换的内容块，用于在同一个块中平行展示多个内容。

``` title="Content tabs with code blocks"
=== "C"

    ``` c
    #include <stdio.h>

    int main(void) {
      printf("Hello world!\n");
      return 0;
    }
    ```

=== "C++"

    ``` c++
    #include <iostream>

    int main(void) {
      std::cout << "Hello world!" << std::endl;
      return 0;
    }
    ```
```

<div class="result" markdown>

=== "C"

    ``` c
    #include <stdio.h>

    int main(void) {
      printf("Hello world!\n");
      return 0;
    }
    ```

=== "C++"

    ``` c++
    #include <iostream>

    int main(void) {
      std::cout << "Hello world!" << std::endl;
      return 0;
    }
    ```

</div>


## 15. Emoji 表情符号
[Emoji](https://facelessuser.github.io/pymdown-extensions/extensions/emoji/) 表情符号扩展会自动将 *.svg 文件格式的捆绑和自定义图标以及表情符号内联到生成的 HTML 页面中。
Material for MkDocs中使用： [Icons, Emojis](https://squidfunk.github.io/mkdocs-material/reference/icons-emojis/)


## 16. Keys 按键
[Keys](https://facelessuser.github.io/pymdown-extensions/extensions/keys/) 扩展添加了一个简单的语法来允许呈现键盘按键和组合。

``` markdown title="Keyboard keys"
++ctrl+alt+del++
```

<div class="result" markdown>

++ctrl+alt+del++

</div>


## 17. Tasklist 任务列表
[Tasklist](https://facelessuser.github.io/pymdown-extensions/extensions/tasklist/) 启用任务列表后，无序列表项可以以 [ ] 为前缀来呈现未选中的复选框，或以 [x] 为前缀来呈现已选中的复选框，从而允许定义任务列表：

``` markdown title="Task list"
- [x] Lorem ipsum dolor sit amet, consectetur adipiscing elit
- [ ] Vestibulum convallis sit amet nisi a tincidunt
    * [x] In hac habitasse platea dictumst
    * [x] In scelerisque nibh non dolor mollis congue sed et metus
    * [ ] Praesent sed risus massa
- [ ] Aenean pretium efficitur erat, donec pharetra, ligula non scelerisque
```

<div class="result" markdown>

- [x] Lorem ipsum dolor sit amet, consectetur adipiscing elit
- [ ] Vestibulum convallis sit amet nisi a tincidunt
    * [x] In hac habitasse platea dictumst
    * [x] In scelerisque nibh non dolor mollis congue sed et metus
    * [ ] Praesent sed risus massa
- [ ] Aenean pretium efficitur erat, donec pharetra, ligula non scelerisque

</div>