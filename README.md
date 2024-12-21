# CSS Specificity Issue with !important

This repository demonstrates a subtle issue related to CSS specificity and the `!important` declaration.  The issue lies in how specificity and `!important` interact; simply using `!important` doesn't always guarantee the rule's dominance. The example highlights a scenario where expected behavior doesn't occur due to conflicting specificity.

The `bug.css` file contains the problematic code, and the `bugSolution.css` file offers a solution that ensures the desired styling applies consistently, regardless of specificity conflicts.

## How to Reproduce

1.  Clone this repository.
2.  Open `bug.html` (or create your own HTML with equivalent structure) in a web browser.
3.  Observe the font size of the paragraph.  You may find it larger than expected because of the CSS specificity issue.  Note that this behavior may be browser-dependent.

## Solution

The `bugSolution.css` file provides a solution that demonstrates how to work around the specificity issue and enforce the desired font size reliably.

## Key Learning

This example emphasizes the importance of understanding CSS specificity when working with `!important` declarations. While `!important` provides a high-weight rule, it doesn't automatically bypass specificity.  This is a common pitfall when attempting to override styles deeply nested in the DOM.