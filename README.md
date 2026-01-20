
# Files Property


When we use (<input type="file" id="videoInput">) and the user selects a file, the browser automatically adds a files property to the input element.

files is a FileList and this.files[0] → the first selected file

Why we write this.files[0], because (<input type="file" multiple>) have attribute (multiple)

# What is URL.createObjectURL(file)?

`It creates a temporary URL for a local file so the browser can use or preview it without uploading.`

It take Parameter (object) as File

Return DOMString

blob:https://example.com/8d9f3c2a-... (This is called a Blob URL.)

# Event

`A JavaScript event is an action (signal) that is happens in the browser (system) and can be detected and handled by JavaScript.`

`An event is a signal that something has happened in the system (user action or browser action), and JavaScript can respond to it using an event handler or listener.`

User actions: (Event)
- click
- keydown
- submit
- mousemove
Browser actions: (Event)
- load
- resize
- scroll

When an event occurs (such as a click), the browser detects it and executes the JavaScript event handler attached to that event. The handler function receives an event object containing details about the event. 
Events are handled using event listeners, and they propagate through the DOM via capturing and bubbling phases.

- (Event propagation in JavaScript describes the order in which events travel through the Document Object Model (DOM))
- It happens in three phases:
01. Capturing Phase (Top → Down)
- Event start from the root and travel to Reaches the target element.
parent.addEventListener('click', handler, true); // capture phase
02. Target Phase
The event reaches the actual element where it happened
button.addEventListener('click', handler);
03. Bubbling Phase (Bottom → Up)
In the bubbling phase, the event starts from the element where it happened and moves up through its parent elements.
parent.addEventListener('click', handler); // bubbling (default)


# Listener

`A JavaScript event listener is a function or method that waits for an event to occur on a specific element (like a button, the entire document, or the window) and then executes a specified block of code in response.` 

element.addEventListener('click', function () {
  console.log('Clicked!');
});
Need to read later
`https://www.geeksforgeeks.org/javascript/what-is-event-propagation-capturing-bubbling/`

# Popular Event
- click
- submit
- input (Live input detect (typing))
- change
- DOMContentLoaded
- scroll
- keydown
- focus / blur (Input validation)
- load
- resize

# Let 
- Change value
- work on Block Scope
- Redeclare same scope
- Resiign later

let add = function(a, b) {
  return a + b;
};
add = 10;

# const
- Need to initilize first
- Never change value
- Objeact/Array not reassign but value change
const user = { name: 'Samiul', age: 25 };
user = { name: 'Ossp' }; (Incorreact)
user.name = 'Ossp'; (Correact)


# video.onloadedmetadata = function () {
  event listener

# URL.revokeObjectURL();

`Frees the memory or resources associated with a dynamically created object URL`