# Uncommon HTML Bug: innerHTML and Null Replacement

This repository demonstrates an uncommon bug related to using `innerHTML` in HTML.  Setting `innerHTML` to `null` unexpectedly prevents subsequent updates to the element's content, even after a delay.

## Bug Description
The provided HTML uses `setTimeout` to try to update the content of a div after a short delay.  However, because `innerHTML` is initially set to `null`, the later attempt to change the `innerHTML` is ineffective. This behavior is not intuitive, and can cause unexpected issues in web development.

## How to Reproduce
1. Open `bug.html` in a web browser.
2. Observe that the text inside the div disappears immediately.
3. After 3 seconds, the text does *not* reappear as expected.  This demonstrates the bug.

## Solution
The solution involves avoiding setting `innerHTML` to `null`.  Instead, use an empty string ("") or remove the element's children using other appropriate methods.