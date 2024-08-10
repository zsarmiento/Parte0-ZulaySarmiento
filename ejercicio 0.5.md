```mermaid
sequenceDiagram

participant browser
participant server


browser->>server: HTTP GET http://studies.cs.helsinki.fi/exampleapp/spa
activate server

server->>browser: HTTP 200
deactivate server

browser->>server: HTTP GET http://studies.cs.helsinki.fi/exampleapp/main.css
activate server
server->>browser: main.css
deactivate server

browser->>server: HTTP GET http://studies.cs.helsinki.fi/exampleapp/spa.js
activate server
server->>browser: spa.js
deactivate server

browser->>server: HTTP GET http://studies.cs.helsinki.fi/exampleapp/data.json
activate server
server->>browser: [{"content":"date":"2024-08-08"},...]
deactivate server
