  Task 1 :
  
get_valid_input function:
This function takes two parameters: prompt (a string representing the prompt for user input) and input_type (a string specifying the expected type of input, either "int" for integer or "bool" for boolean).
It uses a while True loop to repeatedly prompt the user for input until a valid input is provided.
Inside the loop, it attempts to convert the user input to the specified type (int or bool) and performs additional validation based on the input type.
If the input is invalid, it catches a ValueError and prints an appropriate error message.
If the input is valid, it breaks out of the loop and returns the validated user input.
calculate_total_price function:
This function calculates the total price of the pizzas based on various factors:
num_pizzas: Number of pizzas ordered.
delivery_required: Boolean indicating whether delivery is required.
is_tuesday: Boolean indicating whether it is Tuesday.
used_app: Boolean indicating whether the customer used the app for ordering.
It calculates the total price by considering the base pizza price, delivery cost (if applicable), and applying discounts for Tuesday and app usage.
The final total price is rounded to two decimal places and returned.
main function:
This function serves as the entry point of the program.
It prints a header for the pizza price calculator.
It calls the get_valid_input function four times to obtain user inputs for the number of pizzas, delivery requirement, whether it's Tuesday, and whether the customer used the app.
It then calls the calculate_total_price function with the obtained inputs and prints the result, showing the total price of the pizzas.
Execution:
The script executes the main function only if the script is run directly (not imported as a module).
Note:
The comparison in calculate_total_price for delivery_required, is_tuesday, and used_app is against strings 'y' or 'n'. This is because the get_valid_input function converts boolean inputs to lowercase strings ('y' or 'n'). The comparison in calculate_total_price is adjusted accordingly.
In summary, this program takes user inputs for pizza order details, validates the inputs, calculates the total price considering discounts and delivery costs, and then displays the final calculated total price.

Task 2 :

This code is a Python script designed to analyze a cat shelter log file and provide statistics on cat visits. Let's break down the code:

format_time function:
This function takes an input minutes and converts it into a formatted string of hours and minutes.
It calculates the number of hours by using integer division (//) and the remaining minutes using the modulo operator (%).
The result is returned as a formatted string.
analyze_cat_shelter_log function:
This function takes a file path as a parameter and reads the contents of the specified file.
It initializes variables to keep track of cat visits, visits by other cats, total time spent in the house, and a list of durations for cat visits.
It then iterates through each line of the file, extracting information about each cat visit. The information is in the format: cat, entry_time, exit_time.
For each "OURS" cat visit, it increments the cat_visits counter, calculates and accumulates the total time spent in the house, and records the duration of the visit in the durations list.
For visits by other cats (where entry_time is not equal to exit_time), it increments the other_cats counter.
The loop terminates when it encounters a line with 'END'.
After processing the log, it checks if there were any visits recorded for the correct cat ('OURS'). If not, it prints a message and returns.
It calculates and formats statistics such as the average visit duration, longest visit duration, and shortest visit duration.
Finally, it prints the analysis results.
Execution:
The script checks if it is run directly (if __name__ == "__main__":) and ensures that it receives exactly one command-line argument specifying the path to the log file. If not, it prints an error message.
If a valid file path is provided, it calls the analyze_cat_shelter_log function with the specified file path.
Note:
The script assumes a specific log file format where each line contains information about a cat visit in the format cat, entry_time, exit_time. The log is terminated by a line containing 'END'.
The script uses command-line arguments (sys.argv) to get the file path, so the user needs to provide the file path when running the script.
In summary, this script reads a cat shelter log file, analyzes the data to calculate various statistics related to cat visits, and then prints the results.

Task 3 :

This Python script appears to be a basic user management system with password encryption and authentication. Let's go through the code step by step:

Imports:
The script uses the hashlib module for password encryption and the getpass module to securely input passwords.
Constants:
The script defines a constant PASSWORD_FILE representing the path to the password file ("passwd.txt").
Functions:
encrypt_password(password): Takes a password as input, uses SHA-256 hashing to encrypt it, and returns the hexadecimal digest of the hash.
read_password_file(): Reads the password file line by line, removes leading/trailing whitespaces, and returns a list of entries.
write_password_file(entries): Writes the list of entries to the password file, separating them with newline characters.
adduser(): Allows the user to add a new user by providing a username, real name, and password. It checks if the username already exists in the password file before adding a new entry.
deluser(): Allows the user to delete a user by providing the username. It removes the user entry from the password file.
passwd(): Allows a user to change their password. It verifies the current password, prompts for a new password, and updates the password in the file.
login(): Asks the user for a username and password, checks if the provided credentials match any entry in the password file, and prints whether the login was successful.
main() function:
Runs an infinite loop presenting a menu with options to add a user, delete a user, change a password, login, or quit.
Based on the user's choice, it calls the corresponding function (adduser(), deluser(), passwd(), login()), or quits the loop if the user selects the "Quit" option.
Execution:
The script checks if it is run directly (if __name__ == "__main__":) and then calls the main() function to start the user management system.
Notes:
Passwords are stored as hashed values in the password file, enhancing security.
The script ensures that usernames are case-insensitive.
Password change includes verification steps to ensure accuracy.
This script provides a simple, command-line-based user management system but may not be suitable for production use without additional security measures.
Overall, this script serves as a basic example of user management with password encryption and authentication.













