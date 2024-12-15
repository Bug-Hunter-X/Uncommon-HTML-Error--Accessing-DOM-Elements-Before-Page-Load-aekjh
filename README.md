# Uncommon HTML Error: DOM Element Access Before Page Load

This repository demonstrates a subtle error that can occur in HTML when accessing elements in the Document Object Model (DOM) before the page has fully loaded. Attempting to manipulate elements before they exist can lead to runtime errors and unexpected behavior.

## The Bug

The `bug.html` file contains a simple HTML page with a `div` element and a script that attempts to modify its content immediately. Because the script executes before the DOM is fully parsed and ready, the `getElementById` function may return `null` and trigger an error.

## The Solution

The `bugSolution.html` file demonstrates how to correctly handle this issue. The correct approach is to use an event listener to ensure the script executes only after the DOM is fully parsed, using the `DOMContentLoaded` event. This ensures that the script runs after the HTML elements exist, preventing errors and unexpected behavior.

## How to Reproduce

1. Clone the repository.
2. Open `bug.html` in a web browser. You may or may not see an error in the console, depending on the browser.
3. Open `bugSolution.html` in a web browser. This version should work correctly.