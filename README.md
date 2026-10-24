# My-frist-project-as-a-computer-programmer-
This project was made to test my understanding on computer language 
gh repo clone tarejamesbuku-maker/My-frist-project-as-a-compute
import math

def big_calculator():
    while True:
        print("\n" + "=" * 35)
        print("       🧮 BIG PYTHON CALCULATOR")
        print("=" * 35)
        print("1.  Addition (+)")
        print("2.  Subtraction (-)")
        print("3.  Multiplication (*)")
        print("4.  Division (/)")
        print("5.  Power (x^y)")
        print("6.  Square root (√x)")
        print("7.  Modulus (%)")
        print("8.  Floor division (//)")
        print("9.  Factorial (!)")
        print("10. Percentage (%)")
        print("11. Exit")
        print("=" * 35)

        choice = input("Choose an option (1-11): ")

        if choice == "11":
            print("Thanks for using Big Calculator!")
            break

        try:
            if choice == "6":
                x = float(input("Enter a number: "))
                if x < 0:
                    print("Error: Cannot calculate a real square root of a negative number.")
                else:
                    print("Result:", math.sqrt(x))

            elif choice == "9":
                x = int(input("Enter a non-negative integer: "))
                if x < 0:
                    print("Error: Factorial requires a non-negative integer.")
                elif x > 5000:
                    print("Number is too large for this calculator.")
                else:
                    print("Result:", math.factorial(x))

            elif choice in ("1", "2", "3", "4", "5",
                            "7", "8", "10"):
                a = float(input("Enter the first number: "))
                b = float(input("Enter the second number: "))

                if choice == "1":
                    result = a + b
                elif choice == "2":
                    result = a - b
                elif choice == "3":
                    result = a * b
                elif choice == "4":
                    if b == 0:
                        print("Error: Cannot divide by zero.")
                        continue
                    result = a / b
                elif choice == "5":
                    result = a ** b
                elif choice == "7":
                    if b == 0:
                        print("Error: Modulus by zero is undefined.")
                        continue
                    result = a % b
                elif choice == "8":
                    if b == 0:
                        print("Error: Cannot divide by zero.")
                        continue
                    result = a // b
                elif choice == "10":
                    result = (a / 100) * b
                    print(f"{a}% of {b} = {result}")
                    continue

                print("Result:", result)

            else:
                print("Invalid choice. Please choose 1-11.")

        except ValueError:
            print("Error: Please enter a valid number.")
        except OverflowError:
            print("Error: The result is too large.")
        except (ArithmeticError, TypeError) as error:
            print("Calculation error:", error)


big_calculator()
r-programmer-
