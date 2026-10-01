# 考研英语词组抽背助手

> **考研英语词组抽背卡片** · 2214 条词组 · 纯本地单页工具

简体中文 | [English](#english)

---

## 这是什么

一个考研英语**词组抽背工具**：

> 显示英文词组 → 你回忆中文含义 → 翻卡核对 → 标记「记得 / 忘了」 → 自动记录进度

**双击** `index.html` **就能用**，不用装任何东西，不用联网，手机浏览器也能打开。

**词条示例**：

```
abide by       遵守；信守（承诺、规则等）
account for    解释；说明（原因、理由）；占（比例、数量）
break out      （战争、火灾、疾病等）爆发；逃脱；突然发生
break up       打碎；分裂；解散（组织、集会）；（关系）破裂；分手；破碎
```

## 快速开始

```bash
git clone https://github.com/Nagiko0739/kaoyan-flashcards.git
cd kaoyan-flashcards
```

然后**双击** `index.html` 即可。

> ⚠️ **必须让** `index.html` **和** `data/` **目录待在一起。** 词库是独立的 `data/phrases.js`，
> 单独把 `index.html` 发给别人是打不开词库的。

## 目录结构

```
kaoyan-flashcards/
├── index.html          # 工具本体（页面 + 逻辑，约 470 行）
├── data/
│   ├── phrases.js      # 词库（2214 条，程序加载用）
│   └── phrases.txt     # 同一份词库的纯文本版（英文<TAB>中文，便于导入其他工具）
├── LICENSE
└── README.md
```

## 词库格式

`data/phrases.js`：

```js
window.KAOYAN_PHRASES = [
  { id: 1, english: "abide by", chinese: "遵守；信守（承诺、规则等）", weight: 1.0 },
  // ...
];
```

`data/phrases.txt`（同样内容，制表符分隔）：

```
abide by	遵守；信守（承诺、规则等）
```

**想拿去用在别处**（Anki / 自己的程序 / 转成 JSON）都可以，MIT 协议，注明来源即可。

## 已知限制

- **需要两个文件在一起**（`index.html` + `data/phrases.js`），不能只分享单个 html 文件
- **学习进度存在浏览器本地**（localStorage）：换浏览器、清缓存、换设备都会丢
- 词库**只有释义，没有例句、没有音标、没有发音**
- 词库来自个人备考整理的积累，**不保证覆盖全部考纲词组**，也不保证释义与官方教材完全一致
- 释义合并是自动处理的，个别条目可能出现义项顺序不理想的情况——欢迎提 issue

## 贡献

欢迎补充词条、修正释义、报告重复或错漏。

修改词库请直接改 `data/phrases.js`，并同步 `data/phrases.txt`（两者内容应保持一致）。

## License

[MIT](LICENSE) © 2026 Nagiko0739

---

## English

**kaoyan-flashcards** — a flashcard trainer for Chinese postgraduate-entrance-exam (kaoyan) English phrases.

- **2214 English phrases with Chinese definitions**
- Single-page, fully offline: just open `index.html` in a browser
- The phrase bank lives in `data/phrases.js` and can be reused in other tools (Anki, custom apps, etc.)

**Usage**: clone the repo and open `index.html`. Keep it next to the `data/` folder — the phrase bank is a separate file.

**License**: MIT. The phrase data is free to reuse with attribution.
