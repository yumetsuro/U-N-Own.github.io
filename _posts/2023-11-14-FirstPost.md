---
title: First Post
date: 2023-11-14 15:00:00 +0800
categories: [Personal, Blog]
tags: [blog]     # TAG names should always be lowercase
math: true
mermaid: true
---

# Math is Hard, use SARSA (Mayo)

$$
Q(s, a) \leftarrow Q(s, a) + \alpha \left[ R + \gamma Q(s', a') - Q(s, a) \right]
$$

# Mermaid is Easy

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

# Images are Easy

![SARSA](assets/imgs/sarsa.png)
_What did you expect?_

# Code is Easy

```python
import numpy as np

def sarsa():
    return np.random.rand()
```


