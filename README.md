# Markdown简明语法教程

**说明：**

* 本教程基于Markdown语言编写，项目地址位于[Simple-Markdown-Guide](https://github.com/Melo618/Simple-Markdown-Guide)。
* 本教程定位为基础教程，更加详细的用法可参考其他资料。
* 本教程中代码块内的代码为Markdown的语法。
* 本教程中部分语法使用的是[GitHub Flavored Markdown](https://help.github.com/articles/github-flavored-markdown/)，GFM语法与标准语法在不同环境中存在解析差异，本教程在使用时会加以说明。
* 推荐使用Haroopad(Win)、MarkdownPad(Win)和Mou(OS X)编辑器，部分编辑器中文效果欠佳，可通过自定义CSS字体解决。

## 基本

* Markdown是一种用来写作的轻量级标记语言。
* 用标记语法，来代替常见的排版格式。
* 兼容 HTML代码。
* 特殊字符自动转换，例如`<`和`&`。

## 字体

* 使用星号`*`和底号`_`表示`<em>`标签。

  例如：

  ```
  *斜体*
  _斜体_
  ```

  效果：

  *斜体*

* 使用双星号`**`和双底号`__`表示`<strong>`标签。

  例如：

  ```
  **强调**
  __强调__
  ```

  效果：

  **强调**

## 换行

* 单一段落用空白行。

## 标题

* 生成`<h1>`-`<h6>`标签，是通过在文字前面加上同等个数`#`符号来实现。
* 出于美观，也可以使用对称的闭合式标题符号。

  例如：

  ```
  ### 这是标题
  ### 这是标题 ###
  ```

  效果：

  ### 这是标题

## 列表

* `*`，`-`，`+`这三个符号效果都一样，这3个符号被称为Markdown列表符号。而有序列表则使用数字接着一个英文句点（数字大小并不会影响输出序列）。

  例如：

  ```
  * 第一行
  * 第二行
  * 第三行
  6. 第四行
  5. 第五行
  4. 第六行
  ```

  效果：

  * 第一行
  * 第二行
  * 第三行
  6. 第四行
  5. 第五行
  4. 第六行

## 引用

* `>`符号表示引用，可简写于第一行，也可以每一行都添加。
* 区块的引用可以嵌套，只需要在层次数上加上同等数量的`>`符号。
* 引用内可以使用其他Markdown语法，包括标题、列表、代码区块等。

  例如：

  ```
  >    引用
  >    >    引用中的引用
  ```

  效果：

  >    引用
  >    >    引用中的引用

## 代码区块

* <code>\`</code>是表示inline代码，4个<code> </code>（空格）来表示缩进式代码段，分别对应HTML的`<code>`，`<pre>`标签。也可以使用<code>\`\`\`</code>来表达围栏式代码块（**GFM语法**，部分编辑器不支持），并指定他的语言类型，实现语法高亮。围栏式代码块可以大量减少缩进的使用，大规模的代码块使用非常方便。

  例如：

  ```
  `sort()` 函数按升序对给定数组的值排序。
  ```

  普通的缩进式代码块。

  ```
      <?php
          $my_array = array('a' => 'Dog', 'b' => 'Cat');
          sort($my_array);
          print_r($my_array);
      ?>
  ```

  带语法高亮的围栏式代码块（**GFM语法**，部分编辑器不支持）。

      ```php
      <?php
          $my_array = array('a' => 'Dog', 'b' => 'Cat');
          sort($my_array);
          print_r($my_array);
      ?>
      ```

  效果：

  `sort()` 函数按升序对给定数组的值排序。

  普通的缩进式代码块。

      <?php
          $my_array = array('a' => 'Dog', 'b' => 'Cat');
          sort($my_array);
          print_r($my_array);
      ?>

  带语法高亮的围栏式代码块（**GFM语法**，部分编辑器不支持）。

  ```php
  <?php
      $my_array = array('a' => 'Dog', 'b' => 'Cat');
      sort($my_array);
      print_r($my_array);
  ?>
  ```

## 链接

* Markdown支持两种形式的链接语法：行内式和参考式两种形式。

  行内式链接，是在方括号后面接圆括号即可。
  例如：

  ```
  [Google](https://www.google.com "Google")
  ```

  效果：

  [Google](https://www.google.com "Google")

  参考式链接，是在链接文字的括号后面加上另一个方括号，在第二个方括号里面要填入用以辨识链接的标记。
  例如：

  ```
  [Google][GOOGL]

  [GOOGL]: https://www.google.com "Google"
  ```

  效果：

  [Google][GOOGL]

  [GOOGL]: https://www.google.com "Google"

## 图片

* Markdown使用一种和链接很相似的语法来标记图片，只是多了一个`!`在最前面，同样也允许两种样式：行内式和参考式。
* 目前为止，Markdown还没有办法指定图片的宽高，如果你需要的话，你可以使用普通的`<img>`标签。

  行内式链接，是在方括号后面接圆括号即可。
  例如：

  ```
  ![Wikipedia](https://www.wikipedia.org/portal/wikipedia.org/assets/img/Wikipedia-logo-v2.png "Wikipedia")
  ```

  效果：

  ![Wikipedia](https://www.wikipedia.org/portal/wikipedia.org/assets/img/Wikipedia-logo-v2.png "Wikipedia")

## 分隔线

* 使用三个以上的`*`、`-`来建立一个分隔线，行内不能有其他字符。

  例如：

  ```
  * * *
  ***
  - - -
  ---
  ```

  效果：

  上文
  - - -
  下文

## 表格

* Markdown使用`|`和`-`来绘制表格，`:`可控制左对齐、右对齐及居中。

  例如：

  ```
  | Title   | Description                        |
  | :------ | :--------------------------------: |
  | Version | 0.0.1                              |
  | Editor  | [Melo618](mailto:Editor@Email.com) |
  ```

  效果：

  | Title   | Description                        |
  | :------ | :--------------------------------: |
  | Version | 0.0.1                              |
  | Editor  | [Melo618](mailto:Editor@Email.com) |

## 特殊符号

* Markdown利用`\`字符来转义一些在语法中有特殊意义的符号。

## 推荐阅读

* [Markdown语法说明（简体中文版）](http://wowubuntu.com/markdown/index.html)
* [Markdown Syntax Documentation](http://daringfireball.net/projects/markdown/syntax)
* [GitHub Flavored Markdown](https://help.github.com/articles/github-flavored-markdown)

## License

  Copyright © 2014-2018, Melo Chan. [MIT License](http://opensource.org/licenses/MIT).
