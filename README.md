# 🗂️ VaultShare — Backend Developer


## Core Features

### 1. Authentication

- User registration and login (JWT or session-based — your choice, justify it)
- Each user has a private file space

### 2. File Management

- Upload files (any type; set a reasonable size limit)
- Download files
- Download an entire folder as a ZIP archive — think carefully about how you handle this when the folder is large
- Delete files (soft delete preferred — nothing truly disappears)
- List files in your own space with metadata: name, size, MIME type, uploaded at, last modified
- Organise files into **folders**

### 3. Sharing

- Share a file or folder with another registered user
- Three permission levels: **Viewer** (download only), **Editor** (upload/rename), **Owner** (full control including delete and re-share)
- A user can see all files and folders shared with them in a unified "Shared with me" view
- Revoke access at any time (owner only)
- **Public link sharing**: generate a time-limited, shareable link for a file that works without authentication (like Google Drive's "Anyone with the link")

### 4. File Versioning

- Uploading a file with the same name into the same folder creates a new **version**, not a duplicate
- Users can list versions of a file and download any previous version
- The current version is always the default download

### 5. Activity Log (Audit Trail)

- Every meaningful action is recorded: upload, download, share, permission change, delete, version created, link generated
- The log includes: actor, action, target (file/folder), timestamp, IP address
- Users can view the activity log for files they own
- This log is **append-only** — no deletes, no updates


