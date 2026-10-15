# Python Password Generator 🔐

A simple command-line password generator written in Python. It creates a password using letters, numbers, and symbols based on the quantities entered by the user, then shuffles the characters to mix them together.

## Features

- Lets the user choose how many letters, numbers, and symbols to include.
- Supports uppercase and lowercase English letters.
- Includes digits from `0` to `9`.
- Includes a selection of common symbols.
- Randomizes the order of the generated characters.
- Uses Python's built-in `random` module, so no third-party packages are required.

## Requirements

- Python 3.x

## How to Run

1. Save the code in a file named `password_generator.py`.
2. Open a terminal or command prompt in the folder containing the file.
3. Run:

   ```bash
   python password_generator.py
   ```

   Depending on your system, you may need to use `python3` instead:

   ```bash
   python3 password_generator.py
   ```

## Example

```text
---------- Welcome to password generator ----------

How many letter you would like to store in your password : 8

How many number you would like in your password : 2

How many symbol you would like in your password : 2

Your Password is : aB7@cD2!efGh
```

*The password shown above is only an illustrative example. Your output will be different each time.*

## How It Works

1. The program defines pools of letters, numbers, and symbols.
2. It asks the user how many of each type should be included.
3. It randomly selects characters from the corresponding pools.
4. It shuffles the selected characters so the character types are mixed.
5. It joins the characters into a string and prints the password.

## Important Notes

- **Current counting behavior:** Each loop uses `range(0, requested_count + 1)`, which generates one more character than the user requests for that category. For example, entering `8` letters adds `9` letters. Change the loops to `range(requested_count)` to generate the exact requested number.
- **Input validation:** The current version expects whole-number inputs and does not validate negative values or non-numeric input.
- **Security:** This project uses Python's `random` module and is intended for learning and practice. For passwords protecting real accounts, use a trusted password manager or Python's `secrets` module instead.

## Possible Improvements

- Fix the off-by-one counting issue.
- Validate that inputs are non-negative integers.
- Let users set a total password length.
- Use `secrets` for stronger randomness when generating passwords for real use.

## License

This project is provided for learning and personal practice. Add a license file if you plan to distribute it publicly.
