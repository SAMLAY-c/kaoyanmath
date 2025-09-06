---
date: 2024-09-06
course: Zhang Yu 30 Lectures
type: formula
category: differentiation
tags: [formula, calculus, derivative, differentiation-rules, math/graduate]
---

# Common Derivative Formulas

## 📝 Basic Derivative Rules

### Power Rule
```latex
d/dx [x^n] = nx^(n-1), where n is any real number
```

**Examples:**
- d/dx [x³] = 3x²
- d/dx [x^(-2)] = -2x^(-3)
- d/dx [√x] = d/dx [x^(1/2)] = (1/2)x^(-1/2) = 1/(2√x)

### Constant Rule
```latex
d/dx [c] = 0, where c is a constant
```

### Constant Multiple Rule
```latex
d/dx [cf(x)] = c · f'(x)
```

### Sum/Difference Rule
```latex
d/dx [f(x) ± g(x)] = f'(x) ± g'(x)
```

## 📝 Exponential and Logarithmic Functions

### Natural Exponential
```latex
d/dx [e^x] = e^x
```

### General Exponential
```latex
d/dx [a^x] = a^x · ln(a)
```

### Natural Logarithm
```latex
d/dx [ln(x)] = 1/x, for x > 0
```

### General Logarithm
```latex
d/dx [log_a(x)] = 1/(x · ln(a))
```

## 📝 Trigonometric Functions

### Basic Trig Derivatives
```latex
d/dx [sin(x)] = cos(x)
d/dx [cos(x)] = -sin(x)
d/dx [tan(x)] = sec²(x)
d/dx [cot(x)] = -csc²(x)
d/dx [sec(x)] = sec(x)tan(x)
d/dx [csc(x)] = -csc(x)cot(x)
```

### Inverse Trigonometric Functions
```latex
d/dx [arcsin(x)] = 1/√(1-x²), for |x| < 1
d/dx [arccos(x)] = -1/√(1-x²), for |x| < 1
d/dx [arctan(x)] = 1/(1+x²)
```

## 📝 Chain Rule

### Basic Chain Rule
```latex
d/dx [f(g(x))] = f'(g(x)) · g'(x)
```

**Examples:**
- d/dx [sin(x²)] = cos(x²) · 2x
- d/dx [e^(3x)] = e^(3x) · 3
- d/dx [ln(2x+1)] = 1/(2x+1) · 2 = 2/(2x+1)

### Extended Chain Rule
```latex
d/dx [f(g(h(x)))] = f'(g(h(x))) · g'(h(x)) · h'(x)
```

## 📝 Product Rule

### Basic Product Rule
```latex
d/dx [f(x) · g(x)] = f'(x) · g(x) + f(x) · g'(x)
```

**Examples:**
- d/dx [x² · sin(x)] = 2x · sin(x) + x² · cos(x)
- d/dx [e^x · ln(x)] = e^x · ln(x) + e^x · (1/x)

### Generalized Product Rule
```latex
d/dx [f(x) · g(x) · h(x)] = f'(x)gh(x) + f(x)g'(x)h(x) + f(x)g(x)h'(x)
```

## 📝 Quotient Rule

### Basic Quotient Rule
```latex
d/dx [f(x)/g(x)] = [f'(x) · g(x) - f(x) · g'(x)] / [g(x)]²
```

**Example:**
- d/dx [sin(x)/x] = [cos(x) · x - sin(x) · 1] / x² = [x cos(x) - sin(x)] / x²

## 📝 Higher Order Derivatives

### Second Derivative
```latex
f''(x) = d²y/dx² = d/dx [f'(x)]
```

### nth Derivative
```latex
f^(n)(x) = dⁿy/dxⁿ
```

### Leibniz Notation
```latex
d²y/dx² = d/dx [dy/dx]
```

## 📝 Implicit Differentiation

### Basic Method
For equations of the form F(x,y) = 0:
1. Differentiate both sides with respect to x
2. Treat y as a function of x (use chain rule)
3. Solve for dy/dx

**Example:**
x² + y² = 1
2x + 2y(dy/dx) = 0
dy/dx = -x/y

## 📝 Parametric Equations

### First Derivative
```latex
If x = f(t), y = g(t), then dy/dx = (dy/dt) / (dx/dt) = g'(t) / f'(t)
```

### Second Derivative
```latex
d²y/dx² = d/dx [dy/dx] = (d/dt [dy/dx]) / (dx/dt)
```

---

**Created:** 2024-09-06  
**Category:** Differentiation Formulas  
**Total Formulas:** 25+  
**Related Topics:** [[Derivative Definition]], [[Integration Formulas]], [[Chain Rule Applications]]

---
## 💡 Memory Tips
- **Power Rule:** "Bring down the exponent, subtract one"
- **Product Rule:** "First times derivative of second, plus second times derivative of first"
- **Quotient Rule:** "Low d-high minus high d-low, square the bottom and away we go"
- **Chain Rule:** "Outside derivative times inside derivative"