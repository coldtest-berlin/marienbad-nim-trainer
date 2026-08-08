# Nim / Marienbad Trainer 🎲

An interactive, single-file trainer for mastering the winning strategy of the mathematical game **Nim** (popularized as **Marienbad** in the 1961 Alain Resnais film *Last Year at Marienbad*).

---

## 🎬 Background & Player Experience

In the movie, the protagonist challenges various hotel guests to a matchstick game with the classic **1–3–5–7** layout and **always wins**, regardless of who plays first. 

### The Rule of Victory:
- **If Player A knows the formula and Player B does not:** Player A always wins.
- **If both players know the formula:** The **second player** always wins from the standard 1–3–5–7 setup.

This trainer is designed to turn the XOR calculations into fast muscle memory, allowing you to instantly spot the winning move in real-life games with friends.

---

## 📜 Game Rules

1. There are 4 rows of items (standard set: **1, 3, 5, 7**).
2. Two players take turns removing items.
3. On a single turn, a player may remove **any number of items**, but **only from a single row**.
4. **Misère Play:** The player who is forced to take the **last item loses**.

---

## 🧮 Mathematical Strategy (How to Win)

### 1. Mid-Game Strategy (Bouton's Theorem)
Your main goal on every move is to leave the board with a **Nim-sum (XOR-sum) equal to 0**.

$$R_1 \oplus R_2 \oplus R_3 \oplus R_4 = 0$$

#### Quick Heuristics:
- **Two identical rows in a 3-row state:** Completely eliminate the 3rd row 
- **Two identical rows in a 4-row state:** Equalize the other two rows to `1` 

#### You need to aim for the following winning positions (the order does not matter):
* **3-Row Patterns:** `1-2-3`, `1-4-5`, `2-4-6`, `2-5-7`, `3-4-7`, `3-5-6`
* **4-Row Patterns:** `1-2-4-7`, `1-2-5-6`, `1-3-4-6`

---

### 2. The Endgame Strategy
- **Goal:**  make `1-1-1` or `1`.
---

## 🚀 How to Run

1. Open `index.html` in any browser (works on Mobile and Desktop).
2. Use **Standard Nim Mode** to train 0-XOR calculations.
3. Use **Endgame Trainer Mode** to master the Misère transition rule.
4. Fully air-gapped and secured via strict Content Security Policy (`connect-src 'none'`).
