# 📝 Todo Full Stack Application

This is a **full stack Todo application** built with **React**, **Node.js**, **Express**, and **MySQL**. It allows users to register, log in, add tasks, mark them as complete, and delete tasks — all while persisting data securely on the backend.

---

## 🚀 Features

- ✅ **User Authentication**  
  Secure signup and login functionality with unique email validation and error handling.

- 🗂️ **Task Management**  
  Users can add new tasks, categorize them as "Pending" or "Completed", and delete them with real-time UI updates.

- 🧠 **Form Validation with Feedback**  
  Client-side validation for email format, empty inputs, and other user-friendly error prompts.

- 🔄 **Live Task Filtering**  
  Tasks are filtered automatically into Pending and Completed sections without page reload.

- 🧩 **Redux Integration**  
  Manages state efficiently for tasks and user sessions, ensuring smooth UI interaction and task updates.

- 🔐 **Secure API Structure**  
  Express routes and REST API architecture for clean backend handling with MySQL queries.

---

## 🎨 Responsive Design

This app has been built with **mobile-first responsiveness** using **Tailwind CSS**. The UI adjusts dynamically based on the device size to ensure optimal experience on:

- 📱 Mobile Phones  
- 💻 Tablets & Laptops  
- 🖥️ Desktop Monitors  

Components like input fields, buttons, task cards, and layout sections are styled with flexibility and accessibility in mind.

---

## 🧱 Tech Stack

**Frontend:**
- React
- Redux
- Tailwind CSS

**Backend:**
- Node.js
- Express
- MySQL
- CORS
- dotenv

---

## ⚙️ Installation & Setup

### 1. Clone the repository
```
git clone https://github.com/Sivakumar1003/Todo-Full-Stack-Application.git
cd Todo-Full-Stack-Application
```

### 2. Setup MySQL Database
- Create a database named `todo_db`.
- Run the SQL script inside `database/todo_db.sql` to create tables.
- Ensure foreign key constraint handles cascading delete:
  ```sql
  CONSTRAINT `fk_tasks_1` FOREIGN KEY (`userId`) REFERENCES `users` (`id`) ON DELETE CASCADE
  ```

### 3. Setup Backend
```
cd backend
npm install
npm start
```
Add a `.env` file:
```
PORT=5000
DB_HOST=localhost
DB_USER=your_mysql_user
DB_PASSWORD=your_mysql_password
DB_NAME=todo_db
```

### 4. Setup Frontend
```
cd ../frontend
npm install
npm run dev
```
Add a `.env` file:
```
VITE_TODO_API=http://localhost:5000
```

---

## 📦 API Endpoints

| Method | Endpoint                     | Description              |
|--------|------------------------------|--------------------------|
| POST   | `/users/Signup`              | Create new user          |
| POST   | `/users/Login`               | Authenticate user        |
| GET    | `/tasks/:userId`             | Get all tasks by user ID |
| POST   | `/tasks/add/:userId/:tasks`  | Add task for user        |
| PATCH  | `/tasks/update/:id`          | Update task status       |
| DELETE | `/tasks/delete/:id`          | Delete a task            |

---

## 🔮 Future Enhancements

- 🌍 **User Session Persistence**  
  Add JWT or cookie-based authentication so users stay logged in across sessions and page refreshes.

- 📅 **Due Dates & Reminders**  
  Let users assign due dates to tasks and enable reminder notifications or highlight overdue tasks.

- 🔍 **Task Search & Filters**  
  Add search functionality and filters like "Today", "This Week", and "Overdue" for better task management.

- 📱 **Mobile App Version**  
  Extend the project to React Native or Flutter for dedicated Android/iOS app experience.

- 📈 **Task Analytics Dashboard**  
  Track number of tasks completed per week, visualize stats, and improve productivity insights.

---

## 📸 Screenshots

![alt text](<project images/Screenshot from 2025-04-10 21-46-41.png>)

![alt text](<project images/Screenshot from 2025-04-10 21-46-51.png>)

![alt text](<project images/Screenshot from 2025-04-10 21-50-15.png>)

---

## ✍️ Author

Made with ❤️ by [Poorna Teja P]