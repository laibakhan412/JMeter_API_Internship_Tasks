# JMeter_API_Internship_Tasks ⚙️📊

This repository contains JMeter Test Plans created as part of my QA internship training. The tasks cover REST API testing using Apache JMeter, demonstrating CRUD operations, data chaining, and parameterization using CSV files.

---

## 📚 Assignment Overview

This repository addresses **Assignment No. 2: JMeter**, which includes the following tasks:

### ✅ Task 1: Basic CRUD Test Plan
- Create a JMeter Test Plan with:
  - **Thread Group**
  - **HTTP Samplers** for GET, POST, PUT, and DELETE
  - At least **two Listeners** (e.g., View Results Tree, Summary Report)
- Objective: Demonstrate all major HTTP methods in API testing using JMeter.

### ✅ Task 2: Full API Workflow (Create → Read → Update → Delete)
- **Create Data** using POST request  
- **Retrieve Data** using GET request  
- **Update Data** using PATCH request  
- **Delete Data** using DELETE request  
- **Verify Deletion** by sending GET request again (should return empty/null)

### ✅ Task 3: Parameterization using CSV
- Read data from an external **CSV file**
- Use the data in **POST** request
- **GET** the same data and verify the response matches the CSV content

---

## 📁 Repository Structure

```

📦 JMeter\_API\_Internship\_Tasks/
┣ 📄 Q1\_TestPlan.jmx              → Task 1: Basic CRUD operations
┣ 📄 Q2\_ChainRequest.jmx          → Task 2: Full API workflow with chaining
┣ 📄 Q3\_CSV\_Data\_TestPlan.jmx     → Task 3: Data-driven test with CSV
┣ 📄 users.csv                    → CSV file used in Task 3
┗ 📄 README.md                    → Project documentation

```

---

## 🛠️ Tools & Technologies Used

- **Apache JMeter** – Performance and API testing tool
- **HTTP Request Sampler** – Used for sending API calls
- **Listeners** – For result visualization (View Results Tree, Summary Report)
- **CSV Data Set Config** – For reading data from `users.csv` in Task 3
- **JSON Path Extractor** – To parse response data
- **Assertions** – For verifying API response content

---

## ▶️ How to Run the Test Plans

This project includes 3 JMeter test plans. Follow the specific steps below for each.

---

### 🧪 Q1: Basic CRUD Test Plan (No setup required)

1. Open **JMeter**
2. Go to `File → Open → Select Q1_TestPlan.jmx`
3. Click the green ▶️ **Start** button to run
4. View results using:
   - **View Results Tree**
   - **Summary Report**

---

### ⚙️ Q2: Full API Workflow (Requires JSON Server)

This test simulates Create → Read → Update → Delete flow and **needs a local JSON API**.

#### ✅ Step 1: Install JSON Server

Open **Command Prompt** or **Terminal** and run:

```bash
npm install -g json-server
````

---

#### ✅ Step 2: Create a Local `db.json`

1. Create a folder (e.g., `C:\JMeter_JSON_Server_Test`)
2. Inside it, create a file named `db.json`
3. Paste this into the file:

```json
{
  "users": []
}
```

---

#### ✅ Step 3: Start JSON Server

In your terminal:

```bash
cd C:\JMeter_JSON_Server_Test
json-server --watch db.json --port 3000
```

> You should see:
> `Resources: http://localhost:3000/users`

---

#### ✅ Step 4: Run Q2 Test Plan

1. Open `Q2_ChainRequest.jmx` in JMeter
2. Ensure JSON Server is still running
3. Run the test plan (green ▶️ button)
4. This plan will:

   * POST data
   * GET data
   * PATCH (update) data
   * DELETE data
   * GET again to confirm deletion

---

### 🧪 Q3: CSV Data-Driven Testing (No JSON Server needed)

1. Open **JMeter**
2. Load the test plan: `Q3_CSV_Data_TestPlan.jmx`
3. In the **CSV Data Set Config**, verify the correct path to `users.csv`
4. Run the test
5. The test will:

   * Read data from the CSV file
   * Send POST requests using that data
   * Use GET requests to verify the data matches

> No need to install or run any external server for Q3.

---

✅ You’re all set to test APIs in JMeter with confidence!


---

## 🔗 API Under Test

These test plans are based on the public REST API:
**https://68831de421fa24876a9cb69a.mockapi.io/users** 
**https://api.escuelajs.co**
A dummy API commonly used for learning and testing.

---
## 🤝 Credits

This repository is created as part of my internship program focusing on practical API Testing with Postman. I thank my mentors for guiding me through advanced features like scripting, chaining, and dynamic variable management.

## 📬 Contact
Feel free to reach out to me for any queries, feedback, or suggestions. Let’s connect and collaborate!

## 📧 Email: klaiba412@gmail.com  

## 🌐 LinkedIn: [Laiba Khan](https://www.linkedin.com/in/laiba-khan-955691264/)

---

**Happy Testing!** 🧪✨  

