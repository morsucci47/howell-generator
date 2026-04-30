## 🃏 What is a Howell Movement?
In Bridge tournaments, a Howell movement allows pairs to compete against each other, typically moving from table to table, while the boards (hands) follow a specific rotation. Generating these movements is a complex combinatorial problem, especially for **Reduced Howell** (where not all theoretical rounds are played).

## 🚀 Features
- **Dynamic Calculation**: No pre-stored tables. The algorithm finds solutions using a custom search logic.
- **Complete & Reduced Support**: Generates movements for any number of tables $N$, with rounds ranging from $N$ to $2N-1$.
- **Table Assignment (TorneoIN)**: Converts abstract board-round matrices into physical table-seat assignments.
-- **Instant Export**: Generates a CSV-ready list of movements (Table, Board, NS Pair, EW Pair).

## 🧠 The Algorithm
This project implements a unique "Chain Method" (Metodo delle Catene):
1. **Board-Round Matrix**: It first builds a logical matrix where boards are rows and rounds are columns.
2. **Backtracking Search**: It uses a recursive backtracking engine (`ruotaTutteRido`) to find valid pair rotations that satisfy bridge constraints (no pair meets twice, every pair plays every board once).
3. **Vertical & Horizontal Optimization**: The algorithm validates "chains" of encounters to ensure the movement is balanced and follows the "1-up" or "staggered" rotation patterns.

## 🛠️ Installation & Usage
Since this is a client-side JavaScript tool, no installation is required.
1. Clone the repository:
   ```bash
   git clone [https://github.com/morsucci47/howell-generator.git](https://github.com/morsucci47/howell-generator.git)