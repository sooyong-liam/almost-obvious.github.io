---
layout: default
title: Bayes' Theorem
---

# Bayes’ Theorem

$$
P(A \mid B) = \frac{P(B \mid A) \cdot P(A)}{P(B)}
$$

<button id="toggle-details">Toggle Worked Example</button>

<details id="example-details">
  <div>
    Let’s assume 1% have a disease, and the test is 99% accurate.

    This implies:

    - $P(A) = 0.01$
    - $P(B \mid A) = 0.99$
    - $P(B \mid \\neg A) = 0.01$

    Then Bayes’ Theorem tells us:

    $$
    P(A \\mid B) = \\frac{0.99 \\cdot 0.01}{0.99 \\cdot 0.01 + 0.01 \\cdot 0.99}
    $$

  </div>
</details>
