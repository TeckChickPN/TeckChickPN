def calculate_simple_interest(principal, time, gender, senior_citizen):
    if gender == 'Female' and senior_citizen:
        rate = 0.08
    elif gender == 'Female' and not senior_citizen:
        rate = 0.06
    elif gender == 'Male' and senior_citizen:
        rate = 0.07
    elif gender == 'Male' and not senior_citizen:
        rate = 0.05
    else:
        return "Invalid gender or senior citizen status"

    interest = principal * rate * time
    return interest

# Example usage
principal_amount = 10000
time_period = 2
customer_gender = 'Female'
is_senior_citizen = True

interest_amount = calculate_simple_interest(principal_amount, time_period, customer_gender, is_senior_citizen)
print("Simple Interest Amount:", interest_amount)
