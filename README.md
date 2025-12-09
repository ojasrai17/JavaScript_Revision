# JavaScript_Revision

📘 JavaScript DOM – Theory Notes
1️⃣ What is DOM?

DOM (Document Object Model) is a programming interface that represents an HTML document as a tree of nodes so JavaScript can read, change, add, or delete elements dynamically.

Browser converts HTML → DOM

DOM is an object

JS uses document to access DOM

console.log(document);

2️⃣ document Object

document is the entry point to the DOM.

Common properties:

document.title

document.body

document.head

Example:

document.title = "New Title";
document.body.style.backgroundColor = "yellow";


✅ Changes happen without reloading the page

3️⃣ Nodes in DOM

Everything in DOM is a node.

Types of Nodes:

Element Node → <div>, <body>

Text Node → text & whitespace

Comment Node

document.body.childNodes


⚠️ Whitespace (line breaks & spaces) are text nodes

4️⃣ childNodes vs children
childNodes

Returns ALL nodes

Includes text nodes

element.childNodes

children

Returns only element nodes

Most commonly used

element.children


✅ Preferred: children

5️⃣ DOM Traversal (Moving in DOM)
Parent
element.parentElement

First / Last Child
element.firstChild          // includes text
element.lastChild

element.firstElementChild   // ignores text
element.lastElementChild

6️⃣ Sibling Navigation
element.nextElementSibling
element.previousElementSibling


Used to move horizontally between elements.

7️⃣ Styling Elements using DOM
element.style.color = "red";
element.style.backgroundColor = "yellow";


✅ Inline styles are added dynamically
✅ Property names use camelCase

8️⃣ DOM Selectors
getElementById
document.getElementById("blue");


Selects single element

Very fast

getElementsByClassName
document.getElementsByClassName("box");


Returns HTMLCollection

Not array

getElementsByTagName
document.getElementsByTagName("div");


Selects all elements of that tag

9️⃣ querySelector & querySelectorAll
querySelector
document.querySelector(".box");


Returns first matching element

Accepts CSS selectors

querySelectorAll
document.querySelectorAll(".box");


Returns NodeList

Can use forEach

document.querySelectorAll(".box").forEach(e => {
  e.style.backgroundColor = "yellow";
});


✅ Most flexible & modern method

🔟 matches()

Checks if an element matches a CSS selector

element.matches("#blue");


Returns:

true

false

1️⃣1️⃣ closest()

Finds the nearest ancestor (or itself) that matches a selector.

element.closest(".container");


✅ Moves upwards in DOM

1️⃣2️⃣ contains()

Checks whether an element contains another element

parent.contains(child);


Returns:

true

false

✅ Key Points for Interview

DOM is tree-based

childNodes include text → spacing matters

children ignores text nodes ✅

querySelectorAll is most powerful

closest() moves upward

contains() checks parent-child relation
