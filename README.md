python 
from datetime import datetime 
def calculate_age(birthdate): 
today = datetime.today() 
age = today.year - birthdate.year 
# Adjust age if the birth date has not been reached this year 
if (today.month, today.day) < (birthdate.month, birthdate.day): 
age -= 1 
 
return age 
def main(): 
# Ask the user for their birthdate 
birthdate_input = input("Enter your birth date (YYYY-MM-DD): ") 
 
# Convert the input string to a datetime object 
try: 
birthdate = datetime.strptime(birthdate_input, '%Y-%m-%d') 
age = calculate_age(birthdate) 
print(f"You are {age} years old.") 
except ValueError: 
print("Invalid date format. Please enter the date in YYYY-MM-DD format.") 
if __name__ == "__main__": 
main() 
``` 
# Age-calculator
