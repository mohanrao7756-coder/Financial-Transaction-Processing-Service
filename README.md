# Financial-Transaction-Processing-Service

Project Overview

The Financial Transaction Processing Service is a production-style Spring Boot backend application that simulates a banking/payment gateway transaction system.

The system supports:

1.Account management
2.Debit/Credit operations
3.Money transfer between accounts
4.Fraud validation
5.Transaction history
6.Audit logging
7.Idempotent transaction handling
8.Transactional consistency
9.Pagination and filtering
10.Retry mechanism
11.Scheduler jobs
12.Swagger API documentation

This project demonstrates real-world backend architecture and enterprise-level Spring Boot concepts.

Controller Layer
↓
Service Layer
↓
Repository Layer
↓
MySQL Database

src/main/java/com/example/finance

├── audit
├── config
├── controller
├── dto
├── entity
├── exception
├── fraud
├── repository
├── scheduler
├── service
│   └── impl
├── util
└── FinanceApplication.java

Features Implemented
 Account Management
  Create account
  Fetch account details
  Balance tracking
 Transactions
  Debit money
  Credit money
  Transfer money
  Transaction status tracking
 Fraud Detection
  Maximum transaction amount validation
 Audit Logging
  Audit records for successful operations
 Transactional Integrity
  Uses @Transactional
  Rollback support
 Idempotency
  Prevents duplicate transactions using unique request keys
 Pagination
  Transaction history pagination support
 Optimistic Locking
  Prevents concurrent update conflicts using @Version
 Retry Mechanism
  Retry failed transaction processing automatically
 Scheduler
  Daily reconciliation job
 Swagger Documentation
  Interactive API documentation

API Endpoints
Account APIs
 Create Account
 Get Account

Transaction APIs
 Debit Money
 Credit Money
 Transfer Money
 Get Transaction
 Transaction History

Business Rules
 Account balance should never become negative
 Duplicate transaction requests are blocked
 Fraud rules are validated before processing
 Successful transactions are logged
 Transactions use UUID identifiers
 Failed transactions are rolled back automatically

Exception Handling

Global exception handling implemented using:
Handles:

Validation errors
Insufficient balance
Account not found
Duplicate transaction requests
Fraud validation failures

Author

Mohan Rao

Java Backend Developer.

 
 




