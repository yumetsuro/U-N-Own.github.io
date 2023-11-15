---
title: First Post
date: 2023-11-14 15:00:00 +0800
categories: [Personal, Blog]
tags: [blog]     # TAG names should always be lowercase
math: true
---

# Math is Hard, use SARSA (Mayo)

$$
Q(s, a) \leftarrow Q(s, a) + \alpha \left[ R + \gamma Q(s', a') - Q(s, a) \right]
$$

# Images are Easy

![SARSA](/assets/img/sample/sarsa.png)
_What did you expect?_

# Code is Easy

```python
import numpy as np

def sarsa():
    return np.random.rand()
```

# Video are Easy

{% include embed/youtube.html id='dQw4w9WgXcQ' %}

