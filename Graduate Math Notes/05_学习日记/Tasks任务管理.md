---
tags: [tasks/任务管理]
---

# ✅ Tasks插件任务管理系统

## 📋 今日任务概览

### 今日待办
```tasks
not done
due today
path includes 05_学习日记
sort by due
```

### 今日已完成
```tasks
done
done today
path includes 05_学习日记
sort by done
```

---

## 📅 本周任务计划

### 本周待办
```tasks
not done
due before this file.name + 7 days
path includes 05_学习日记
sort by due
```

### 本周已完成
```tasks
done
done after this.file.name - 7 days
path includes 05_学习日记
sort by done
```

---

## 🎯 学习任务模板

### 新建学习任务
```markdown
- [ ] #task 学习 [[知识点名称]] 📚
  scheduled:: 2024-09-06
  due:: 2024-09-06
  tags:: #学习 #数学/考研
  difficulty:: 初级
  estimated_time:: 30分钟
```

### 复习任务
```markdown
- [ ] #task 复习 [[笔记名称]] 🔄
  scheduled:: 2024-09-07
  due:: 2024-09-07
  tags:: #复习 #数学/考研
  review_type:: 日度复习
  estimated_time:: 15分钟
```

### 练习任务
```markdown
- [ ] #task 完成 [[练习题名称]] ✏️
  scheduled:: 2024-09-06
  due:: 2024-09-06
  tags:: #练习 #数学/考研
  estimated_time:: 45分钟
  difficulty:: 中级
```

---

## 📊 任务统计分析

### 按标签分类的任务
```tasks
not done
tags include #学习
path includes 05_学习日记
```

```tasks
not done
tags include #复习
path includes 05_学习日记
```

```tasks
not done
tags include #练习
path includes 05_学习日记
```

### 按优先级分类
```tasks
not done
priority is high
path includes 05_学习日记
```

```tasks
not done
priority is medium
path includes 05_学习日记
```

```tasks
not done
priority is low
path includes 05_学习日记
```

---

## 🔄 定期任务管理

### 每日例行任务
```tasks
not done
recurrence matches daily
path includes 05_学习日记
```

### 每周例行任务
```tasks
not done
recurrence matches weekly
path includes 05_学习日记
```

### 每月例行任务
```tasks
not done
recurrence matches monthly
path includes 05_学习日记
```

---

## 🎯 任务完成情况追踪

### 今日完成率
```tasks
done today
path includes 05_学习日记
```

### 本周完成情况
```tasks
done after this.file.name - 7 days
path includes 05_学习日记
```

### 本月完成情况
```tasks
done after this.file.name - 30 days
path includes 05_学习日记
```

---

## 📝 任务管理最佳实践

### 任务命名规范
- **学习任务**: `学习 [知识点]`
- **复习任务**: `复习 [笔记名称]`
- **练习任务**: `完成 [练习题]`
- **整理任务**: `整理 [文件/文件夹]`

### 任务标签系统
- `#学习`: 新知识学习
- `#复习`: 复习已有知识
- `#练习`: 做练习题
- `#整理`: 整理文件和笔记
- `#数学/考研`: 数学考研相关
- `#英语/考研`: 英语考研相关

### 任务优先级设置
- **🔴 高优先级**: 紧急重要的任务
- **🟡 中优先级**: 重要但不紧急的任务
- **🟢 低优先级**: 紧急但不重要的任务

---

## 🚀 自动化任务生成

### 基于学习记录生成任务
```tasks
not done
description includes 学习
path includes 05_学习日记
```

### 基于复习计划生成任务
```tasks
not done
description includes 复习
path includes 05_学习日记
```

### 基于时间生成任务
```tasks
not done
due after this.file.name
due before this.file.name + 7 days
path includes 05_学习日记
```

---

*最后更新: 2024-09-06*