---
date: 2024-09-06
course: Zhang Yu 30 Lectures
lecture: 01
topic: Derivative Definition
difficulty: beginner
tags: [math/graduate, zhang-yu, calculus, derivative, definition, limits]
---

# Derivative Definition

## 📝 Core Concepts

### Definition
The derivative of a function f(x) at point x₀ is defined as the limit of the difference quotient:

```latex
f'(x₀) = lim[h→0] [f(x₀+h) - f(x₀)] / h
```

### Alternative Form
```latex
f'(x₀) = lim[x→x₀] [f(x) - f(x₀)] / (x - x₀)
```

### Key Properties
- **Geometric meaning**: Slope of the tangent line at point (x₀, f(x₀))
- **Physical meaning**: Instantaneous rate of change
- **Existence**: Limit must exist and be finite
- **Uniqueness**: If derivative exists, it's unique

### Visual Representation
![Derivative as tangent line slope](media/derivative_geometric_meaning.png)

## 🔍 Detailed Analysis

### Theoretical Foundation
- Based on the concept of limits
- Requires function to be defined in a neighborhood of x₀
- Connects to continuity (differentiable ⇒ continuous)

### Problem-Solving Approaches
1. **Direct substitution**: Use limit definition directly
2. **Algebraic manipulation**: Simplify before taking limit
3. **Graphical approach**: Estimate from graph
4. **Numerical approach**: Use small h values

### Common Mistakes
- Forgetting to check if limit exists
- Algebraic errors in simplification
- Confusing derivative with function value
- Misapplying limit laws

## 💡 Examples

### Example 1: Basic Application
**Problem:** Find f'(2) if f(x) = x²

**Solution:** 
f'(2) = lim[h→0] [(2+h)² - 2²] / h
= lim[h→0] [4 + 4h + h² - 4] / h
= lim[h→0] [4h + h²] / h
= lim[h→0] (4 + h) = 4

**Key Insight:** The derivative of x² at x=2 is 4, which matches the slope of the tangent line.

### Example 2: Advanced Application
**Problem:** Find f'(0) if f(x) = |x|

**Solution:** 
f'(0) = lim[h→0] [|0+h| - |0|] / h
= lim[h→0] |h| / h

This limit does not exist because:
- Right-hand limit: lim[h→0⁺] h/h = 1
- Left-hand limit: lim[h→0⁻] (-h)/h = -1

**Key Insight:** Absolute value function is not differentiable at x=0.

## 🔗 Connections

### Prerequisites
- [[Limit Definition]]
- [[Continuity Definition]]
- [[Function Concept]]

### Applications
- [[Tangent Line Equation]]
- [[Velocity and Acceleration]]
- [[Optimization Problems]]

### Related Concepts
- [[Partial Derivatives]]
- [[Higher Order Derivatives]]
- [[Differentiation Rules]]

## 📚 Practice Problems

### Problem Set
1. Find f'(1) for f(x) = x³ using the definition
2. Show that f(x) = x² is differentiable at all points
3. Prove that f(x) = |x-1| is not differentiable at x=1
4. Find the derivative of f(x) = √x at x=4

### Solutions
1. f'(1) = lim[h→0] [(1+h)³ - 1³] / h = lim[h→0] (1 + 3h + 3h² + h³ - 1)/h = lim[h→0] (3 + 3h + h²) = 3
2. For any x₀: f'(x₀) = lim[h→0] [(x₀+h)² - x₀²]/h = lim[h→0] (2x₀h + h²)/h = 2x₀, which exists for all x₀
3. Similar to |x| case, left and right limits differ at x=1
4. f'(4) = lim[h→0] [√(4+h) - 2]/h = 1/4 (rationalize numerator)

## 🎯 Summary

### Key Takeaways
- Derivative represents instantaneous rate of change
- Definition relies on limit concept
- Not all functions are differentiable everywhere
- Geometric interpretation as tangent slope

### Memory Aids
- **"Rise over run"** in the limit as run approaches zero
- **Slope of tangent line** visualization
- **Instantaneous speed** analogy

---

**Created:** 2024-09-06 15:30  
**Last Modified:** 2024-09-06 15:30  
**Course Progress:** Lecture 1/30  

---
## 📊 Metadata
- **Study Time:** 45 minutes
- **Mastery Level:** Understanding
- **Review Count:** 1
- **Related Lectures:** Lecture 1 (Foundation), Lecture 8 (Formal)
- **Practice Problems Completed:** 4/4