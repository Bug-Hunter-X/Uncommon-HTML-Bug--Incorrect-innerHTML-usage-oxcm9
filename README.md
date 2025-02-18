# Uncommon HTML Bug: Incorrect innerHTML Usage

This repository demonstrates a subtle bug related to the use of `innerHTML` in HTML.  The issue arises from attempting to replace the content of a div with a newly created DOM node using `innerHTML`.  `innerHTML` expects a string; when given a node, it converts the node into a string representation rather than inserting the node itself.

## Bug Description
The `bug.html` file contains a simple HTML structure with a div and a script. The script attempts to replace the div's content with a new div element using `innerHTML`. However, due to this incorrect usage, the new div is not added to the DOM; instead, the div's content becomes a text string representation of the node.  This will appear visually different to a user.

## Solution
The `bugSolution.html` provides the corrected version.  The solution uses `replaceChild()` or `appendChild()` to properly insert the new div node into the DOM.