# markdown开发规范

这是参（复）考（制）了TiDB的文档开发markdown规范，大家学一学文档更得劲。

 [markdownlint 规则](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md)

| NO. | 规则 | 描述 |
| :-- | :-- | :-- |
| 1 | [MD001 - Heading levels should only increment by one level at a time](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md001---heading-levels-should-only-increment-by-one-level-at-a-time) | 标题从一级开始递增使用，禁止跳级使用。例如：一级标题下面不能直接使用三级标题；二级标题下面不能直接使用四级标题。 |
| 2 | [MD003 - Heading style](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md003---heading-style) | 标题必须统一使用 ATX 风格，即在标题前加 `#` 号来表示标题级别。 |
| 3 | [MD018 - No space after hash on atx style heading](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md018---no-space-after-hash-on-atx-style-heading) | 标题的引导符号 `#` 后必须**空一格**再接标题内容。 |
| 4 | [MD019 - Multiple spaces after hash on atx style heading](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md019---multiple-spaces-after-hash-on-atx-style-heading) | 标题的引导符号“#”后只能空**一格**后再接标题内容，不能有多个空格。 |
| 5 | [MD023 - Headings must start at the beginning of the line](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md023---headings-must-start-at-the-beginning-of-the-line) | 标题必须出现在一行行首，即标题的 `#` 号前不能有任何空格。 |
| 6 | [MD026 - Trailing punctuation in heading](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md026---trailing-punctuation-in-heading) | 标题末尾仅能出现中英文问号、反引号、中英文单双引号等符号。其余如**冒号**、逗号、句号、感叹号等符号均不能在标题末尾使用。 |
| 7 | [MD022 - Headings should be surrounded by blank lines](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md022---headings-should-be-surrounded-by-blank-lines) | 标题上下均须空一行。 |
| 8 | [MD024 - Multiple headings with the same content](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md024---multiple-headings-with-the-same-content) | 文档中不能连续出现内容重复的标题，如一级标题为 `# TiDB 架构`，紧接着的二级标题就不能是 `## TiDB 架构`。如果不是连续的标题，则标题内容可重复。 |
| 9 | [MD025 - Multiple top level headings in the same document](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md025---multiple-top-level-headings-in-the-same-document) | 文档中只能出现一个一级标题。一级标题前的元数据（写明了 `title` 和 `category`）不会违反该规则。 |
| 10 | [MD041 - First line in file should be a top level heading](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md041---first-line-in-file-should-be-a-top-level-heading) | 文档正文一开始必须是一级标题。这条规则会自动忽略文档中头几行的元数据，直接检查后面是否有一级标题。 |
| 11 | [MD007 - Unordered list indentation](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md007---unordered-list-indentation) | 一般来说，除 `TOC.md` 文件可缩进 2 个空格外，其余所有 `.md` 文件每缩进一级，默认须缩进 4 个空格。 |
| 12 | [MD010 - Hard tabs](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md010---hard-tabs) | 文档中（包括代码块内）禁止出现 **Tab 制表符**，如需缩进，必须统一用**空格**代替。 |
| 13 | [MD012 - Multiple consecutive blank lines](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md012---multiple-consecutive-blank-lines) | 禁止出现连续的空行。 |
| 14 | [MD027 - Multiple spaces after blockquote symbol](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md027---multiple-spaces-after-blockquote-symbol) | 块引用符号 `>` 后禁止出现多个空格，只能使用**一个**空格，后接引用内容。 |
| 15 | [MD029 - Ordered list item prefix](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md029---ordered-list-item-prefix) | 使用有序列表时，必须从 1 开始，按顺序递增。 |
| 16 | [MD030 - Spaces after list markers](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md030---spaces-after-list-markers) | 使用列表时，每一列表项的标识符（`+`、`-`、`*` 或数字）后只能**空一格**，后接列表内容。 |
| 17 | [MD032 - Lists should be surrounded by blank lines](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md032---lists-should-be-surrounded-by-blank-lines) | 列表（包括有序和无序列表）前后必须各空一行。 |
| 18 | [MD031 - Fenced code blocks should be surrounded by blank lines](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md031---fenced-code-blocks-should-be-surrounded-by-blank-lines) | 代码块前后必须各空一行。 |
| 29 | [MD034 - Bare URL used](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md034---bare-url-used) | 文档中禁止出现裸露的 URL。如果希望用户能直接点击并打开该 URL，则使用一对尖括号 (`<URL>`) 包裹该 URL。如果由于特殊情况必须使用裸露的 URL，不需要用户通过点击打开，则使用一对反引号 (`` `URL` ``) 包裹该 URL。 |
| 20 | [MD037 - Spaces inside emphasis markers](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md037---spaces-inside-emphasis-markers) | 使用加粗、斜体等强调效果时，在强调标识符内禁止出现多余的空格。如不能出现 `` `** 加粗文本 **` ``。 |
| 21 | [MD038 - Spaces inside code span elements](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md038---spaces-inside-code-span-elements) | 单个反引号包裹的代码块内禁止出现多余的空格。如不能出现 `` ` 示例文本 ` ``。 |
| 22 | [MD039 - Spaces inside link text](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md039---spaces-inside-link-text) | 链接文本两边禁止出现多余的空格。如不能出现 `[ 某链接 ](https://www.example.com/)`。 |
| 23 | [MD042 - No empty links](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md042---no-empty-links) | 链接必须有链接路径。如不能出现`[空链接]()`或`[空链接](#)`等情况。 |
| 24 | [MD045 - Images should have alternate text (alt text)](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md045---images-should-have-alternate-text-alt-text) | 图片链接必须添加描述文本（即 `[]()` 的 `[]` 内必须有描述文字），这是为了让无法加载出图片的人看到图片的描述性文字。 |
| 25 | [MD046 - Code block style](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md#md046---code-block-style) | 文档中的代码块统一使用**三个反引号** ` ``` ` 进行包裹，**禁止**使用**缩进四格**风格的代码块。 |