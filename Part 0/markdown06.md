sequenceDiagram
    participant browser
    participant server
    
    browser->>server: POST(message) https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: Response (201) note created
    deactivate server
    
    Note right of browser: The page doesn't rerender it just got update with the new note
