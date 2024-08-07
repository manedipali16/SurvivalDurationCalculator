# SurvivalDurationCalculator
Function calculate_duration(age, unit):

 Takes the user's age and the chosen time unit as inputs.
 Converts the age into the corresponding time unit.
 Returns the calculated duration and the unit name.
2.Function main():

    Prompts the user for their age.
    Prompts the user to choose a time unit.
    Calls the calculate_duration function with the provided age and unit.
    Prints the duration in the chosen time unit.
This code will handle the conversion and display the duration in the selected unit. The user can input either the full name of the time unit or just the first letter like for Month write M.

We use unit.lower() function to convert the input string to lowercase.

Explanation of how the unit.lower() function works:

          Input Handling: When the user inputs their chosen time unit, they might use different capitalizations.
          Case-Insensitive Comparison: By converting the input to lowercase with unit.lower(), we can compare it against lowercase strings ("months", "weeks", etc.) consistently, 
          avoiding errors due to capitalization differences.
I will explain the code with a detailed explanation to get clarity of the code:

def calculate_duration(age, unit): # Convert the unit to lowercase for case-insensitive comparison unit_lower = unit.lower()

if unit_lower in ['months', 'm']:
    # Convert age to months
    return age * 12, "Months"
elif unit_lower in ['weeks', 'w']:
    # Convert age to weeks
    return age * 52, "Weeks"
elif unit_lower in ['days', 'd']:
    # Convert age to days
    return age * 365, "Days"
elif unit_lower in ['hours', 'h']:
    # Convert age to hours
    return age * 365 * 24, "Hours"
elif unit_lower in ['minutes', 'min']:
    # Convert age to minutes
    return age * 365 * 24 * 60, "Minutes"
elif unit_lower in ['seconds', 's']:
    # Convert age to seconds
    return age * 365 * 24 * 60 * 60, "Seconds"
else:
    # If the unit is not recognized, return None
    return None, None
def main(): # Prompt the user for their age age = int(input("What's your age? "))

# Prompt the user to choose a time unit
unit = input("Please choose a time unit: Months, Weeks, Days, Hours, Minutes, Seconds.\nNote: You can write the first letter or the full name of the time unit. ")

# Calculate the duration in the chosen time unit
duration, unit_name = calculate_duration(age, unit)

# Check if the calculation was successful
if duration is not None:
    # Display the result
    print(f"You have lived for {duration} {unit_name}.")
else:
    # Inform the user of an invalid time unit
    print("Invalid time unit chosen.")
Run the main function when the script is executed
if name == "main": main()
