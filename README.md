# Marp Snippets 使用说明

> 下面仅代表我个人的配置喜好，大家可以随便 DIY 自己需要的模板！


## 第一次使用前，请设置 VSCode-Markdown 中的 Snippet 显示！
写好 Snippet 文件之后，markdown 还是不会显示自动补全，因为 `settings.json` 中没有相关配置。

这时候，需要在 `settings.json` 的末尾补上一段：
```json
"[markdown]": {
    "editor.quickSuggestions": {
        "other": "on",
        "comments": "on",
        "strings": "on"
    },
    "editor.suggest.showSnippets": true,
    "editor.snippetSuggestions": "top"
}
```

最终 `settings.json` 的效果类似这样：
```json
{   
    "other_settings": {
    },
    "[markdown]": {
    "editor.quickSuggestions": {
        "other": "on",
        "comments": "on",
        "strings": "on"
    },
    "editor.suggest.showSnippets": true,
    "editor.snippetSuggestions": "top"
    }
}
```

这样就能正常显示 markdown 的 snippet 了。

## 基本用法

在 Markdown 文件中输入前缀，按 `Tab` 键插入模板。

也可以使用快捷键 `Ctrl+Shift+P`，输入 `Snippets: Insert Snippet`，查看可以快速插入的 Snippet 以及对应的效果说明。

---

## Snippets 列表

### `marp-2col`
**两栏布局** - 创建左右两栏的内容布局

### `marp-3col`
**三栏布局** - 创建三栏并列布局

### `marp-key`
**重点结论框** - 深蓝色背景框，用于突出显示关键内容

### `marp-quote`
**引用块** - 插入引用文字，带署名

### `marp-img`
**图片** - 插入大小可调的图片

### `marp-img4`
**2×2 图片网格** - 展示 4 张图片的网格布局

### `marp-sm`
**较小文字** - 字体缩小到 0.8em

### `marp-xs`
**更小文字** - 字体缩小到 0.7em

### `marp-code-sm`
**小字号代码块** - 插入较小字号的代码块

### `marp-code-2col`
**两栏代码布局** - 将代码分成左右两栏显示，适合长代码或代码对比

### `marp-vcenter`
**垂直居中幻灯片** - 创建内容垂直居中的幻灯片，常用于封面页、章节页

### `marp-slide`
**新幻灯片** - 创建新的幻灯片页面