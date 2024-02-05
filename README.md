# Backend Engineer Code Assessment

## Introduction
Welcome to the Backend Engineer Code Assessment project! This project involves enhancing a Spring Boot Application developed in Java 21, leveraging the Temporal Workflow Engine for business logic orchestration. Your primary task is to integrate the Stripe payment processing service to manage customer data during user signup.

## Project Overview
### Base Application
The project provides a Spring Boot Application setup with Java 21.

### External Service
The Temporal Workflow Engine is employed to handle workflow tasks.

## Project Setup
### Prerequisites
Ensure the following are installed on your system:
- Java 21 or later
- Temporal
- Docker
- Stripe API Keys

### Setup Instructions
1. **Java 21 Installation (macOS):**
    ```bash
    brew install --cask zulu21
    ```

2. **Temporal Installation:**
    ```bash
    brew install temporal
    ```

3. **Docker Installation:**
    ```bash
    brew install docker
    ```

4. **Stripe API Keys:**
   - Sign up for a Stripe account.
   - Add your secret key to `application.properties`:
        ```properties
        stripe.api-key=sk_test_51J3j
        ```

### Running the Application
1. **Start Temporal Server:**
    ```bash
    temporal server start-dev
    ```

2. **Run the Application:**
    ```bash
    ./gradlew bootRun
    ```

### Other Commands
- **Lint Checks:**
    ```bash
    ./gradlew sonarlintMain
    ```

- **Code Formatting:**
    ```bash
    ./gradlew spotlessApply
    ```

## Implementation
Follow these tasks to complete the project:

1. **Stripe Integration for Customer Creation:**
   - Integrate Stripe Create Customer API on new user signup.
   - Use provided Stripe SDK and integrate it into Temporal workflow.

2. **API Enhancements:**
   - Add `providerType` (enum type: stripe) and `providerId` fields to the user model.
   - Update the application controller to handle these fields during user signup.

3. **API Implementation:**
   - A `GET /accounts` endpoint is implemented. Use it to verify integration and functionality.