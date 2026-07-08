# Student Management System

A React.js web application for managing student records with full CRUD functionality, client-side routing, and browser-based data persistence.

---

## Tech Stack

- **React.js** (Create React App)
- **React Router DOM v6** for navigation
- **Bootstrap** for UI styling and responsiveness
- **LocalStorage** for data persistence

---

## Features

- Add, edit, and delete student records
- View all students in a card-based list
- Form validation with inline error messages
- Data persists across browser sessions via LocalStorage
- Fully responsive layout using Bootstrap
- 404 page for undefined routes

---

## Project Structure

```
src/
├── components/       # Reusable UI components (StudentCard, Navigation, Button, FormGroup)
├── pages/            # Route-level screens (Home, AddStudent, EditStudent, NotFound)
├── utils/            # Helper functions (localStorage.js for read/write operations)
├── App.js            # Route configuration
├── index.js          # App entry point
└── index.css         # Global styles
```

---

## Routes

| Path | Page | Description |
|------|------|-------------|
| `/` | Home | Lists all students in card format |
| `/add` | Add Student | Form to add a new student |
| `/edit/:id` | Edit Student | Edit an existing student record |
| `*` | Not Found | 404 page for invalid routes |

---

## Getting Started

### Prerequisites

- Node.js v14 or above
- npm

### Installation

```bash
git clone https://github.com/BenishAhsan/student-management-system.git
cd student-management-system
npm install
npm start
```

The app runs at `http://localhost:3000`.

---

## State Management

- `useState` manages form inputs and the student records array
- `useEffect` loads data from LocalStorage on initial render and syncs on every update
- Props passed between parent pages and child components for shared state

---

## Data Persistence

All student records are stored in the browser's LocalStorage. No backend or database required. Data survives page refreshes and browser restarts.

---

## Design Notes (MVC Mapping)

This project follows an MVC-inspired structure adapted for React:

- **Model** — LocalStorage is the data layer; `utils/localStorage.js` handles all read/write operations
- **View** — Components in `components/` and `pages/` render the UI
- **Controller** — Event handlers and state logic in page-level components coordinate data flow between model and view

---

## Author

Binash Ahsan, Information Technology University, Lahore
