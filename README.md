# Gomoku (Five in a Row) AI Player

> **An algorithmic Gomoku AI bot developed using pure C++/Python, achieving Rank 2nd in the in-class AI Programming Tournament.**

<p align="center">
  <img src="[여기에 게임 플레이 스크린샷 이미지 주소를 넣으세요]" width="45%">
  <img src="[여기에 터미널 입력/출력 스크린샷 이미지 주소를 넣으세요]" width="45%">
</p>

## 📖 Project Overview
This project is an implementation of a Gomoku (Five in a Row) game AI without relying on machine learning libraries. The goal was to construct a high-performance player using only fundamental search algorithms and heuristic evaluations, demonstrating strong algorithmic problem-solving skills.

The AI player ranked **2nd out of [몇 명인지 대략 숫자] teams** in the final class tournament, proving its robust and strategic gameplay capability.

## 🧠 Core Algorithms & Logic
Unlike ML-based approaches, this AI makes decisions based on a set of prioritized rules inspired by the **Minimax algorithm principles**.

### 1. Strategic Priority System (Heuristics)
The AI evaluates the board and decides its move based on the following strict priority order:

1.  **Immediate Win:** If I can complete 5-in-a-row now, take it.
2.  **Block Opponent Win:** If the opponent can win next turn, block them immediately.
3.  **Create Threats (4-3 / Open 4):** If I can create a double threat (e.g., "four and three"), do it.
4.  **Block Threats:** Block the opponent's attempts to create threats.
5.  **Develop Board (Open 3 / Open 2):** If no immediate threats, make a strategic move to build open rows (e.g., open 3, open 2) for future attacks.

### 2. Algorithmic Implementation
* The core logic is implemented using extensive nested conditional statements (`if/else`) and loops (`for`) to scan the board and detect patterns.
* **Custom Pattern Recognition Functions:** Developed functions like `three_rule()` and `can_form_n_in_a_row()` to accurately identify complex board states like "open 3", "closed 4", "broken 3", etc.

## 📸 Gameplay Demo (How it works)
(See screenshots above)
1.  The game starts by asking who goes first.
2.  The user enters coordinates (e.g., `K, 10`) in the console.
3.  The AI instantly calculates its best move based on the priority logic and places its stone.
4.  The board state is visually updated using `matplotlib` after each move.

## 🛠 Tech Stack
- **Languages:** C++, Python
- **Libraries:** `matplotlib` (for board visualization), `numpy` (for calculations)

## 🚀 How to Run
```bash
# Clone this repository
git clone [본인의 리포지토리 주소]

# Navigate to the project directory
cd [폴더 이름]

# Run the game script
python [실행 파일 이름, 예: gomoku_ai.py]
