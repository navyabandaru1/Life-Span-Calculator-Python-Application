# Life-Span-Calculator-Python-Application
# A Python-based command-line application that calculates the total number of days a user has lived based on their birthdate. This project demonstrates expertise in date manipulation, input validation, and error handling using Python’s DateTime module.


from datetime import datetime

def calculate_days_survived(birthdate):
    today = datetime.today()
    birthdate = datetime.strptime(birthdate, "%d/%m/%Y")
    days_survived = (today - birthdate).days
    
    return days_survived

def main():
    print("Welcome to the Days Survived Calculator!")
    birthdate = input("Enter your birthdate (DD/MM/YYYY): ")
    
    try:
        days = calculate_days_survived(birthdate)
        print(f"You have survived {days} days in this world!")
    
    except ValueError:
        print("Invalid date format. Please enter the date in DD/MM/YYYY format.")
if __name__ == "__main__":
    main()
