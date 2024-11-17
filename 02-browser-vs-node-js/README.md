# Browser JavaScript vs Node.js

Browser JavaScript designed to execute JavaScript in web browsers It’s focused on frontend development while, Node.js is a runtime envrionment for executing JavaScript code on server-side. It’s focused on backend development tasks like handling HTTP requests, file I/O, and building APIs.

## APIs and Features Differences

**Browser JavaScript:**

Provides browser-specific APIs like:

- DOM Manipulation (`document`).
- Event Handling (`addEventListener`).
- Fetch API for making HTTP requests.
- Web storage API (`localstorage`, `sessionStorage`).
- Restricted access to system resources for security.

**Node.js:**

Provides sever-specific APIs like:

- File System (`fs`) for reading/writing files.
- HTTP Module (`http`) for building servers.
- Streams for processing data efficiently.
- Process Management (`process`, `child_process`).
- No support for browser-specific features like DOM or window.

## Concurrency and Asynchronous Handling

**Browser JavaScript:**

- Single-threaded with asynchronous operations managed via the **event loop**.
- Supports **Web Workers** for multi-threading.

**Node.js:**

- Also single-threaded but uses **libuv** for managing asynchronous I/O tasks.
- Supports **Worker Threads** for multi-threading and clustering for scaling across CPU cores.

## Global Object

**Browser JavaScript:**

- The global object is `window`. Variables declared globally are accessible through `window`.

**Node.js:**

- The global object is `global`. However, global variables are not added to `global` unless explicitly declared.

## Module system

**Browser JavaScript:**

- Modules in the browser can be import using `script` tag with the `type` attribute set to `module` and the `src` attribute set to the path of the module file.

```html
<script type="module" src="./some-dir/module.js"></script>
```

- Supports ES6 Modules (`import`/`export`) for modular development.

**Node.js:**

- Uses CommonJS Modules (`require`/`module.exports`).
- Modern Node.js supports ES6 Modules with `.mjs` files or "type": "module" in package.json.
