# 💰 Google Pay Expense Sharing System

## 📌 Project Overview
This project simulates an expense sharing system similar to Google Pay. It helps a group of friends track shared expenses and calculate who owes whom after splitting costs.

The system supports:
- Equal expense splitting
- Multiple participants
- Calculation of balances
- Identification of creditors and debtors
- Final settlement between users

---

## 🎯 Business Use Case
Friends traveling together often share expenses such as accommodation, food, and transport. This system helps:
- Track shared expenses
- Automatically split costs
- Determine final settlements
- Avoid manual calculations

---

## ⚙️ Methodology

### ✅ Equal Split Method
Each expense is divided equally among all participants.

**Formula:**
Split Amount = Total Expense / Number of Participants

- The payer's contribution is adjusted.
- Other participants are assigned their share of the expense.

---

## 🧮 Algorithm Approach

### Case 1: Balance Tracking
- Maintain a balance for each user.
- If a person pays, their balance decreases (they are owed money).
- Participants' balances increase (they owe money).

### Case 2: Creditor & Debtor Identification
- Creditors → users with positive balance (to receive money)
- Debtors → users with negative balance (to pay money)
- Match debtors with creditors to settle payments.

---

## 📊 Dataset Details
The dataset is manually provided via user input or hardcoded values:
- List of friends (users)
- Expense entries:
  - Payer
  - Amount
  - Participants

Example:
- Alice pays ₹900 for accommodation
- Bob pays ₹300 for food
- Carol pays ₹200 for fuel

---

## 🧹 Data Preprocessing
- Input is cleaned and converted into lists
- Strings are stripped of extra spaces
- Expense values are converted to float
- Participants are validated
- Balances are initialized for each user

---

## ⚠️ Special Cases Handled
- **Refunds:** Can be treated as negative adjustments
- **Unequal Participation:** Some users may not be part of all expenses
- **Self-participation:** Payer may also be included in splitting
- **Floating point values:** Rounded during output
- **Dynamic input mode:** Users can enter expenses interactively

---

## 🧑‍💻 Implementation Details

### Libraries Used:
- Python built-in data structures (no external libraries required)
- Optional: Pandas / Matplotlib (for extension and visualization)

### Core Components:
- `ExpenseSharing` class
- `add_expense()` method
- `calculate_settlement()` method
---

## 🧾 Sample Input

- Alice pays ₹900 for [Alice, Bob, Carol]
- Bob pays ₹300 for [Alice, Bob, Carol]
- Carol pays ₹200 for [Alice, Carol]

---

## 📤 Sample Output

- Bob owes Alice ₹X
- Carol owes Alice ₹Y
- Final settlement balances displayed

---

## 🔍 Results and Insights
- Identifies who owes money
- Identifies who should be reimbursed
- Provides optimized settlement between users
- Reduces multiple transactions into minimal payments

---

## 🚧 Challenges Faced
- Handling multiple participants
- Managing floating point precision
- Avoiding incorrect balance calculations
- Structuring creditor-debtor settlement logic
- Handling dynamic user input

---

## 🚀 Future Improvements
- Add GUI or web application
- Implement weighted splitting
- Add authentication system
- Export reports as PDF/CSV
- Add database storage
- Improve visualization dashboards

---

## ▶️ How to Run the Project

### Run in Command Prompt:
```bash
python sharing_app.py
