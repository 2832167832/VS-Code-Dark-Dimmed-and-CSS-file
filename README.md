# AnKi 代码高亮卡片模板 
高亮风格：VSCode 深色主题

后续目标：实现 Markdown 中的代码块，解决代码类型只能在 js 源码中修改
```Javascript
<pre><code class="language-html">{{背面}}</code></pre>

    <!-- 引入 Prism.js 库 -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/components/prism-javascript.min.js"></script>

<script>
    document.addEventListener("DOMContentLoaded", function() {
        const back = document.getElementById("back");

        // 应用 Prism.js 高亮
        Prism.highlightAll();
    });
</script>
```

样式
```css
<!-- 包含代码块的卡片内容 -->
<pre><code class="language-javascript">{{YourCodeField}}</code></pre>

<!-- 自定义 CSS 来模仿 VSCode 的黑色主题 -->
<style>
    /* Prism.js 代码块的基础样式 */
pre[class*="language-"],
code[class*="language-"] {
    color: #d4d4d4;
    background: #1e1e1e; /* 代码块背景色 */
    font-family: Consolas, Monaco, 'Andale Mono', 'Ubuntu Mono', monospace;
    font-size: 13px;
    line-height: 1.5;
    border-radius: 4px;
    padding: 10px;
    overflow: auto;
}

/* 注释 */
.token.comment,
.token.block-comment,
.token.prolog,
.token.doctype,
.token.cdata {
    color: #6a9955;
}

/* 标点符号 */
.token.punctuation {
    color: #d4d4d4;
}

/* 属性、标签、关键字等 */
.token.property,
.token.tag,
.token.constant,
.token.symbol,
.token.deleted,
.token.keyword {
    color: #569cd6;
}

/* 布尔值、数字 */
.token.boolean,
.token.number {
    color: #b5cea8;
}

/* 函数 */
.token.function,
.token.class-name {
    color: #dcdcaa;
}

/* 字符串和字符 */
.token.string,
.token.char,
.token.attr-value,
.token.builtin,
.token.inserted {
    color: #ce9178;
}

/* 变量 */
.token.variable {
    color: #9cdcfe;
}

/* 操作符和实体 */
.token.operator,
.token.entity,
.token.url {
    color: #d4d4d4;
}

/* 规则 */
.token.atrule,
.token.attr-value {
    color: #c586c0;
}

/* 正则表达式 */
.token.regex {
    color: #d16969;
}

/* 重要性 */
.token.important {
    font-weight: bold;
}

.token.italic {
    font-style: italic;
}

/* 添加额外的样式 */
.token.deleted {
    text-decoration: line-through;
}

.token.inserted {
    text-decoration: underline;
}

/* 代码块中的行号样式 */
pre[data-line] {
    position: relative;
    padding-left: 3.8em;
}

.line-highlight {
    background: rgba(128, 128, 128, 0.2);
    background-blend-mode: multiply;
}

</style>
```

