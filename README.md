
# calculator.jac

walker init {
    # Starting point of the calculator program
    std.out("Welcome to Jaseci Calculator!")
    std.out("Choose operation: add / sub / mul / div")

    operation = std.input("Enter operation: ")

    num1 = int(std.input("Enter first number: "))
    num2 = int(std.input("Enter second number: "))

    result = 0

    if operation == "add" {
        result = num1 + num2
    }
    elif operation == "sub" {
        result = num1 - num2
    }
    elif operation == "mul" {
        result = num1 * num2
    }
    elif operation == "div" {
        if num2 != 0 {
            result = num1 / num2
        }
        else {
            std.out("Error: Division by zero!")
            result = None
        }
    }
    else {
        std.out("Invalid operation!")
    }

    if result != None {
        std.out("Result = " + str(result))
    }
}


