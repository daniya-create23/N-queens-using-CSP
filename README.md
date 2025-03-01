# **N-Queens Problem Solver** 🧩👑

## **Overview**  
This project implements **N-Queens problem solvers** using various algorithms and optimization techniques. The N-Queens problem involves placing **n queens** on an **n×n chessboard** such that no two queens threaten each other. The project explores **backtracking**, **forward checking**, **MRV + LCV heuristics**, and **local search with min-conflicts** to solve the problem efficiently.

---

## **Features**  
- 🧠 **Multiple Algorithms**: Implements **backtracking**, **forward checking**, **MRV + LCV heuristics**, and **min-conflicts local search**.  
- ⏱️ **Performance Analysis**: Measures execution times for different algorithms and problem sizes.  
- 🚀 **Optimized Initialization**: Uses **greedy initialization** to reduce conflicts and improve runtime.  
- 📊 **Scalability**: Tests algorithms for **n up to 8004** and analyzes performance trends.  

---

## **Algorithms Implemented**  

### 🔵 **1. Backtracking**  
- **Strategy**: Recursively places queens column by column, backtracking when conflicts arise.  
- **Complexity**: Exponential time complexity, suitable for small **n**.  

### 🔴 **2. Backtracking with Forward Checking**  
- **Strategy**: Reduces search space by eliminating invalid rows and diagonals for future columns.  
- **Complexity**: More efficient than standard backtracking but still exponential.  

### 🟢 **3. Backtracking with MRV + LCV Heuristics**  
- **Strategy**: Uses **Minimum Remaining Values (MRV)** and **Least Constraining Value (LCV)** to prioritize columns and rows with fewer conflicts.  
- **Complexity**: Significantly reduces search space and runtime for larger **n**.  

### 🟠 **4. Min-Conflicts Local Search**  
- **Strategy**: Starts with a greedy initialization and iteratively minimizes conflicts using the **min-conflicts heuristic**.  
- **Complexity**: Scales well for large **n**, with sublinear growth in runtime.  

---

## **Results & Performance Metrics**  

### **Backtracking, Forward Checking, and MRV + LCV**  
| **n** | Backtracking (s) | Forward Checking (s) | MRV + LCV (s) |  
|-------|------------------|----------------------|---------------|  
| 4     | 0.0000           | 0.0000               | 0.0001        |  
| 10    | 0.0009           | 0.0008               | 0.0003        |  
| 20    | 7.2082           | 2.5562               | 0.0031        |  
| 29    | 105.0659         | 28.7028              | 0.0027        |  

- **MRV + LCV** outperforms the other methods, especially for larger **n**, due to its efficient pruning of the search space.  
- **Backtracking** becomes impractical for **n > 20**, while **forward checking** performs better but still struggles with larger **n**.  

---

### **Min-Conflicts Local Search**  
| **n**   | Min-Conflicts Optimized (s) |  
|---------|-----------------------------|  
| 4       | 0.0001                      |  
| 504     | 0.5406                      |  
| 1004    | 3.0570                      |  
| 8004    | 161.8191                    |  

- **Min-Conflicts** scales well for large **n**, with execution time growing sublinearly.  
- **Greedy initialization** and **conflict minimization** significantly reduce runtime compared to backtracking-based methods.  

---

## **Key Observations**  
1. **Small n (4–10)**: All algorithms perform similarly, completing in fractions of a second.  
2. **Moderate n (10–20)**: **MRV + LCV** starts to outperform **backtracking** and **forward checking**.  
3. **Large n (20–8004)**: **Min-Conflicts** dominates, with execution times remaining manageable even for very large **n**.  

---

## **How to Run**  

### **1. Clone the Repository**  
```bash
git clone https://github.com/YOUR_USERNAME/N-Queens-Solver.git
cd N-Queens-Solver
```

### **2. Install Dependencies**  
```bash
pip install numpy
```

### **3. Run the Solvers**  
- **Backtracking, Forward Checking, and MRV + LCV**:  
  ```bash
  python n_queens_csp.py
  ```
- **Min-Conflicts Local Search**:  
  ```bash
  python n_queens_min_conflicts.py
  ```

---

## **Future Improvements**  
🚀 **A* Search**: Implement A* with heuristic functions for better performance.  
🚀 **Parallelization**: Use multi-threading or GPU acceleration for large **n**.  
🚀 **Visualization**: Add a GUI to visualize the N-Queens solutions.  

---

## **Contributing**  
Want to improve this project? **Fork, submit pull requests, or suggest enhancements!**  

---

## **License**  
📜 This project is **open-source** and available for academic and research use.  

--- 

This README provides a **clear and structured overview** of your **N-Queens Problem Solver** project. 🚀 Let me know if you need further modifications!
