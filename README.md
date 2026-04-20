# Hibernate CRUD Operations

## 📌 Project Overview

This project demonstrates basic **CRUD (Create, Read, Update, Delete)** operations using **Hibernate ORM** in Java. It is designed to help beginners understand how Hibernate interacts with a relational database and how to perform database operations efficiently.

---

## 🚀 Features

* Create (Insert) new records
* Read (Fetch) records from database
* Update existing records
* Delete records
* Hibernate configuration using XML
* Simple and clean project structure

---

## 🛠️ Technologies Used

* Java
* Hibernate ORM
* MySQL (or any relational database)
* Maven (if used)

---

## 📂 Project Structure

```
Hibernate_CRUD_Operations
│── src/main/java
│   ├── entity
│   │   └── (Entity classes)
│   ├── dao
│   │   └── (CRUD operations logic)
│   └── util
│       └── HibernateUtil.java
│
│── src/main/resources
│   └── hibernate.cfg.xml
│
│── pom.xml (if Maven project)
```

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/ramyahp19/HIbernate_CRUD_Operations.git
cd HIbernate_CRUD_Operations
```

### 2. Configure Database

Update your database credentials in `hibernate.cfg.xml`:

```xml
<property name="hibernate.connection.url">jdbc:mysql://localhost:3306/your_db</property>
<property name="hibernate.connection.username">root</property>
<property name="hibernate.connection.password">password</property>
```

### 3. Build and Run

* If Maven project:

```bash
mvn clean install
```

* Run the main class from your IDE

---

## 📖 CRUD Operations Explained

### ➤ Create

Insert new data into the database using Hibernate `save()` method.

### ➤ Read

Fetch records using `get()` or `load()` methods.

### ➤ Update

Modify existing records using `update()` method.

### ➤ Delete

Remove records using `delete()` method.

---

## 💡 Example Code

```java
Session session = sessionFactory.openSession();
Transaction tx = session.beginTransaction();

Employee emp = new Employee();
emp.setName("John");
emp.setSalary(50000);

session.save(emp);

tx.commit();
session.close();
```

---

## 📸 Output

* Successfully performs CRUD operations
* Data stored and retrieved from database

---
