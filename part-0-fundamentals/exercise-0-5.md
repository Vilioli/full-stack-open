sequenceDiagram
    browser->>server:GET https://studies.cs.helsinki.fi/exampleapp/spa
    server->>browser:sends the html document
    browser->>server:GET https://studies.cs.helsinki.fi/exampleapp/main.css
    server->>browser:sends the css file
    browser->>server:GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    server->>browser:sends the javascript file
    note right of browser:Executes the JavaScript program, which requests note data from the server.
    browser->>server:GET https://studies.cs.helsinki.fi/exampleapp/data.json
    server->>browser:sends json containing the note data
    note right of browser:Executes a callback function that renders the note data when it arrives from the server.