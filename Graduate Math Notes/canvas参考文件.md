好的，我明白了。你想要的是 Obsidian Canvas 的 **json 文件格式规范**，而不是功能说明。

我来给你提供一份 Obsidian Canvas 的 **标准 JSON 模板**，你可以直接复制使用，或者交给 AI 生成符合这个规范的内容：

---

### 📄 Obsidian Canvas 的 JSON 文件规范（标准模板）

文件名：`canvas.canvas`（扩展名必须是 `.canvas`）

```json
{
  "nodes": [
    {
      "id": "node-id-1",
      "type": "text",
      "text": "这是一个文本卡片",
      "x": 100,
      "y": 100,
      "width": 250,
      "height": 150,
      "color": "1"
    },
    {
      "id": "node-id-2",
      "type": "file",
      "file": "笔记文件名.md",
      "x": 400,
      "y": 100,
      "width": 300,
      "height": 200
    },
    {
      "id": "node-id-3",
      "type": "link",
      "url": "https://obsidian.md",
      "x": 100,
      "y": 300,
      "width": 300,
      "height": 180
    },
    {
      "id": "node-id-4",
      "type": "image",
      "file": "assets/image.png",
      "x": 450,
      "y": 350,
      "width": 200,
      "height": 200
    }
  ],
  "edges": [
    {
      "id": "edge-id-1",
      "fromNode": "node-id-1",
      "fromSide": "right",
      "toNode": "node-id-2",
      "toSide": "left",
      "label": "连接说明文字"
    }
  ]
}
```

---

### 🔍 字段说明（JSON 结构详解）

| 字段名 | 类型 | 说明 |
|---|---|---|
| `nodes` | 数组 | 所有卡片节点 |
| `edges` | 数组 | 所有连接线 |

#### ✅ Node 字段（每个卡片）

| 字段名 | 类型 | 说明 |
|---|---|---|
| `id` | 字符串 | 卡片唯一标识符 |
| `type` | 字符串 | 卡片类型：`text`、`file`、`link`、`image`、`group` |
| `text` | 字符串 | 仅 `type=text` 时使用，卡片内容 |
| `file` | 字符串 | 仅 `type=file` 或 `type=image` 时使用，对应 Vault 中的文件路径 |
| `url` | 字符串 | 仅 `type=link` 时使用，网页链接 |
| `x`, `y` | 数字 | 卡片左上角坐标 |
| `width`, `height` | 数字 | 卡片宽高 |
| `color` | 字符串 | 卡片颜色编号（1-6 对应 Obsidian 内置颜色） |

#### ✅ Edge 字段（每条连接线）

| 字段名 | 类型 | 说明 |
|---|---|---|
| `fromNode` | 字符串 | 起点卡片 ID |
| `toNode` | 字符串 | 终点卡片 ID |
| `fromSide`, `toSide` | 字符串 | 连接方向：`top`、`bottom`、`left`、`right` |
| `label` | 字符串 | 连接线上的文字说明 |

---

### 📥 使用方法

1. 新建一个文本文件，粘贴上述 JSON。
2. 保存为 `xxx.canvas`（扩展名必须是 `.canvas`）。
3. 放入你的 Obsidian Vault 根目录或任意子目录。
4. 打开 Obsidian，即可在文件列表中看到并打开这个 Canvas。

---

如果你需要我帮你生成一个具体的 Canvas JSON 文件（比如包含特定笔记、图片、连接关系），告诉我具体内容，我可以直接帮你生成。