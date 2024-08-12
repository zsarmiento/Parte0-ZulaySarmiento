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

browser->>server: HTTP GET http://studies.cs.helsinki.fi/exampleapp/ejercicio.js
activate server
server->>browser: ejercicio.js
deactivate server

browser->>server: HTTP GET http://studies.cs.helsinki.fi/exampleapp/data.json
activate server
server->>browser: data.json
deactivate server


browser->>server: HTTP GET http://studies.cs.helsinki.fi/exampleapp/new_note_spa
activate server
server->>browser: {"message":"note created"}
deactivate server