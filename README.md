# Luis-Sequence
**Discovered by Luis [Not revealing second name]**

The Luis Sequence is a chaotic recursive formula defined by:  
**LS(n, b)**

- If `n <= 0`  
  → return `1`

- Otherwise  
  → return `n - LS(n - b, b) * (n / 10 + b)`

---

### 🔬 Properties:
- Recursive
- Chaotic sign flips
- Wave-like explosion patterns
- Atomic-level decimal sensitivity
- Base `b` acts as a frequency modulator

---

### 🧪 Example (Python)

#### With `mpmath` (for 1000+ digit accuracy):
```python
from mpmath import mp

mp.dps = 1000

def LS(n, b):
    if n <= 0:
        return mp.mpf(1)
    return n - LS(n - b, b) * (n / 10 + b)

print(LS(mp.mpf("1.0000000000000000001"), mp.mpf("1")))
```

#### Without any libraries (Classic float):
```python
def LS(n: float, base: float):
    if n <= 0:
        return 1
    return n - (LS(n - base, base) * (n / 10 + base))

print(LS(2, 1))
```

#### Heres some output examples:
# *base = 1*
LS(1)   = -0.10000000000000009

LS(2)   = 2.12

LS(3)   = 0.24399999999999977

LS(4)   = 3.6584000000000003

LS(5)   = -0.4876000000000005

LS(6)   = 6.78016

LS(7)   = -4.5262720000000005

LS(8)   = 16.1472896

LS(9)   = -21.67985024

LS(10)  = 53.35970048

# *base = 1*
LS(1, 2)   = -1.1

LS(2, 2)   = -0.20000000000000018

LS(3, 2)   = 5.529999999999999

LS(4, 2)   = 4.48

LS(5, 2)   = -8.825

LS(6, 2)   = -5.6480000000000015

LS(7, 2)   = 30.8275

LS(8, 2)   = 23.814400000000003

LS(9, 2)   = -80.39975

LS(10, 2)  = -61.443200000000004
