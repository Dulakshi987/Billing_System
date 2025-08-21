# CRM_PahanaEdu

Book Shop Web System that allows cashiers to generate customer bills and admins to manage users, items, customers, and view generated bills.

## 1. Features

### 1.1 Admin Features
- **Admin Login** (Username: `Admin` / Password: `Admin12345`)
- Register and manage Users (Admin or Cashier)
- Add and manage Customers (Prevents duplicate Account Number for different customers)
- Add and manage Items (Prevents duplicate Item Code for different items)
- View generated bills
- Help Section for new Admin
- HttpSession and usertype validation

### 1.2 Cashier Features
- Cashier Login
- Generate Bill with customer accounts and bill items
- View generated Bill
- Help section for new cashier
- HttpSession and usertype validation

## 2. Installation

To run this locally, you need the following requirements:

### 2.1 Software Requirements
- **Apache Tomcat** - Download and install on your computer
- **XAMPP** - Download and install for database connection
- **IntelliJ IDEA Ultimate** - IDE for running this program

### 2.2 Running the Project

1. **Setup Project**
   - Download this project and open in IntelliJ IDEA as a Maven project
   
2. **Configure Tomcat**
   - Click "Current File" on the top navbar in the IDE
   - Select "Edit Configurations"
   - Press the "+" icon and select "Tomcat Server" → "Local"
   - Add a suitable name and change the port to `8086` (or any other available port)
   
3. **Configure Deployment**
   - Go to the "Deployment" tab
   - Press "+" and select "Artifact"
   - Select the "Exploded" option (like: `/billsystem_war_exploded`)
   - Press "Apply" and "OK"

4. **Setup Database**
   - Open XAMPP and start the database service
   - Create a database named `bill_system`
   - Import the database tables located in the `resources` folder of the project directory

5. **Run the Application**
   - Go back to IntelliJ IDEA
   - Run the project by clicking the Tomcat configuration

### 2.3 Dependencies

If you encounter any dependency errors, copy the following dependencies to your project's `pom.xml` file and reload Maven:

```xml
<dependencies>
    <dependency>
        <groupId>javax.servlet</groupId>
        <artifactId>javax.servlet-api</artifactId>
        <version>4.0.1</version>
        <scope>provided</scope>
    </dependency>
    
    <dependency>
        <groupId>mysql</groupId>
        <artifactId>mysql-connector-java</artifactId>
        <version>8.0.33</version> 
    </dependency>
    
    <dependency>
        <groupId>com.sun.mail</groupId>
        <artifactId>jakarta.mail</artifactId>
        <version>2.0.1</version>
    </dependency>
    
    <dependency>
        <groupId>org.junit.jupiter</groupId>
        <artifactId>junit-jupiter</artifactId>
        <version>5.9.3</version>
        <scope>test</scope>
    </dependency>
    
    <dependency>
        <groupId>org.mockito</groupId>
        <artifactId>mockito-core</artifactId>
        <version>5.2.0</version>
        <scope>test</scope>
    </dependency>
</dependencies>
```



