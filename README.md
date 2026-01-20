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