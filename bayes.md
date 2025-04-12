---
layout: default
title: Bayes' Theorem
---

# Bayes’ Theorem

$$
P(A \mid B) = \frac{P(B \mid A) \cdot P(A)}{P(B)}
$$

<!-- Custom Toggle Button for the collapsible -->
<button id="toggle-details">Toggle Worked Example</button>

<!-- The details block with math inside -->
<details id="example-details">
  <div>
    Let’s assume 1% have a disease, test is 99% accurate.

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

<script>
  // The toggle button logic with MathJax retypesetting
  document.getElementById('toggle-details').addEventListener('click', function(){
    var detailsEl = document.getElementById('example-details');
    detailsEl.open = !detailsEl.open;

    if(detailsEl.open && window.MathJax && MathJax.typesetPromise) {
      MathJax.typesetPromise([detailsEl])
        .then(function(){
          console.log("MathJax has reprocessed the newly revealed content.");
        })
        .catch(function(err){
          console.error("MathJax typeset failed: " + err.message);
        });
    }
  });
</script>
