# 🏦 ATM Simulation (Python DSA Project)

## 📌 Overview
This project is a **Python-based ATM simulation** designed for practicing **Data Structures & Algorithms (DSA)** concepts.  
It uses **arrays (lists)** to store account information, balances, ATM cash, and transaction history.  
The program simulates basic ATM functionality, including withdrawals, deposits, mini statements, and PIN changes.

---

## ⚙ Features
- **User Login** (Account number & PIN verification)
- **Balance Check**
- **Deposit Money**
- **Withdraw with Exact Denomination Calculation**
- **Mini Statement** (Last 5 transactions)
- **PIN Change**
- **ATM Cash Availability Display**
- **Daily Withdrawal Limit Enforcement**
- **ATM Cash Tracking & Update after Withdrawals**

---

## 🛠 Data Structures Used
- **Lists (Arrays)** for:
  - Accounts, PINs, Balances
  - ATM note denominations & quantities
  - Transaction history
  - Daily withdrawal tracking
- **Loops & Conditionals** for ATM menu control
- **Index Lookup** to map accounts to PINs & balances

---

## 💻 How It Works
1. **Login** with account number and PIN.
2. Choose an option from the menu:
   - **Check Balance**
   - **Deposit**
   - **Withdraw** (multiple of ₹100 only)
   - **Mini Statement** (last 5 transactions)
   - **Change PIN**
   - **Logout**
3. **Withdrawal Process**:
   - Validates amount (positive, multiple of ₹100)
   - Checks account balance
   - Enforces daily withdrawal limit (`₹25,000`)
   - Checks if ATM has enough cash
   - Calculates the **exact denomination combination** using available notes
   - Updates ATM storage and account balance

---

## 📜 Cash Dispensing Algorithm
**Pseudocode:**
remaining = amount
for each note_value in note_values:
needed = remaining // note_value
if needed > atm_cash[i]:
needed = atm_cash[i]
notes_to_dispense[i] = needed
remaining -= needed * note_value

if remaining != 0:
print("Cannot dispense exact amount")
cancel transaction


Example Run:
Welcome to ATM
1.Login
2.Show ATM Cash
3.Exit
Enter the choice: 1

Enter the Account number: 100
Enter the pin: 0000
Login successful

====ATM MENU====
1.Check Balance
2.Deposit
3.Withdraw
4.Mini Statement
5.Change Pin
6.Logout
Enter Choice: 3

Enter the withdrawal amount(multiple of 100): 1200
Please collect your cash: [2, 1, 0] # ₹500 x 2, ₹200 x 1
