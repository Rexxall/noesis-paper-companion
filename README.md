# Noesis Paper Reader

A small web app for reading research papers: the original PDF on the left, a reading companion and notes on the right. Installable on a phone.

一个读论文的网页应用：左边看原版 PDF，右边是陪读和笔记；可以添加到手机主屏幕。

Live: https://rexxall.github.io/noesis-paper-companion/

## Why / 为什么做

I wanted to read one research paper a day and keep what I learned. Reading in a PDF viewer while copying passages into a chat window was slow, and my notes ended up scattered. The first version was a checklist of tasks; it felt like a to-do card rather than a reader, so it was rebuilt around the PDF itself.

想每天读一篇论文并留下收获。在 PDF 阅读器和聊天窗口之间来回复制太慢，笔记也散。第一版像一张任务卡，不像阅读器，所以改成以 PDF 原文为中心。

## What it does / 功能

- Add a paper by arXiv ID, PDF link, or by uploading a PDF; the list remembers your papers.
- Read the original PDF page by page; switch to the page's plain text.
- Select text → explain, translate, ask a question for the authors, or save as a term card.
- Five-line notes and term cards are kept **per paper**; export them as Markdown.
- Works without an AI key: it copies a ready-made prompt you can paste into any chat tool. With an OpenAI key (stored only in this browser) it answers directly.

## Design choices / 设计取舍

| Choice | Why | Cost |
|---|---|---|
| Everything stays in the browser (localStorage, IndexedDB) | No account, no server; notes are private | Notes do not sync between devices; export Markdown to keep them |
| PDFs are read from the source link or an upload, never stored in the repository | Respect copyright; the repo stays small | Some sites block direct loading — download and upload instead |
| AI is optional; without a key the prompt is copied | Usable with any AI tool, no cost by default | One extra paste step |
| Title is read from the PDF and can be edited | arXiv's API cannot be called from a web page | The guess is sometimes wrong |

## Install on a phone / 手机安装

iPhone: open the link in Safari → Share → Add to Home Screen. Android: open in Chrome → menu → Install app.

