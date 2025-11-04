# Module Sandbox Project

This is a simple Python project demonstrating basic module importing and variable sharing between Python files.

## Project Structure

```text
20251104_module_sandbox/
├── Hello.py          # Main module with variables and calculations
├── Mod01.py          # Module that imports and uses Hello.py
├── __pycache__/      # Python bytecode cache directory (auto-generated)
└── README.md         # This documentation file
```

## Files Description

### Hello.py

This is the main module that contains:

- **Print Statement**: Outputs "Hello, World!" to the console
- **Variables**:
  - `x = 100` - Integer variable with value 100
  - `y = 200` - Integer variable with value 200
  - `z = x + y` - Calculated variable that stores the sum of x and y (300)

**Code:**

```python
print("Hello, World!")
x = 100
y = 200
z = x + y
```

### Mod01.py

This module demonstrates how to import another Python module and access its variables:

- **Import Statement**: `import Hello` - Imports the Hello.py module
- **Variable Access**: Accesses and prints the variables `x`, `y`, and `z` from the Hello module using dot notation

**Code:**

```python
import Hello

print(Hello.x)  # Prints: 100
print(Hello.y)  # Prints: 200
print(Hello.z)  # Prints: 300
```

## How to Run

1. **Run Hello.py directly:**

   ```bash
   python Hello.py
   ```

   **Output:**

   ```text
   Hello, World!
   ```

2. **Run Mod01.py:**

   ```bash
   python Mod01.py
   ```

   **Output:**

   ```text
   Hello, World!
   100
   200
   300
   ```

## Key Concepts Demonstrated

1. **Module Creation**: How to create a simple Python module (`Hello.py`)
2. **Module Importing**: How to import a custom module using `import` statement
3. **Variable Access**: How to access variables from an imported module using dot notation
4. **Code Execution**: When a module is imported, all its top-level code is executed

## Notes

- When `Mod01.py` imports `Hello`, the print statement in `Hello.py` executes automatically, which is why "Hello, World!" appears in the output
- The `__pycache__` directory is automatically created by Python to store compiled bytecode files for faster module loading
- Variables defined at the module level (like `x`, `y`, `z`) become attributes of the module object when imported

## Learning Objectives

This project is useful for understanding:

- Basic Python module structure
- How imports work in Python
- Variable scope and access across modules
- The execution flow when importing modules
