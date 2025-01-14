```mermaid
sequenceDiagram
    participant User
    participant Page
    participant Server

    User->>Page: Open page (https://studies.cs.helsinki.fi/exampleapp/notes)
    Page->>Server: Request for existing notes
    Server->>Page: Return existing notes
    Page->>User: Display existing notes

    User->>Page: Enter text into the text field
    User->>Page: Click "Save" button
    Page->>Server: Send the new note data (text)
    Server->>Page: Respond with confirmation (new note saved)
    Page->>User: Display confirmation (note saved)
    Page->>Server: Request for updated list of notes
    Server->>Page: Return updated list of notes
    Page->>User: Display updated list of notes
