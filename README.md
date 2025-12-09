🌐 JavaScript DOM (Document Object Model)

DOM is how JavaScript “sees” and controls a web page.
Without DOM, JavaScript cannot change HTML or CSS.

🧠 What Exactly is the DOM?

When a browser loads an HTML file:

It reads the HTML

Converts it into a tree structure

Each HTML element becomes an object

This tree is called the Document Object Model (DOM) 🌳

👉 JavaScript interacts with this tree to:

Change text

Change styles

Add / remove elements

React to user actions

🚪 Entry Point: document

The document object is the doorway to the DOM.

console.log(document);


Commonly used properties:

document.title → page title

document.body → <body> element

document.head → <head> element

document.title = "Ojas is King";
document.body.style.backgroundColor = "yellow";


✅ Page changes instantly (no refresh)

🌳 DOM = Tree of Nodes

Everything in DOM is a node.

Types of Nodes:

Element Nodes → <div>, <body>

Text Nodes → text + spaces + line breaks

Comment Nodes

document.body.childNodes;


⚠️ Important:
Spacing and indentation in HTML create text nodes.

👶 childNodes vs children (Very Important)
childNodes

Returns ALL nodes

Includes text nodes

element.childNodes;

children

Returns ONLY element nodes

Ignores text nodes ✅

element.children;


✅ Use children in most real projects

🧭 Navigating the DOM (Traversal)
Moving Down
element.firstChild;
element.lastChild;

element.firstElementChild;   // ignores text
element.lastElementChild;

Moving Up
element.parentElement;

Moving Sideways (Siblings)
element.nextElementSibling;
element.previousElementSibling;


👉 Used to jump between nearby elements

🎨 Styling HTML Using JavaScript

JavaScript can change CSS dynamically:

element.style.color = "red";
element.style.backgroundColor = "yellow";


📌 Notes:

Style properties use camelCase

Adds inline styles

🔎 Selecting Elements from the DOM
🔹 getElementById
document.getElementById("blue");


Selects one unique element

Fast & simple

🔹 getElementsByClassName
document.getElementsByClassName("box");


Returns HTMLCollection

Not an array

🔹 getElementsByTagName
document.getElementsByTagName("div");


Selects all elements of a tag

⭐ Modern Selectors (Most Powerful)
querySelector
document.querySelector(".box");


Returns first match only

Uses CSS selectors

querySelectorAll
document.querySelectorAll(".box");


Returns NodeList

Can loop using forEach

document.querySelectorAll(".box").forEach(box => {
  box.style.backgroundColor = "yellow";
});


✅ Most used in modern JavaScript

✅ matches() – Element Check

Checks whether an element matches a selector:

element.matches("#blue");


Returns:

true

false

🧗 closest() – Move Upward Smartly

Finds the nearest ancestor (or itself) matching a selector:

element.closest(".container");


✅ Traverses upwards in the DOM tree

📦 contains() – Parent Check

Checks if one element contains another:

parent.contains(child);


Returns:

true

false

🧩 Real-World Understanding
Concept	Meaning
childNodes	Everything (including text)
children	Only elements ✅
querySelectorAll	Best & flexible
closest()	Go up
nextElementSibling	Go sideways
contains()	Parent-child check
🎯 Interview Gold Points

✔ DOM is a tree structure
✔ Text nodes appear due to spacing
✔ Prefer children over childNodes
✔ querySelectorAll + forEach is modern
✔ DOM changes happen without page reload
