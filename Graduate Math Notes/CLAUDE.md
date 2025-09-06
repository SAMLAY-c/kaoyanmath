# Zhang Yu 30 Lectures Course Content Tracking System

## 📋 Course Content Record

### Foundation Section (00_Foundation)
| Lecture | Topic | Status | Atomic Notes | Canvas File | Processing Date |
|---------|-------|--------|--------------|-------------|-----------------|
| 00-01 | Introduction | ⏳ | 0 | - | - |
| 00-02 | Basic Knowledge Structure | ⏳ | 0 | - | - |
| 00-03 | Basic Logic | ⏳ | 0 | - | - |
| 00-04 | Expression Concepts and Operations | ⏳ | 0 | - | - |
| 00-05 | Equations and Inequalities | ⏳ | 0 | - | - |
| 00-06 | Functions | ⏳ | 0 | - | - |
| 00-07 | Sequences and Monotonicity | ⏳ | 0 | - | - |
| 00-08 | Coordinate Systems and Transformations | ⏳ | 0 | - | - |

### Formal Course (01-05)
| Lecture | Topic | Status | Atomic Notes | Canvas File | Processing Date |
|---------|-------|--------|--------------|-------------|-----------------|
| 01-01 | Function Limits and Continuity - Basic Knowledge Structure | ⏳ | 0 | - | - |
| 01-02 | Function Concepts and Properties | ⏳ | 0 | - | - |
| 01-03 | Function Graphs | ⏳ | 0 | - | - |
| 01-04 | Function Limit Concepts and Properties | ⏳ | 0 | - | - |
| 01-05 | Limit Calculations | ⏳ | 0 | - | - |
| 01-06 | Function Continuity and Discontinuity | ⏳ | 0 | - | - |
| 01-07 | Notes | ⏳ | 0 | - | - |
| 02-01 | Sequence Limits - Basic Knowledge Framework | ⏳ | 0 | - | - |
| 02-02 | Sequence Limits - Basic Content Detailed | ⏳ | 0 | - | - |
| 03-01 | Single Variable Differential Calculus Concepts - Basic Knowledge Structure | ⏳ | 0 | - | - |
| 03-02 | Single Variable Differential Calculus Concepts - Basic Content Detailed | ⏳ | 0 | - | - |
| 04-01 | Single Variable Differential Calculus Calculations - Basic Knowledge Structure | ⏳ | 0 | - | - |
| 04-02 | Single Variable Differential Calculus Calculations - Basic Content Detailed | ⏳ | 0 | - | - |
| 05-01 | Single Variable Differential Calculus Applications - Basic Knowledge Structure | ⏳ | 0 | - | - |
| 05-02 | Single Variable Differential Calculus Applications - Basic Content Detailed | ⏳ | 0 | - | - |

## 🔢 Atomic Note Numbering System

### Numbering Rules
- **Format**: `[Chapter]-[Lecture]-[Sequence]`
- **Example**: `01-04-1` (Chapter 1 - Lecture 4 - First atomic note)
- **Prefix**: All atomic note filenames start with this number

### Created Atomic Notes
| Number | Note Title | Created Date | Link |
|--------|------------|--------------|------|
| 01-04-1 | Derivative Definition | 2024-09-06 | [[01-04-1-Derivative Definition]] |
| 01-04-2 | Common Derivative Formulas | 2024-09-06 | [[01-04-2-Common Derivative Formulas]] |

## 🎨 Canvas File System

### File Naming Rules
- **Format**: `Canvas_[Chapter]_[Lecture]_[Topic].md`
- **Location**: `03_Canvas/` directory
- **Example**: `Canvas_01_04_Function_Limits_and_Properties.md`

### Canvas Structure Template
```markdown
# 🎨 Canvas: [Lecture Topic]

## 📋 Knowledge Points List
1. **Knowledge Point 1**: [[01-04-1-Related Atomic Note]]
2. **Knowledge Point 2**: [[01-04-2-Related Atomic Note]]
3. **Knowledge Point 3**: [[01-04-3-Related Atomic Note]]

## 📊 Knowledge Graph Layout
[Visualization layout description]

## 🔗 Knowledge Connections
- **Prerequisites**: [[Prerequisite knowledge links]]
- **Applications**: [[Application knowledge links]]
- **Related Concepts**: [[Related concept links]]
```

## 📝 Content Processing Workflow

### When user provides Markdown course manuscript:
1. **Update this file**: Record lecture information in corresponding table
2. **Analyze heading structure**: 
   - Scan all heading levels in the document
   - Identify the base heading level (could be #, ##, or ###)
   - Determine relative hierarchy for mapping
3. **Parse Markdown structure**: Extract content based on relative heading levels
4. **Normalize content organization**: 
   - Map base level → Canvas/Lecture title
   - Map base+1 level → Main topic categories
   - Map base+2 level → Individual atomic notes
   - Preserve all original formatting and content
5. **Create atomic notes**: Generate numbered atomic notes using the normalized structure
6. **Generate Canvas**: Create dedicated Canvas file with knowledge point mapping
7. **Establish links**: Create bidirectional links between related atomic notes
8. **Update MOC**: Add new content to corresponding chapter MOC

### File Management Rules
- **Atomic Notes**: Store in `02_Atomic_Notes/[Category]/` directory
- **Canvas Files**: Store in `03_Canvas/` directory  
- **Daily Records**: Store in `05_Daily_Notes/` directory
- **Review Materials**: Store in `02_Atomic_Notes/Review_Materials/` directory
- **Study Plans**: Store in `02_Atomic_Notes/Study_Plans/` directory
- **Templates**: Store in `00_Templates/` directory
- **MOCs**: Store in `01_MOCs/` directory

## 🛠️ Automation Script Instructions

### Batch Creation Commands
```bash
# Create atomic notes for new lecture
touch "02_Atomic_Notes/Calculus/01-04-3-Concept_Name.md"

# Create canvas file for new lecture
touch "03_Canvas/Canvas_01_04_Lecture_Topic.md"

# Update CLAUDE.md records
# [Manual update of tables and number lists]
```

### Template Application
- Use templates from `00_Templates/` to create new notes
- Uniformly use numbered prefixes for filenames
- Record corresponding lecture information in metadata

## 📊 Statistics

### Overall Progress
- **Total Lectures**: 16 lectures (8 foundation + 8 formal)
- **Processed Lectures**: 0 lectures
- **Created Atomic Notes**: 2
- **Created Canvas**: 0

### Recent Updates
- **Last Update**: 2024-09-06
- **Next Processing**: Waiting for user-provided Markdown course manuscript
- **Processing Format**: Markdown (.md files only, not PDF)

---

**File Maintenance**: Update this file when processing new course manuscripts  
**Version**: 1.0  
**Created**: 2024-09-06

---

## 📝 Markdown Processing Guidelines

### Supported Markdown Features
- **Headings**: `#`, `##`, `###` for knowledge hierarchy
- **Lists**: Bullet points and numbered lists
- **Code blocks**: For mathematical formulas and code
- **Tables**: For structured data
- **Links**: Both external and internal Obsidian links
- **Bold/Italic**: For emphasis
- **Blockquotes**: For important notes

### Markdown to Atomic Notes Conversion
#### Handling Irregular Heading Hierarchies
Since Markdown headings may be inconsistent (starting with ### instead of #), the system uses:

1. **Heading Level Analysis**: 
   - Detect the highest level heading used in document
   - Normalize levels based on relative hierarchy
   - Map to atomic note structure regardless of absolute level

2. **Relative Hierarchy Mapping**:
   - **Highest level found** → Lecture/Canvas level
   - **Second level** → Main topic categories  
   - **Third level** → Individual atomic notes
   - **Fourth level+** → Sub-notes or examples

3. **Flexible Conversion Rules**:
   - Whatever is the main heading (#, ##, or ###) → Canvas file name
   - One level down → Main topic areas
   - Two levels down → Individual atomic notes
   - Code blocks → Formula atomic notes
   - Lists → Practice atomic notes

### Example Markdown Structures

#### Standard Structure:
```markdown
# Lecture 01: Function Limits

## 1.1 Definition of Limits
The limit of f(x) as x approaches a...

### Key Properties
- Property 1
- Property 2

## 1.2 Limit Laws
```

#### Irregular Structure (Starting with ###):
```markdown
### 第一讲 函数极限

#### 1.1 极限的定义
函数f(x)当x趋近于a时的极限...

##### 关键性质
- 性质1
- 性质2

#### 1.2 极限法则
```

#### Mixed Structure:
```markdown
## 概念定义

### 极限的ε-δ定义
对于任意ε>0，存在δ>0...

#### 应用例子
例子1：证明lim[x→2] x² = 4

### 计算方法
直接代入法、因式分解法...
```

### Processing Best Practices
- **Preserve formatting**: Keep original Markdown structure
- **Extract metadata**: Lecture number, topic, difficulty
- **Create links**: Automatically link related concepts
- **Maintain hierarchy**: Use relative heading levels for organization
- **Handle irregularities**: Adapt to whatever heading structure is provided

### Heading Analysis Algorithm
1. **Scan all headings**: Find all `#`, `##`, `###`, etc. in document
2. **Determine base level**: Identify the highest-level heading (minimum # count)
3. **Normalize hierarchy**: 
   - Base level → Lecture/Canvas level
   - Base+1 → Main topics
   - Base+2 → Atomic notes
   - Base+3+ → Sub-notes/examples
4. **Handle edge cases**:
   - Single level documents: Create artificial hierarchy
   - Mixed languages: Preserve original, add English translations
   - Inconsistent formatting: Normalize to consistent structure

### Input Requirements
- **Format**: .md files only
- **Encoding**: UTF-8
- **Structure**: Clear heading hierarchy
- **Content**: Mathematical concepts in LaTeX code blocks