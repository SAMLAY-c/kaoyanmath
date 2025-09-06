# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Obsidian-Based Graduate Math Learning System

This is a sophisticated Obsidian-based knowledge management system for graduate-level mathematics learning, specifically designed for Zhang Yu's 30-lecture course. The system leverages Obsidian's core features: atomic notes, Canvas visualization, and bidirectional linking.

### System Architecture

The system is organized into six main directories:

- **00_Templates/** - Standardized templates for consistent note creation
- **01_主题索引/** - Map of Content (MOC) files for knowledge navigation
- **02_Atomic_Notes/** - Individual concept notes with rich metadata
- **03_知识画布/** - Canvas files for visual knowledge graphs
- **05_学习日记/** - Daily learning records and statistics dashboards
- **06_复习回顾/** - Review and reflection materials

### Core Components

#### Atomic Notes System
Each note follows a strict YAML frontmatter schema with:
- Standardized metadata: `note_id`, `chapter`, `lecture`, `topic`, `difficulty`
- Learning tracking: `mastery_level`, `review_count`, `study_time`
- Automated bidirectional connections using Dataview queries
- Structured content: core concepts, detailed analysis, examples, exercises

#### Canvas Knowledge Graphs
JSON-based visualizations with:
- Grouped nodes by concept type (core concepts, theoretical foundation, calculation methods)
- Color-coded connections indicating relationship types
- File nodes linking to atomic notes for interactive exploration
- Hierarchical layout showing knowledge dependencies

#### MOC Index System
Three-tier hierarchy:
- Course level: 张宇30讲-主索引.md
- Chapter level: e.g., 01-函数极限与连续性-MOC.md
- Lecture level: e.g., 01-04-函数极限与性质-MOC.md

#### Learning Analytics
Automated statistics using Dataview:
- Learning progress tracking by difficulty and mastery level
- Review frequency analysis with spaced repetition
- Study time analytics and trends
- Knowledge connection mapping

### Key Technologies

#### Dataview Queries
The system relies heavily on Dataview for automation:
```dataview
TABLE WITHOUT ID
  file.link as "📝 原子笔记",
  topic as "📚 主题",
  difficulty as "🎯 难度"
FROM "02_原子笔记"
WHERE 
  note_id = "01-04-*" OR
  (chapter = "01" AND lecture = "04")
SORT note_id ASC
```

#### Bidirectional Linking
Automatic connection system using:
- `[[concept]]` syntax for manual links
- Dataview queries for automated related content discovery
- Categorized connections: prerequisite, application, related concepts

#### Canvas JSON Structure
Standardized node types:
- `text` nodes for descriptions and groups
- `file` nodes linking to atomic notes
- `group` nodes for concept categorization
- Color coding for difficulty levels and concept types

### Naming Conventions

#### Atomic Notes
Format: `{chapter}-{lecture}-{sequence}-{topic}.md`
Example: `01-04-1-导数定义.md`

#### Canvas Files
Format: `Canvas_{chapter}_{lecture}_{topic}.canvas`
Example: `Canvas_01_04_函数极限与性质-增强版.canvas`

#### MOC Files
Format: `{chapter}-{lecture}-{topic}-MOC.md`
Example: `01-04-函数极限与性质-MOC.md`

### Metadata Schema

#### YAML Frontmatter
```yaml
---
date: YYYY-MM-DD
course: Zhang Yu 30 Lectures
chapter: NN
lecture: NN
topic: [Topic Name]
difficulty: [初级|中级|高级]
note_id: NN-NN-N
type: atomic-note
tags: [atomic-note, [difficulty], [topic], zhang-yu, chapter-[chapter]]
mastery_level: [初学|基本理解|完全掌握]
review_count: N
study_time: N
related_lecture: [[Canvas_[chapter]_[lecture]_[topic]]]
---
```

### Required Obsidian Plugins

1. **Dataview** - For automated queries and data visualization
2. **Canvas** - For knowledge graph visualization
3. **Tasks** - For task management integration
4. **Templates** - For standardized note creation

### Mathematical Formula Formatting

**All mathematical formulas must follow the format specified in [`obsidian公式.md`](obsidian公式.md):**

#### Inline Formulas
Use single dollar signs: `$E = mc^2$`

#### Block Formulas  
Use double dollar signs on separate lines:
```latex
$$
\int_0^\infty e^{-x^2} \, dx = \frac{\sqrt{\pi}}{2}
$$
```

#### Common Examples
- Exponents: `$x^2 + y_i$`
- Fractions: `$\frac{a+b}{c}$`
- Roots: `$\sqrt{x^2 + 1}$`
- Matrices: `$\begin{pmatrix}1 & 2\\3 & 4\end{pmatrix}$`
- Sums/Integrals: `$\sum_{i=1}^n i^2$` or `$\int_a^b f(x)\,dx$`
- Greek letters: `$\alpha + \beta = \gamma$`
- Piecewise functions: `$f(x) = \begin{cases}x^2, & x \geq 0\\-x, & x < 0\end{cases}$`

**Important Notes:**
- All formulas must use dollar sign delimiters, not standard LaTeX `\(...\)` or `\[...\]`
- For complex formulas, consider using the Transfer LaTeX from GPT plugin for format conversion
- For frequent formula input, consider the Latex Suite plugin for shortcuts and autocomplete

### Canvas JSON File Format

**Canvas files must follow the JSON structure specified in [`canvas参考文件.md`](canvas参考文件.md):**

Canvas files use `.canvas` extension with this structure:

```json
{
  "nodes": [
    {
      "id": "unique-id",
      "type": "text|file|link|image|group",
      "text": "content (for text type)",
      "file": "path/to/file.md (for file/image type)",
      "url": "https://example.com (for link type)",
      "x": 100,
      "y": 100,
      "width": 250,
      "height": 150,
      "color": "1-6"
    }
  ],
  "edges": [
    {
      "id": "edge-id",
      "fromNode": "from-node-id",
      "toNode": "to-node-id", 
      "fromSide": "top|bottom|left|right",
      "toSide": "top|bottom|left|right",
      "label": "connection description"
    }
  ]
}
```

**Node Types:**
- `text`: Text content cards
- `file`: Links to markdown files in the vault
- `link`: External web links
- `image`: Image files from the vault
- `group`: Container nodes for organizing other nodes

**Edge Properties:**
- `fromNode`/`toNode`: Node IDs to connect
- `fromSide`/`toSide`: Connection sides (`top`, `bottom`, `left`, `right`)
- `label`: Description text for the connection

**Usage:**
1. Create a text file with the JSON structure
2. Save with `.canvas` extension
3. Place in any directory within the Obsidian vault
4. Open in Obsidian to view and edit the Canvas

### Common Development Tasks

#### Creating New Atomic Notes
1. Copy from `00_Templates/原子笔记模板-优化版.md`
2. Fill in YAML metadata with appropriate values
3. Populate content sections following the standard structure
4. Establish bidirectional links to related concepts
5. Update corresponding Canvas and MOC files

#### Updating Canvas Files
1. Add new file nodes for created atomic notes
2. Position nodes within appropriate concept groups
3. Establish connections showing dependencies and relationships
4. Optimize layout for clarity and visual hierarchy

#### Maintaining MOC Indexes
1. Update lecture-level MOCs with new atomic notes
2. Refresh chapter-level MOCs with lecture updates
3. Ensure learning progress statistics are current
4. Verify all bidirectional links are functional

### Data Flow Architecture

```
Learning Activity → Atomic Note Creation → Metadata Tagging
       ↓
Bidirectional Linking → Canvas Visualization → MOC Integration
       ↓
Daily Recording → Progress Tracking → Review Scheduling
```

This creates a self-reinforcing knowledge management system where each component enhances the others through automated connections and data flow.