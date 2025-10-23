---
marp: true
theme: default # 这里的主题可以更改
paginate: true
class: invert # 这里可以设置颜色
math: katex

# ===============================================
# ===         MY MARP CSS TOOLKIT             ===
# ===============================================
style: |
  /* --- 0. 全局设置 --- */
  /* 在每页右上角添加 Logo */
  section {
    background-image: url('sjtu_logo.png');
    background-repeat: no-repeat;
    background-position: top 20px right 20px;
    background-size: 80px auto; /* 调整 logo 大小，80px 宽度，高度自适应 */
  }

  /* --- 1. 分栏布局 --- */
  /* 两栏布局容器 */
  .two-columns {
    display: flex;
    gap: 2rem; /* 两栏间距 */
    align-items: flex-start; /* 顶部对齐，防止图片撑大容器 */
  }
  .two-columns > .col {
    flex: 1; /* 每栏占据 1 份空间 (平分) */
  }
  /* 三栏布局容器 */
  .three-columns {
    display: flex;
    gap: 1.5rem;
    align-items: flex-start; /* 顶部对齐，适合内容不等高 */
  }
  .three-columns > .col {
    flex: 1;
  }

  /* --- 2. 特殊容器 --- */
  /* 重点突出/结论框 */
  .key-takeaway {
    background-color: #f0f7ff;
    border-left: 5px solid #007bff;
    padding: 1rem 1.2rem;
    border-radius: 8px;
    font-size: 0.9em;
  }
  /* 重点突出/结论框 - 深色版本 */
  .key-takeaway-dark {
    background-color: #1a2332;
    border-left: 5px solid #4a9eff;
    padding: 1rem 1.2rem;
    border-radius: 8px;
    font-size: 0.9em;
    color: #e8f0ff;
  }
  /* 引用/名言块 */
  .quote-block {
    text-align: center;
    font-style: italic;
    font-size: 1.2em;
    padding: 1rem;
  }
  .quote-block footer {
    font-style: normal;
    font-size: 0.8em;
    margin-top: 0.5rem;
    opacity: 0.8;
  }
  .quote-block .footer {
    font-style: normal;
    font-size: 0.8em;
    margin-top: 0.5rem;
    opacity: 0.8;
  }

  /* --- 3. 图片布局 --- */
  /* 2x2 图片网格 */
  .image-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem;
    width: 80%;
    height: auto;
    max-width: 500px;
    margin: 0 auto;
  }
  .image-grid img {
    width: 100%;
    height: auto;
    object-fit: contain;
  }
  
  /* --- 4. 辅助工具 --- */
  /* 让整个页面内容垂直居中（应用到 section） */
  section.v-center {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  /* 让 div 内容垂直居中（应用到 div） */
  .v-center-box {
    display: flex;
    flex-direction: column;
    justify-content: center;
    min-height: 400px;
  }
  /* 缩小文字 */
  .text-sm { font-size: 0.8em; }
  .text-xs { font-size: 0.7em; }

  /* --- 5. 代码块样式 --- */
  /* 自定义代码块背景色 */
  pre {
    background-color: #1e1e1e; /* 深色背景 */
    border-radius: 8px;
    padding: 1rem;
  }
  /* 行内代码样式 */
  code {
    background-color: #2d2d2d; /* 深色背景 */
    color: #e06c75; /* 浅红色文字 */
    padding: 0.2em 0.4em;
    border-radius: 4px;
  }
  /* 代码块内的 code（覆盖行内样式） */
  pre code {
    background-color: transparent; /* 透明，使用 pre 的背景 */
    color: #d4d4d4; /* 浅灰色 */
    padding: 0;
  }
  /* 小字号代码块 */
  .code-sm pre {
    font-size: 0.7em;
  }
  .code-sm code {
    font-size: 0.7em;
  }

  /* --- 6. 两栏代码布局 --- */
  .code-two-columns {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1.5rem;
    font-size: 0.55em;
  }
  .code-two-columns pre {
    margin: 0;
    height: 100%;
  }

---

<!-- =============================================== -->
<!-- ===             SLIDE EXAMPLES              === -->
<!-- =============================================== -->

<!-- _class: invert v-center -->

# Slide Flow 效果展示

### 基于 Marp + AI 的高效演示文稿制作

#### 2025-10-21 塔塔洛夫
---

<!-- 示例1: 两栏布局 -->
## 示例1: 两栏布局

<div class="two-columns">
<div class="col">

### 左侧标题
- 要点一
- 要点二

</div>
<div class="col">

![width:400px](test_image.png)


</div>
</div>

---

<!-- 示例2: 三栏布局 -->
## 示例2: 三栏布局

<div class="three-columns">
<div class="col">

### 特性 A
- 高效
- 灵活
- 易用

</div>
<div class="col">

### 特性 B
- 模块化
- 可复用
- 可扩展

</div>
<div class="col">

### 特性 C
- 美观
- 专业
- 现代化

</div>
</div>

---

<!-- 示例3: 重点结论框 -->
## 示例3: 重点结论框

<div class="key-takeaway-dark">

**核心结论:** 通过预定义 CSS 模板，我们可以将 AI 从“创作者”转变为“执行者”，从而极大地提升 Slides 的制作效率和一致性。

</div>

---

<!-- 示例4: 引用块 -->
## 示例4：引用块

<div class="quote-block">

"The best way to predict the future is to invent it."

<div class="footer">
— Alan Kay
</div>

</div>




---

<!-- 示例5 : 2x2 图片网格 -->
## 示例5：2x2图片网格

<div class="image-grid">
  <img src="test_image.png" alt="Feature A">
  <img src="test_image.png" alt="Feature B">
  <img src="test_image.png" alt="Feature C">
  <img src="test_image.png" alt="Feature D">
</div>

---

<!-- 示例6: 文字大小调整 -->
## 示例6：文字大小调整

### 正常大小文字
这是默认大小的文字，用于主要内容展示。

<div class="text-sm">

### 较小文字 (text-sm)
这是较小的文字（0.8em），适合用于补充说明、注释或次要信息。

</div>

<div class="text-xs">

### 更小文字 (text-xs)
这是更小的文字（0.7em），适合用于版权信息、引用来源或脚注等。

</div>

---

<!-- 示例7: 代码块展示 -->
## 示例7：代码块展示

### Python 示例代码

```python
def greet(name):
    """向用户问候"""
    return f"Hello, {name}!"

# 调用函数
message = greet("World")
print(message)
```

<div class="text-sm">

💡 **提示**: 代码块使用深色背景（#1e1e1e），自动语法高亮

</div>

---

### 小字号代码块

<div class="code-sm">

```javascript
// 使用 .code-sm 类来缩小代码字号
const createSlide = (title, content) => {
  return { title, content, timestamp: Date.now() };
};
```

</div>

---

<!-- 示例8: LaTeX 数学公式 -->
## 示例8：LaTeX 数学公式展示

<div class="text-sm">

### 行内公式
爱因斯坦质能方程：$E = mc^2$

### 块级公式（居中显示）

$$
\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
$$

### 复杂公式示例

$$
f(x) = \frac{1}{\sigma\sqrt{2\pi}} e^{-\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2}
$$


💡 **提示**: 使用 `$...$` 表示行内公式，`$$...$$` 表示块级公式

</div>

---

<!-- 示例9: 两栏代码展示 -->
## 示例9：两栏代码展示

<div class="text-sm">

适合展示较长的代码，左右分栏显示更紧凑

</div>

<div class="code-two-columns">

```python
# 左栏代码
class DataCollector:
    def __init__(self):
        self.data = []
    
    def collect(self, item):
        self.data.append(item)
    
    def process(self):
        for item in self.data:
            print(item)
```

```python
# 右栏代码
class DataAnalyzer:
    def analyze(self, data):
        total = sum(data)
        avg = total / len(data)
        return avg
    
    def report(self):
        print("Analysis complete")
```

</div>

---

<!-- 示例10: 垂直居中 -->
<!-- _class: invert v-center -->

# 示例10：垂直居中

## 整页内容垂直+水平居中

适合用于封面页、章节过渡页



---
<!-- _class: invert v-center -->

# END

## Thanks