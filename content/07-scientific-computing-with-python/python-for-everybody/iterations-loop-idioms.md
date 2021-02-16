---
id: 5e7b9f070b6c005b0e76f05e
title: 'Iterações: Loop Idioms'
challengeType: 11
videoId: AelGAcoMXbI
dashedName: iterations-loop-idioms
---

# --question--

## --text--

Abaixo vemos um código para achar o menor valor em uma lista de valores. Uma linha tem um erro que fará com que o código não trabalhe como o esperado. Qual linha é essa?:

```python
smallest = None
print("Before:", smallest)
for itervar in [3, 41, 12, 9, 74, 15]:
    if smallest is None or itervar < smallest:
        smallest = itervar
        break
    print("Loop:", itervar, smallest)
print("Smallest:", smallest)
```

## --answers--

3

---

4

---

6

---

7

## --video-solution--

3

