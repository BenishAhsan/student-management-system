# Student Management System

A React.js web application for managing student records with full CRUD functionality, client-side routing, and browser-based data persistence.

---

## Tech Stack

- **React.js** (Create React App)
- **React Router v6** for navigation
- **Bootstrap 5** for UI styling
- **LocalStorage** for data persistence

---

## Features

- Add, edit, and delete student records
- View all students in a dynamic list
- Form validation with inline error messages
- Data persists across browser sessions via LocalStorage
- Responsive layout using Bootstrap
- 404 page for undefined routes

---

## Project Structure

```
src/
├── components/       # Reusable UI components (Form, StudentCard, Navbar, etc.)
├── pages/            # Route-level screens (Home, StudentList, AddStudent, NotFound)
├── utils/            # Helper functions (storage.js for LocalStorage operations)
├── App.js            # Route configuration
└── index.js          # App entry point
```

---

## Routes

| Path | Page | Description |
|------|------|-------------|
| `/` | Home | Landing page with summary |
| `/students` | Student List | View, edit, and delete records |
| `/add` | Add Student | Form to add a new student |
| `*` | 404 | Catch-all for undefined routes |

---

## Getting Started

### Prerequisites

- Node.js v14 or above
- npm

### Installation

```bash
git clone https://github.com/your-username/student-management-system.git
cd student-management-system
npm install
npm start
```

The app runs at `http://localhost:3000`.

---

## State Management

- `useState` manages form inputs and the student records array
- `useEffect` loads data from LocalStorage on initial render and syncs on every update
- Props are passed between parent pages and child components for shared state

---

## Data Persistence

All student records are stored in the browser's LocalStorage under the key `students`. No backend or database is required. Data survives page refreshes and browser restarts.

---

## Design Notes

This project follows an MVC-inspired structure adapted for React:

- **Model** — LocalStorage acts as the data layer; `utils/storage.js` handles all read/write operations
- **View** — Components in `components/` and `pages/` render the UI
- **Controller** — Event handlers and state logic inside page-level components coordinate data flow

---
