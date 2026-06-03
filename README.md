# Interest Calculator

A Java-based banking application that calculates interest based on user-provided inputs including tenure, principal amount, age, and gender.

## Project Structure

```
intcalc/
└── intcalc/
    └── src/
        └── com/
            └── wipro/
                └── bank/
                    ├── main/
                    │   └── Main.java          # Entry point of the application
                    └── service/
                        └── BankService.java   # Interest calculation logic
```

## Features

- **Tenure Selection**: Choose between 5 or 10 years investment period
- **Principal Input**: Enter the monthly principal amount
- **Age Consideration**: Input customer age for age-based calculations
- **Gender-Based Rates**: Different interest rates based on gender
- **Interest Calculation**: Automated interest calculation based on the provided parameters

## Prerequisites

- Java 8 or higher
- JDK (Java Development Kit) installed
- A terminal or command prompt

## How to Compile

Navigate to the project directory and compile the Java files:

```bash
javac -d bin src/com/wipro/bank/main/Main.java src/com/wipro/bank/service/BankService.java
```

## How to Run

After compilation, run the application:

```bash
java -cp bin com.wipro.bank.main.Main
```

## Usage

When you run the application, you'll be prompted to enter the following information:

1. **Tenure**: Enter `5` or `10` (years)
2. **Monthly Principal**: Enter the monthly principal amount (in currency units)
3. **Age**: Enter your age (numeric value)
4. **Gender**: Enter `Male` or `Female`

### Example

```
Enter Tenure (5 or 10): 5
Enter Monthly Principal: 1000
Enter Age: 35
Enter Gender (Male/Female): Male
```

The application will then calculate and display the interest based on the inputs.

## Input Parameters

| Parameter | Type | Valid Values | Description |
|-----------|------|--------------|-------------|
| Tenure | int | 5, 10 | Investment period in years |
| Principal | float | Any positive number | Monthly principal amount |
| Age | int | Any positive number | Customer's age |
| Gender | String | Male, Female | Customer's gender |

## Code Overview

### Main.java
- Entry point of the application
- Handles user input using Scanner
- Creates a BankService instance and calls the calculate method

### BankService.java
- Contains the interest calculation logic
- Applies gender-based interest rates
- Calculates total interest based on tenure, principal, and age

## Notes

- The Scanner resource is properly closed after use to prevent resource leaks
- Input validation should be added for production use
- Consider adding exception handling for invalid inputs

## Future Enhancements

- Add input validation for all parameters
- Implement exception handling
- Add support for more tenure options
- Create a GUI interface
- Add database integration for storing calculations
- Generate detailed interest calculation reports

## Author

Created by: abinandu2005

## License

This project is open source and available under the MIT License.
