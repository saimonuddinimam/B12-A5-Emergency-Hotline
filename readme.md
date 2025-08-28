
1. Difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?
Ans:
getElementById is the most direct way to grab something from a webpage. It looks for an element with a specific id and gives you only that one element, because an id should always be unique in a page. It’s super fast and best when you know exactly which single element you want.
getElementsByClassName is for when you want all the elements that share the same class. Instead of giving you just one, it returns a live list of every element with that class. “Live” means if new elements with that class appear later, they’ll automatically show up in the list too.
querySelector is the modern and flexible tool. It uses CSS-style rules to find elements. The catch is that it only gives you the first element that matches. For example, if you ask for .red, you’ll only get the very first red element on the page.
querySelectorAll works like querySelector, but instead of stopping at the first match, it grabs all of them. It returns a NodeList, which is like a snapshot—you can loop through it, but if new elements are added later, they won’t appear in that list automatically.

2. How do you create and insert a new element into the DOM?
Ans:
To create and insert a new element in the DOM, first use document.createElement() to make the element, like let newDiv = document.createElement("div");. Then, add content or attributes, for example newDiv.textContent = "Hello!" or newDiv.className = "myClass";. Finally, select a parent element and insert the new element using appendChild(), like document.getElementById("container").appendChild(newDiv);. This adds the new element to the webpage dynamically.

3. What is Event Bubbling and how does it work?
Ans:
Event bubbling means that when you trigger an event (like clicking a button), it first runs on that exact element, then moves up to its parent, then the parent’s parent, and so on until it reaches the top of the page. For example, clicking a button inside a <div> will fire the button’s event, then the div’s event, then the body’s event. This lets us use event delegation, where instead of adding listeners to many small elements, we can add one listener to a parent and still catch the events.

4. What is Event Delegation and why is it useful?
Ans:
Instead of adding listeners to every child, we add one to the parent and use event.target to check which child was clicked.

Saves performance and works for dynamically added elements.

5. What is the Difference between preventDefault() and stopPropagation() methods?
Ans:
preventDefault() → Stops the browser’s default behavior (like stopping a form submit).

stopPropagation() → Stops the event from bubbling up or down in the DOM tree.