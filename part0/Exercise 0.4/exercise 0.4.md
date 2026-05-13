sequenceDiagram
    browser->>server: POST "https://studies.cs.helsinki.fi/exampleapp/new_note"
    server-->>browser: Tells to do GET to "/exampleapp/notes" (redirect URL after POST with 302)


    browser->>server: GET "https://studies.cs.helsinki.fi/exampleapp/notes"
    server-->>browser: notes document

    browser->>server: GET "https://studies.cs.helsinki.fi/exampleapp/main.css"
    server-->>browser: main.css

    browser->>server: GET "https://studies.cs.helsinki.fi/exampleapp/main.js"
    server-->>browser: main.js (javascript file received, browser asks data.json)

    browser->>server: GET "https://studies.cs.helsinki.fi/exampleapp/data.json"
    server-->>browser: data.json ({"content": "...", "date": "..."}) (includes newly added note)