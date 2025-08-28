
1. Difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?
Ans:
getElementById("id") → Selects one element with a specific id.
getElementsByClassName("class") → Returns multiple elements with that class as a live HTMLCollection.
querySelector("css") → Selects the first element matching the CSS selector.
querySelectorAll("css") → Selects all matching elements and returns a NodeList.

2. How do you create and insert a new element into the DOM?
Ans:
Use document.createElement("tag") to create.

Add content: element.textContent = "Hello".

Insert into DOM with appendChild(), prepend(), or insertBefore().

3. What is Event Bubbling and how does it work?
Ans:
When an event happens, it doesn’t stop at the element.

It travels upward (child → parent → document).

Example: Clicking a button also triggers click on its parent div.

4. What is Event Delegation and why is it useful?
Ans:
Instead of adding listeners to every child, we add one to the parent and use event.target to check which child was clicked.

Saves performance and works for dynamically added elements.

5. What is the Difference between preventDefault() and stopPropagation() methods?
Ans:
preventDefault() → Stops the browser’s default behavior (like stopping a form submit).

stopPropagation() → Stops the event from bubbling up or down in the DOM tree.