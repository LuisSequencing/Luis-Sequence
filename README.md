# Luis-Sequence
**Discovered by @YOUR_USERNAME**

The Luis Sequence is a chaotic recursive formula defined by:
**LS(n, b)**:

- If `n <= 0`  
  → return `1`

- Otherwise  
  → return `n - LS(n - b, b) * (n / 10 + b)`

####################################################################

### 🔬 Properties:
- Recursive
- Chaotic sign flips
- Wave-like explosion patterns
- Atomic-level decimal sensitivity
- Base `b` acts as a frequency modulator

####################################################################

### Example:
```python
from mpmath import mp

mp.dps = 1000

def LS(n, b):
    if n <= 0:
        return mp.mpf(1)
    return n - LS(n - b, b) * (n / 10 + b)

print(LS(mp.mpf("1.0000000000000000001"), mp.mpf("1")))
```
