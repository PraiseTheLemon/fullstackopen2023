```mermaid
sequenceDiagram
  participant browser
  participant server

  browser->>server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note
  activate server
  server-->>browser: Status Code 302
  deactivate server

  browser->>server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/notes
  activate server
  server-->>browser: HTML Code
  deactivate server

  browser->>server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
  activate server
  server-->>browser: main.css
  deactivate server

  browser->>server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.js
  activate server
  server-->>browser: main.js
  deactivate server

  browser->>server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
  activate server
  server-->>browser: [{content: "Workers of the world, unite!", date: "2023-06-16T14:10:00.899Z"},...]
  deactivate server

  ```
