

## ✅ **Expression Conversions – Quick Revision**

---

### **1. Infix → Postfix**

**Hint:**
Use a stack; scan left to right. Push operators after popping higher/equal precedence operators (handle parentheses properly).
**Key Rule:**
Operands → output directly.
Operators → pop while `stack.top()` has higher or equal precedence (except `^` which is right-associative).
Parentheses → `(` push, `)` pop until `(`.
**Time Complexity:** O(n).

---

### **2. Infix → Prefix**

**Hint:**
Reverse infix, swap `(` and `)`, then apply infix → postfix logic, and reverse the result.
**Time Complexity:** O(n).

---

### **3. Prefix → Infix**

**Hint:**
Scan **right to left**; push operands. For operator, pop two operands and combine:
`("(" + op1 + operator + op2 + ")")`.
**Stack holds strings.**
**Time Complexity:** O(n²) (due to string concatenation).

---

### **4. Prefix → Postfix**

**Hint:**
Scan **right to left**; push operands. For operator, pop two operands and combine:
`operand1 + operand2 + operator`.
**Time Complexity:** O(n²) (string concatenation).

---

### **5. Postfix → Infix**

**Hint:**
Scan **left to right**; push operands. For operator, pop two operands (`op1` then `op2`), combine:
`("(" + op2 + operator + op1 + ")")`.
**Time Complexity:** O(n²).

---

### **6. Postfix → Prefix**

**Hint:**
Scan **left to right**; push operands. For operator, pop two operands (`op1` then `op2`), combine:
`operator + op2 + op1`.
**Time Complexity:** O(n²).

---

---

### ✅ **Precedence Table**

```
^ : 3 (Right-associative)
*, /, % : 2
+, - : 1
```

---

### ✅ **Best Practice**

* Use `stack<string>` for conversions involving infix.
* For prefix/postfix conversion, `stack<string>` is easiest.
* For efficiency → Use `std::move` or expression tree for O(n).

---

