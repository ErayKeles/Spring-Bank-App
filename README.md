# Spring Bank Application

## Overview
The **Spring Bank Application** is a comprehensive web application designed to manage essential banking operations efficiently. Built with **Spring Boot**, this application provides distinct functionalities based on user roles (Admin, Banker, and Customer), making it versatile for different financial scenarios. The application implements robust user authentication and authorization using **Spring Security**, ensuring data privacy and secure operations.

## Features
### Admin Features
- Add, edit, and delete banker accounts.
- Approve or reject loan applications.

### Banker Features
- Add, edit, and delete customer accounts.
- Manage customer transactions (deposit and withdrawal).

### Customer Features
- Apply for loans and track application statuses.
- Perform deposit and withdrawal transactions.

## Database Structure
The application uses a **MySQL database** with two primary tables:
1. **`kullanici` (User Table)**:
   - Stores user details including:
     - User ID
     - Name
     - Role (Admin, Banker, or Customer)
     - Username
     - Password (hashed for security)
2. **`kredi_basvurusu` (Loan Application Table)**:
   - Tracks loan applications with:
     - Application ID
     - Applicant User ID
     - Loan Amount
     - Application Status

These tables are generated automatically following a **code-first approach** using the application’s model classes.

### Database Screenshots
![User Table](https://github.com/user-attachments/assets/b01c6426-44e7-41ce-906b-4e480eccdffe)
![Loan Application Table](https://github.com/user-attachments/assets/075e02a8-f16f-475d-abce-d5d6a49f96de)

## Project Structure
```
Spring-Bank-App-main
│
├── Bank_WEB_APP
│   ├── pom.xml                              # Maven project configuration
│   ├── src
│   │   ├── main
│   │   │   ├── java/com/example/Eray
│   │   │   │   ├── controller               # Controllers for handling requests
│   │   │   │   ├── model                    # Entity classes
│   │   │   │   ├── repository               # Database repositories
│   │   │   │   ├── service                  # Business logic
│   │   │   │   ├── ErayApplication.java     # Application entry point
│   │   │   └── resources
│   │   │       ├── application.properties   # Application configuration
│   │   │       └── templates                # Thymeleaf templates for UI
│   └── target
│
├── README.md                                # Project documentation
```

## Technologies Used
- **Backend**: Spring Boot, Spring Security
- **Frontend**: Thymeleaf, HTML, CSS
- **Database**: MySQL
- **Build Tool**: Maven
- **Testing**: JUnit

## Installation

### Prerequisites
- **Java JDK 8+**
- **Maven**
- **MySQL**

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/SpringBankApp.git
   cd SpringBankApp/Bank_WEB_APP
   ```

2. Configure the database:
   - Update the `application.properties` file with your MySQL credentials.
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/spring_bank_app
   spring.datasource.username=yourusername
   spring.datasource.password=yourpassword
   ```

3. Build the project:
   ```bash
   mvn clean install
   ```

4. Run the application:
   ```bash
   mvn spring-boot:run
   ```

5. Access the application:
   Open your browser and navigate to `http://localhost:8080`.

## Pages and Their Functions
### Authentication
- **Login Page**: All users log in here and are redirected based on their roles.
![Login Page](https://github.com/user-attachments/assets/8e7ae414-5ffa-429f-a96d-ee210b32337f)

- **Register Page**: Customers can register for the application.
![Register Page](https://github.com/user-attachments/assets/a3e7f385-cfb5-42d2-aef7-538bfcb65291)

### Admin Pages
- **Admin Dashboard**: Access to all admin functionalities.
![Admin Dashboard](https://github.com/user-attachments/assets/e5ac964d-0202-473d-8249-065dd0612652)

- **Banker Management**:
  - Add new bankers.
  ![Add Banker Page](https://github.com/user-attachments/assets/180a8ae9-9447-4bb6-a758-6fc5cc2ba986)
  - View, edit, or delete existing bankers.
  ![Banker List](https://github.com/user-attachments/assets/e271643b-de5e-4921-b20b-dd9a2fa1e60c)
  ![Edit Banker](https://github.com/user-attachments/assets/9207d1f2-b97f-40ce-87cb-58c5a7203d26)

- **Loan Application Management**:
  - Approve or reject loan applications.
  ![Loan Applications](https://github.com/user-attachments/assets/29df31aa-650b-4450-9a82-634bfa99083b)

### Banker Pages
- **Banker Dashboard**: Access to all banker functionalities.
![Banker Dashboard](https://github.com/user-attachments/assets/078e876c-67a6-47b5-bca1-ea6c8bed5cf1)

- **Customer Management**:
  - Add, edit, or delete customers.
  ![Customer List](https://github.com/user-attachments/assets/d37d5170-2b3e-4f61-afb6-fba11215abd0)
  ![Edit Customer](https://github.com/user-attachments/assets/a6115f25-6913-4a9a-b395-9cd3102beaf2)
  - Perform deposit and withdrawal operations.
  ![Deposit Money](https://github.com/user-attachments/assets/cec61817-ce60-4ce4-b4e2-0906c706c8c4)
  ![Withdraw Money](https://github.com/user-attachments/assets/494d2570-b1f6-46fe-a312-567f86a62cc2)

### Customer Pages
- **Customer Dashboard**: View balance, deposit, or withdraw money.
![Customer Dashboard](https://github.com/user-attachments/assets/eb15e5d0-6b58-48f5-8404-f9be1be0a019)

- **Loan Application**:
  - Submit loan applications.
  ![Loan Application](https://github.com/user-attachments/assets/34c1a689-4d46-4b3d-a240-c065a39ef973)
  - Track application status.
  ![Loan Status](https://github.com/user-attachments/assets/fbd1cdbe-e2dc-4fb2-9860-617e672bfe82)

## Contribution
Contributions are welcome! Follow these steps:
1. Fork the repository.
2. Create a new feature branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -m 'Add feature'`
4. Push to the branch: `git push origin feature-name`
5. Submit a pull request.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Contact
For any inquiries or feedback, feel free to reach out:
- **Email**: eraykelesk@gmail.com
- **LinkedIn**: [Eray Keleş](https://linkedin.com/in/eraykeles)

