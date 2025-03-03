# Banking System Application

## Overview
This is a simple banking system application developed in Java. It allows users to register, log in, open a bank account, and perform various banking operations such as depositing money, withdrawing money, transferring funds, and checking account balances.

---

## Features
- **User Registration**
- **User Login**
- **Open a New Bank Account**
- **Deposit Money**
- **Withdraw Money**
- **Transfer Funds**
- **Check Account Balance**
- **Secure Transactions with PIN Authentication**

---

## Setup Instructions

### Clone the Repository
```sh
git clone https://github.com/harshhsaini/banking-system.git
cd banking-system
```

---

## Database Setup

1. **Install PostgreSQL** and create a database named `bank_db`:
   ```sql
   CREATE DATABASE bank_db;
   ```

2. **Create the `accounts` table** with the following schema:
   ```sql
   CREATE TABLE accounts (
       account_number BIGINT PRIMARY KEY,
       email VARCHAR(255) UNIQUE NOT NULL,
       balance DOUBLE PRECISION DEFAULT 0,
       security_pin VARCHAR(255) NOT NULL
   );
   ```

---

## Configure and Run

### 1. Configure Database Connection
- Update the database connection details in `src/BankingApp.java`:
   ```java
   private static final String URL = "jdbc:postgresql://localhost:5432/bank_db";
   private static final String USERNAME = "postgres";
   private static final String PASSWORD = "your_password";
   ```

### 2. Build and Run the Application
- Open the project in IntelliJ IDEA or any Java IDE.
- Build the project.
- Run the `main` method in `src/BankingApp.java`.

---

## Usage

### 1. Register
- Select the **"Register"** option.
- Provide your email and a secure PIN to create an account.

### 2. Login
- Select the **"Login"** option.
- Enter your email and PIN to authenticate.

### 3. Open a Bank Account
- If you don’t have a bank account, you will be prompted to create one after logging in.

### 4. Banking Operations
Once logged in, you can perform the following operations:

- **Deposit Money:** Add funds to your account.
- **Withdraw Money:** Deduct money from your account.
- **Transfer Funds:** Transfer money to another account securely.
- **Check Balance:** View your current account balance.

### 5. Logout
- Select the **"Log Out"** option to safely exit the system.

---
