#__practical__1_

#Finding_roots



import math


def find_roots(a, b, c):
    # Calculate the discriminant
    discriminant = b**2 - 4 * a * c
    
    # Check if roots are real and different
    if discriminant > 0:
        root1 = (-b + math.sqrt(discriminant)) / (2 * a)
        root2 = (-b - math.sqrt(discriminant)) / (2 * a)
        return f"Roots are real and different: Root1 = {root1}, Root2 = {root2}"
    

    elif discriminant == 0:
        root1 = -b / (2 * a)
        return f"Roots are real and same: Root = {root1}"
    

    else:
        real_part = -b / (2 * a)
        imaginary_part = math.sqrt(-discriminant) / (2 * a)
        return f"Roots are complex: Root1 = {real_part} + {imaginary_part}i, Root2 = {real_part} - {imaginary_part}i"


a = float(input("Enter coefficient a: "))
b = float(input("Enter coefficient b: "))
c = float(input("Enter coefficient c: "))


if a == 0:
    print("The coefficient 'a' cannot be zero in a quadratic equation.")
else:
    print(find_roots(a, b, c))