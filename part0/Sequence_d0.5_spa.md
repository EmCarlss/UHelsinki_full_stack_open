
```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: User goes to the single page version of the notes app.
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: HTTP status code 201 (Created). JavaScript code it fetched from the server.
    deactivate server
    Note right of browser: No new requst is sent.
```
