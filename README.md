# 📚 Quiz App – Spring Boot + PostgreSQL + Lombok

A simple backend quiz management system built using **Spring Boot**, **PostgreSQL**, and **Lombok**. The app allows users to create quizzes based on categories, retrieve quiz questions, and more.

## 🚀 Features

* Create quizzes dynamically based on category and question count
* Retrieve quiz questions by quiz ID
* Uses DTOs (like `QuestionWrapper`) to expose only necessary data
* Clean structure using Service & Controller layers
* Simplified code with Lombok annotations
* Connected to PostgreSQL for persistent storage

## 🛠️ Tech Stack

* **Spring Boot**
* **Spring Data JPA**
* **PostgreSQL**
* **Lombok**
* **Maven**

## 📦 Project Structure

```
com.kumod.quizapp
│
├── controller         → REST Controllers (QuizController, etc.)
├── model              → Entity and DTO classes (Question, Quiz, QuestionWrapper)
├── repository         → Spring Data JPA Repositories
├── service            → Business logic services (QuizService)
└── QuizAppApplication.java
```

## 🧾 Requirements

* Java 17+
* Maven
* PostgreSQL database
* IDE (e.g., IntelliJ, VS Code)

## ⚙️ Setup Instructions

1. **Clone the Repository**

   ```bash
   git clone https://github.com/kumodN/Simple-QuizzApp-API.git
   cd quiz-app
   ```

2. **Configure PostgreSQL**
   Create a database named `quizdb` in PostgreSQL and update your `application.properties`:

   ```properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/quizdb
   spring.datasource.username=your_username
   spring.datasource.password=your_password
   spring.jpa.hibernate.ddl-auto=update
   spring.jpa.show-sql=true
   ```

3. **Run the App**

   ```bash
   mvn spring-boot:run
   ```

## 📮 API Endpoints

### Create a Quiz

```
POST /quiz/create?category=Java&numQ=5&title=Java Basics
```

### Get Quiz Questions by ID

```
GET /quiz/get/{id}
```

## ✅ Lombok Setup

If using an IDE like IntelliJ or Eclipse, make sure you enable annotation processing to use Lombok:

* **IntelliJ**: Preferences → Build, Execution, Deployment → Compiler → Annotation Processors → Enable
* **Eclipse**: Install Lombok plugin

## 📌 To-Do (Future Features)

* Submit and evaluate quiz answers
* Authentication and user roles
* Frontend (React/Angular) integration
* Timer and scoring system

## 🧑‍💻 Author

**Kumod De Silva**
[LinkedIn](https://www.linkedin.com/in/kumod-de-silva) | [Email](mailto:kumodnenuk@gmail.com)

