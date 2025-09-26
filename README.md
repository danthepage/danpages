# danpages.me - A Full-Stack Go Web Application

This repository contains the complete source code for my personal portfolio, blog, and custom-built financial ledger, available at [danpages.me](https://danpages.me). The entire application is built from scratch in Go, following professional software architecture and security best practices.

## Core Features

*   **Professional Portfolio:** A dynamic, multi-project gallery to showcase my work.
*   **Full Blogging Engine:** A complete CRUD admin panel for writing and managing articles, with a public-facing blog.
*   **AI Integration:**
    *   **"The Scribe":** An AI-powered editor in the admin panel to generate excerpts for posts and projects using the Gemini API.
    *   **"Gordon" & "Pagey Boy":** A multi-persona public chatbot for user engagement.
*   **Financial Ledger:** A custom, entity-centric accounting tool to manage rental property and limited company finances, complete with receipt uploads and tax reporting.
*   **Secure by Default:** Features include role-based access control, CSRF protection on all forms, and secure session management.

## Tech Stack & Architecture

This project is built on a professional, multi-server architecture.

### Backend
*   **Language:** Go (Golang)
*   **Web Framework:** Go's native `net/http` library with the Chi router for flexible and performant routing.
*   **Database:** MySQL, hosted on a dedicated, firewalled VPS.
*   **Session Management:** `alexedwards/scs` with a MySQL database store.
*   **AI:** Google's Gemini API via the official Go SDK.
*   **Security:** `bcrypt` for password hashing, `justinas/nosurf` for CSRF protection.

### Frontend
*   **Templating:** Go's native `html/template` package.
*   **Styling:** Plain CSS3 with a mobile-first, responsive design.
*   **JavaScript:** Vanilla JavaScript for interactive UI components (AI Chatbot, Slideshows).

### Deployment
*   **Application Server:** Ubuntu Linux VPS running the compiled Go binary.
*   **Web Server:** Apache2 acting as a secure reverse proxy and handling TLS termination.
*   **SSL:** Free, automated certificates from Let's Encrypt via Certbot.
*   **Version Control:** Git & GitHub.

## Running Locally

1.  **Prerequisites:** Go, MySQL, and an active SSH tunnel to the database server.
2.  **Clone the repository:** `git clone [your-repo-url]`
3.  **Set up the database:** Create the `danpages_db` and run the SQL schemas.
4.  **Configure:** Create a `.env` file in the root and set the `DB_DSN` and `GEMINI_API_KEY` variables.
5.  **Run:** From the root directory, run `go run ./cmd/web`. The application will be available at `http://localhost:9999`.

---
© 2025 Dan Page. All Rights Reserved.
