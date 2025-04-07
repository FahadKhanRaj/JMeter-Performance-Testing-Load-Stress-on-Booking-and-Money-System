# Booking API Performance Test - JMeter

This project contains performance and stress testing scripts for the [Restful Booker API](https://restful-booker.herokuapp.com/) using Apache JMeter.

---

## ✅ Files Included

- `booking.jmx` – JMeter test plan for login, create booking, and search booking.
- `Report/` – HTML reports for load test and stress test (add after running tests).
- `booking-api-test-report.xlsx` – Excel file with two tabs: Load Test Report and Stress Test Report.
- `README.md` – This file.
- `.gitignore` – Ignores unnecessary files like `.jtl` results and large report folders.
- `Resource` – includes necessary csv files
- `10min-100users booking report`
- `20min-200users booking report`
- `5min-50users booking report`
---

## ✅ Prerequisites

- [Apache JMeter](https://jmeter.apache.org/) (v5.5 or above)
- Java (JDK 8 or higher)
- Internet Connection (to reach the API endpoints)

---

## ✅ How to Run the Test

1. **Open `booking.jmx`** in JMeter.
2. Set the thread values according to test phase (e.g., 50 users for 5 min).
3. Run the test using **Start** button.
4. After the test is complete, JMeter will save results in the defined folder.
5. To generate an HTML report:
   - Go to `bin` directory of JMeter.
   - Run:
     ```bash
     jmeter -g result.jtl -o Report/
     ```

---

## ✅ Load Test Steps

Performed in 3 stages using a **Gaussian Random Timer** (Deviation: 2000ms, Delay: 500ms):

| Stage | Users | Duration |
|-------|-------|----------|
| 1     | 50    | 5 minutes |
| 2     | 100   | 10 minutes |
| 3     | 200   | 20 minutes |

**Metrics Collected:**
- Throughput
- Response Time
- Error %  

---

## ✅ Stress Test Steps

Gradually increased the number of users until the server bottleneck was observed.  

---

# ✅ Load test and Stress test from the Excel file

![image](https://github.com/user-attachments/assets/0295e183-a865-4bbd-a174-f2f7d12217b4)
![image](https://github.com/user-attachments/assets/7fce0404-5a6a-4549-9e4e-d771b3eb28d0)




## ✅ Report Screenshots
### ✅ Booking Load Testing (5Min, 10Min, 20Min)

![5min 2](https://github.com/user-attachments/assets/49a94101-cc98-4d6b-927a-784772cea7be)
![5min 1](https://github.com/user-attachments/assets/ccbcb28c-2a1f-4cb8-9a4e-2d1985bb5858)

---
![10min 2](https://github.com/user-attachments/assets/406f8b59-abf3-40af-9b1d-bc5dd48cc9ef)
![10min 1](https://github.com/user-attachments/assets/38b81388-269b-46ca-8e9e-1e7eaf3bb740)

---
![20min 2](https://github.com/user-attachments/assets/94cb99d1-d87f-4b34-97ea-301531f72cbc)
![20min 1](https://github.com/user-attachments/assets/293896c2-ec76-4bc5-825d-c795be579c9f)


### ✅ Booking Stress Testing 
![user700 1](https://github.com/user-attachments/assets/703d7fa8-fcbd-48cd-9e89-c306d6bdfc10)
![user700 2](https://github.com/user-attachments/assets/55befe2e-433a-4564-8677-7b47ab73e441)

# ✅ Dmoney request summary and statistics from the generated HTML report
![Screenshot1](https://github.com/user-attachments/assets/00dc8279-b109-4019-9cdf-706d06a9e7a5)

---

