```mermaid
sequenceDiagram

participant browser
participant server


browser->>server: HTTP POST https://fullstack-exampleapp.herokuapp.com/new_note
activate server

server->>browser: HTTP 302
deactivate server

browser->>server: HTTP GET https://fullstack-exampleapp.herokuapp.com/notes
activate server
server->>browser: HTML - code
deactivate server

browser->>server: HTTP GET https://fullstack-exampleapp.herokuapp.com/main.css
activate server
server->>browser: main.css
deactivate server

browser->>server: HTTP GET https://fullstack-exampleapp.herokuapp.com/main.js
activate server
server->>browser: main.js
deactivate server


Note right of browser: The browser starts executing the JavaScript code that fetches the JSON from the server

browser->>server: HTTP GET https://fullstack-exampleapp.herokuapp.com/data.json
activate server
server->>browser: [{content:"ejemplo",date "2024-08-08"},...]
deactivate server

