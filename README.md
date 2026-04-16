# Fake Store API Testing – E-commerce Flows

**Postman Collection** for testing a RESTful e-commerce API.

This is my practical project created while preparing for the **Junior QA Engineer (Serverless Core)** position at **GymBeam**.

---

## 🎯 Project Goal

To build a comprehensive Postman collection that covers key e-commerce scenarios, including:

- Product management
- User operations
- Shopping cart functionality
- Positive and negative test scenarios
- Data consistency verification
- Simulation of regression testing in user flows

---

## 🛠 Tools Used

- **Postman** – main testing tool
- **Newman** – command-line collection runner
- JavaScript (for assertions and tests)
- Environments & Variables

---

## 📁 Collection Structure

- **Products** – CRUD operations, category filtering, negative cases
- **Users** – retrieving and creating users
- **Carts** – adding items to cart, viewing cart content
- **Negative Tests** – testing invalid data and non-existent resources
- **Full E-commerce Flows** – simulation of complete user journey (Add to cart → Cart verification)

---

## ✅ What Was Tested

### Positive Scenarios
- Retrieving all products and single product details
- Getting product categories and filtering by category
- Creating a new user
- Adding products to the shopping cart
- Retrieving cart contents

### Negative Scenarios
- Requesting non-existent product (`/products/99999`, `/products/abc`)
- Creating user without required fields
- Sending invalid data to cart endpoint

### Regression & Data Consistency
- Simulated e-commerce flow: **Add to Cart → Verify Cart Contents**
- Checked that added items appear correctly in the cart
- Analyzed data persistence behavior of the mock API

---

## Fake Store API Specifics

This is a **mock API**, therefore:
- POST requests return `201 Created`, but data is **not persisted**
- Requesting non-existent resources often returns `200 OK` with an empty array instead of `404 Not Found`
- These behaviors were documented and taken into account during testing

---

## How to Run the Collection

### 1. In Postman
1. Import the file `Fake-Store-API-Testing.postman_collection.json`
2. Open the collection and click **Run collection**

