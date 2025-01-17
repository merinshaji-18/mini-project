```mermaid
sequenceDiagram
    participant User
    participant Browser
    participant Server

    User->>Browser: Open page (https://studies.cs.helsinki.fi/exampleapp/notes)
    Browser->>Server: Request for existing notes
    activate Server
    Server->>Browser: Return existing notes
    deactivate Server
    Browser->>User: Display existing notes

    User->>Browser: Enter text into the text field
    User->>Browser: Click "Save" button
    Browser->>Server: Send the new note data (text)
    activate Server
    Server->>Browser: Respond with confirmation (new note saved)
    deactivate Server
    Browser->>User: Display confirmation (note saved)
    Browser->>Server: Request for updated list of notes
    activate Server
    Server->>Browser: Return updated list of notes
    deactivate Server
    Browser->>User: Display updated list of notes

