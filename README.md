no# Hotel_Management_System

*Subject Name*: Advanced Java  
*Subject Code*: BCS613D  
*Name*: Sowmya Shetty  
*USN*: 4AL22CS160  
*Sem/Section*: VI/C  

---
A comprehensive web application for managing hotel reservations built with JSP, Servlets, and MySQL following MVC architecture principles.

## 🚀 Features

- *Complete CRUD Operations*: Add, Update, Delete, and Display hotel booking records
- *Advanced Search*: Search bookings by Customer ID
- *Comprehensive Reports*: Generate various reports including:
  - Current active bookings
  - Bookings by room type
  - High-paying customers
- *Input Validation*: Client-side and server-side validation
- *Professional UI*: Bootstrap-based responsive design
- *MVC Architecture*: Clean separation of concerns
- *Database Integration*: MySQL with JDBC connectivity

## 📋 Prerequisites

Before running this application, make sure you have the following installed:

- *Java Development Kit (JDK) 8 or higher*
- *Apache Tomcat 9.0 or higher*
- *MySQL Server 5.7 or XAMPP Server*
- *MySQL JDBC Driver (mysql-connector-java)*
- *IDE*: Eclipse (J2EE), IntelliJ IDEA, or any Java IDE
- *Web Browser*: Chrome, Firefox, or Edge

## 🛠 Project Structure

HotelWebApp/  
├── WebContent/  
│   ├── index.jsp  
│   ├── reservationadd.jsp  
│   ├── reservationupdate.jsp  
│   ├── reservationdelete.jsp  
│   ├── reservationdisplay.jsp  
│   ├── reports.jsp  
│   ├── report_form.jsp  
│   └── report_result.jsp  
├── src/  
│   └── com/  
│       ├── dao/  
│       │   └── ReservationDAO.java  
│       ├── model/  
│       │   └── Reservation.java  
│       └── servlet/  
│           ├── AddReservationServlet.java  
│           ├── UpdateReservationServlet.java  
│           ├── DeleteReservationServlet.java  
│           ├── DisplayReservationsServlet.java  
│           ├── ReportServlet.java  
│           └── ReportCriteriaServlet.java  
├── WEB-INF/  
│   └── web.xml  

## 🗄 Database Setup

### 1. Create Database

```sql
CREATE DATABASE IF NOT EXISTS hotel_management;
USE hotel_management;
```

### 2. Create Table

```sql
CREATE TABLE IF NOT EXISTS Booking (
    BookingID INT PRIMARY KEY,
    CustomerName VARCHAR(100),
    RoomType VARCHAR(50),
    CheckInDate DATE,
    CheckOutDate DATE,
    TotalAmount DECIMAL(10, 2)
);
```

### 3. Insert Sample Data

```sql
INSERT INTO Booking VALUES
(2, 'Sowmya Shetty', '202', '2025-05-29', '2025-05-29', 1500.00),
(3, 'Harshitha Shetty', '111', '2025-04-01', '2025-04-03', 1000.00),
(5, 'Sadanand', '300', '2025-04-25', '2025-04-29', 2200.00),
(8, 'Sowmya Shetty', '200', '2025-05-15', '2025-05-30', 500.00);
```

## ⚙ Installation & Setup

### Step 1: Clone/Download the Project
Download all the project files and organize them according to the project structure above.

### Step 2: Database Configuration
1. Start your MySQL server  
2. Run the database setup scripts provided above  
3. Update database credentials in `ReservationDAO.java`:

```java
connection = DriverManager.getConnection(
    "jdbc:mysql://localhost:3306/hotel_management", 
    "your_username", 
    "your_password");
```

### Step 3: Add MySQL JDBC Driver
1. Download MySQL Connector/J from the official MySQL website  
2. Add the JAR file to your project's `WEB-INF/lib` directory  
3. If using an IDE, add it to your build path

### Step 4: Deploy to Tomcat
1. Create a new Dynamic Web Project in your IDE  
2. Copy all source files to the appropriate folders  
3. Deploy the project to Tomcat server  
4. Start the Tomcat server

### Step 5: Access the Application
Open your web browser and navigate to:

```
http://localhost:8080/HotelWebApp/
```

## 🖼 Screenshots

Add screenshots in the `/screenshots` directory and link here:

Screenshots
### 🏠Home Page
  <img src="https://github.com/14SowmyaShetty23/Hotel_Management_System/blob/main/HotelWebApp1/Demo_Screenshots/Homepage.jpg" alt="Home Page" width="700"/>
  
- Add Reservation Page  
- Search Reservation  
- Delete Reservation  
- Update Reservation  
- Display Reservation  

## 🎯 Usage Application

### Adding Reservation
- Go to "Add Reservation"
- Fill:
  - Booking ID (unique)
  - Customer Name
  - Room Type (Deluxe, Suite, etc.)
  - Check-In and Check-Out Dates
  - Total Amount
- Submit form

### Updating Reservation
- Go to "Update Reservation"
- Search by Booking ID
- Update any fields
- Submit

### Deleting Reservation
- Go to "Delete Reservation"
- Enter Booking ID
- Confirm and delete

### Displaying Reservation
- View all reservations
- Search by Booking ID
- Edit/Delete options

### Generating Reports
- Go to "Generate Reports"
- Choose filter (room type, date range, etc.)
- Generate and print

## 🔧 Technical Features

### Input Validation
- JavaScript + Bootstrap
- Server-side validation
- NOT NULL & PK constraints in DB

### Error Handling
- Try-catch for DB
- Graceful failovers

### Security Features
- Prepared statements
- Input checks
- Session handling

### Responsive Design
- Bootstrap 5.3
- Adaptive layout
- Print-ready reports

## 🧪 Testing the Application

### Test Scenarios

1. Add: Valid booking, duplicate ID, invalid date  
2. Update: Modify existing booking, non-existent ID  
3. Delete: Remove booking, handle missing ID  
4. Display: View all, search by ID  
5. Reports: All filters, correctness of values  

## 🎓 Outcomes

This project demonstrates:
- Full-stack web development with JSP & Servlets  
- MVC architecture  
- MySQL integration with JDBC  
- CRUD and reporting logic  
- Form validation  
- Clean and responsive UI  
