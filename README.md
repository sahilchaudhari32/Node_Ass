# 📚 Node.js Student API

A RESTful API built with **Node.js** and **Express.js** that serves student data with various query endpoints. This project demonstrates core backend development concepts including REST API design, routing, and data filtering.

---

## 🚀 Tech Stack

| Technology | Purpose |
|------------|---------|
| Node.js | Runtime environment |
| Express.js v5 | Web framework |
| CORS | Cross-origin resource sharing |
| Nodemon | Development auto-restart |

---

## 📁 Project Structure

```
Node_Ass/
└── server-1/
    ├── index.js          # Main server with all API routes
    ├── package.json      # Project dependencies
    └── .gitignore        # Git ignore rules
```

---

## ⚙️ Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/) (v14 or higher)
- npm

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/sahilchaudhari32/Node_Ass.git

# 2. Navigate into the project folder
cd Node_Ass/server-1

# 3. Install dependencies
npm install

# 4. Start the development server
npx nodemon index.js
```

The server will start on **http://localhost:3000**

---

## 🔌 API Endpoints

Base URL: `http://localhost:3000`

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/students` | Get all students |
| GET | `/students/count` | Get total number of students |
| GET | `/students/topper` | Get the student with the highest CGPA |
| GET | `/students/average` | Get the average CGPA of all students |
| GET | `/students/:id` | Get a student by their ID |
| GET | `/students/branch/:branchName` | Get all students from a specific branch |

---

## 📋 Sample Responses

### `GET /students`
```json
[
  { "id": 1, "name": "Aarav Sharma", "branch": "CSE", "semester": 8, "cgpa": 9.3 },
  { "id": 2, "name": "Ishita Verma",  "branch": "IT",  "semester": 7, "cgpa": 8.9 }
]
```

### `GET /students/topper`
```json
{ "id": 1, "name": "Aarav Sharma", "branch": "CSE", "semester": 8, "cgpa": 9.3 }
```

### `GET /students/average`
```json
{ "averageCGPA": 8.61 }
```

### `GET /students/count`
```json
{ "totalStudents": 10 }
```

### `GET /students/3`
```json
{ "id": 3, "name": "Rohan Kulkarni", "branch": "ECE", "semester": 6, "cgpa": 8.4 }
```

### `GET /students/branch/cse`
```json
[
  { "id": 1, "name": "Aarav Sharma", "branch": "CSE", "semester": 8, "cgpa": 9.3 },
  { "id": 4, "name": "Meera Iyer",   "branch": "CSE", "semester": 8, "cgpa": 9.1 }
]
```

---

## 🎓 Student Data

The API includes 10 pre-seeded students across the following branches:

- **CSE** – Computer Science Engineering
- **IT** – Information Technology
- **ECE** – Electronics & Communication Engineering
- **AI** – Artificial Intelligence
- **Data Science**

---

## 📦 Dependencies

```json
{
  "express": "^5.2.1",
  "cors": "^2.8.6",
  "nodemon": "^3.1.14"
}
```

---

## 👨‍💻 Author

**Sahil Chaudhari**  
GitHub: [@sahilchaudhari32](https://github.com/sahilchaudhari32)

---

## 📄 License

This project is licensed under the **ISC License**.
