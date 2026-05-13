sequenceDiagram
browser->>server: POST "https://studies.cs.helsinki.fi/exampleapp/new_note_spa"
    server-->> browser: 201, created.

    Note over server: No re-render, new note seen on frontend due to redrawNotes() updating the DOM. New note present on server side and viewable on browser reload.
