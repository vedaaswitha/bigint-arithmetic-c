 🔢 1024-bit Big Integer Arithmetic Library in C

A high-precision arithmetic library built in C that supports operations on **1024-bit integers** (up to 309 decimal digits).  
This project includes addition, subtraction, multiplication (Karatsuba), and division with full error handling and an interactive terminal-based interface.


✨ Features

- **Custom BigInt Type**  
  Represents integers up to 1024 bits using dynamic memory and array-based storage.

- **Arithmetic Operations**
  - ✅ Addition & Subtraction (with sign management)
  - ✅ Classical and Karatsuba Multiplication
  - ✅ Long Division Algorithm

- **Robust Error Handling**
  - Detects overflow for values exceeding 1024 bits
  - Gracefully handles division by zero
  - Validates input format and sign

- **Efficient Memory Management**
  - Allocates and frees memory cleanly to avoid leaks

- **User-Friendly CLI Interface**
  - Menu-based console input for operations and large number input

🧠 Algorithms Used

This library handles big integer arithmetic using a mix of classical and optimized algorithms to ensure both correctness and performance:

➕ 1. Addition & Subtraction
- Implemented using a digit-by-digit approach, similar to how we manually add or subtract numbers.
- Carries (in addition) and borrows (in subtraction) are handled explicitly.
- Supports both positive and negative integers with proper sign checks.
- Operates directly on arrays of digits to simulate high-precision math.


✖️ 2. Karatsuba Multiplication (Optimized)
- An efficient recursive algorithm used for multiplying large numbers.
- Reduces the number of multiplications compared to the standard method.
- Time complexity: **O(n^1.58)**, which is significantly better than classical **O(n²)** for big inputs.
- Useful when input size is large (hundreds of digits).



✖️ 3. Classical Multiplication (Fallback)
- Used for smaller inputs where recursion overhead in Karatsuba is unnecessary.
- Simple, schoolbook-style digit-by-digit multiplication.
- Time complexity: **O(n²)** — fine for short to medium-sized numbers.



➗ 4. Long Division
- Implements long division logic similar to what we use by hand.
- Processes the dividend one digit at a time to compute the quotient.
- Handles edge cases like negative numbers, leading zeros, and division by zero.
- Ensures correctness by keeping track of remainders and signs throughout.
