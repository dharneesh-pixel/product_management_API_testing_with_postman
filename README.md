Here is a **clean, formatted README** based on your uploaded PDF.
If you want, I can also convert this into **Markdown**, **PDF**, **DOCX**, **GitHub-style README**, or **add diagrams**.

---

# 📦 Inventory Management API – README

API Testing with Postman & Newman

---

## 📘 Introduction

The **Inventory Management API** is a RESTful service used to manage toy product inventory.
It supports full **CRUD operations** and is tested using **Postman** with automated scripts, environment variables, schema validations, and Postman Visualizer outputs.

A mock backend (**MockAPI**) simulates real-world API behaviour with structured JSON responses.

---

## 🌐 Base URL

```
https://6925967582b59600d72443bb.mockapi.io/toysdata
```

---

## 🧩 Main Endpoint

**Resource:** `/toy`

### **Fields**

| Field   | Type    | Description                     |
| ------- | ------- | ------------------------------- |
| Prid    | String  | Unique product ID               |
| toyname | String  | Name of the toy                 |
| Stocks  | Boolean | Stock availability (true/false) |
| price   | Number  | Price of the toy                |

---

## 🔄 CRUD Operations

### **1. GET /toy — Retrieve All Products**

Used for:

* Fetching product list
* Stock distribution visualization
* Schema validation

---

### **2. POST /toy — Add New Product**

**Sample Body**

```json
{
  "toyname": "{{toyname}}",
  "price": "{{$randomPrice}}",
  "stock": false
}
```

Uses Postman dynamic variables.

---

### **3. GET /toy/{Prid} — Retrieve Product by ID**

Purpose:

* Validate fields
* Show product card in Visualizer
* Schema checks

---

### **4. PUT /toy/{Prid} — Update Product**

Updates fields:

* toyname
* price
* stock

---

### **5. DELETE /toy/{Prid} — Delete Product**

Confirms deletion with a follow-up GET.

---

## 🛠 Environment Variables

| Variable | Description            |
| -------- | ---------------------- |
| baseURL  | Main API URL           |
| endpoint | Resource name (`toy`)  |
| Prid     | Auto-stored product ID |
| toyName  | Dynamic product name   |
| Stocks   | Stock value            |

---

## 🏗 API Architecture

### **RESTful Features**

* Client–server model
* Stateless requests
* JSON-based data flow
* Resource-based URIs: `/toy/{prid}`
* Standard HTTP verbs: GET, POST, PUT, DELETE

### **Sample Response**

```json
{
  "toyname": "car",
  "Stocks": true,
  "Prid": "45"
}
```

### **MockAPI Benefits**

* Auto-generated IDs
* Cloud database
* Consistent structure
* Realistic API simulation

---

## 🚀 Newman Integration (Automation)

Newman allows running the Postman collection via CLI.

### **Commands**

Run collection:

```
newman run Inventory_management.postman_collection.json
```

Run with CSV data:

```
newman run Inventory_management.postman_collection.json -d data.csv
```

Run with HTML Extra report:

```
newman run Inventory_management.postman_collection.json -d data.csv -r htmlextra
```

Generates professional HTML test reports for CI/CD workflows.

---

## 🖼 Screenshots (From PDF)

* Basic Auth configuration
* Newman run with CSV
* Newman run with JSON

---

## 🏁 Conclusion

This project demonstrates complete API lifecycle testing using:

* Postman
* Automated test scripts
* Schema validation
* MockAPI backend
* Newman CLI
* HTML Extra Reporting

It serves as a strong foundation for real-world API testing and CI/CD automation.

---

If you want, I can generate:

✅ **A perfect GitHub README.md file**
✅ **A DOCX or PDF version**
✅ **Add diagrams (API flow, architecture, sequence)**
✅ **Create Postman test scripts for each request**

Just tell me what you need!
