# Student Management App (Monolithic Version)

# Your task: Refactor this into multiple modules!

students = {}

# # -------------------------

# Student Functions

# # -------------------------


def add_student(name):
    if name not in students:
        students[name] = []
        print(f"Student {name} added.")
    else:
        print("Student already exists.")


def remove_student(name):
    if name in students:
        del students[name]
        print(f"Student {name} removed.")
    else:
        print("Student not found.")


def display_students():
    if not students:
        print("No students available.")
    else:
        print("Students:")
        for student in students:
            print(f"- {student}")


# -------------------------

# Grade Functions

# -------------------------


def add_grade(name, grade):
    if name in students:
        students[name].append(grade)
        print(f"Added grade {grade} to {name}.")
    else:
        print("Student not found.")


def calculate_average(name):
    if name in students and students[name]:
        avg = sum(students[name]) / len(students[name])
        return avg
        return 0


def display_student_info(name):
    if name in students:
        print(f"\n{name}'s Grades: {students[name]}")
        avg = calculate_average(name)
        print(f"Average: {avg:.2f}")
    else:
        print("Student not found.")


# -------------------------

# Main Program

# -------------------------


def main():
    while True:
        print("\n--- Student Management Menu ---")
        print("1. Add Student")
        print("2. Remove Student")
        print("3. Add Grade")
        print("4. Display Students")
        print("5. Display Student Info")
        print("6. Exit")

        choice = input("Enter your choice: ")

        if choice == "1":
            name = input("Enter student name: ")
            add_student(name)

        elif choice == "2":
            name = input("Enter student name: ")
            remove_student(name)

        elif choice == "3":
            name = input("Enter student name: ")
            try:
                grade = float(input("Enter grade: "))
                add_grade(name, grade)
            except ValueError:
                print("Invalid grade.")

        elif choice == "4":
            display_students()

        elif choice == "5":
            name = input("Enter student name: ")
            display_student_info(name)

        elif choice == "6":
            print("Goodbye!")
            break

        else:
            print("Invalid option.")


if __name__ == "main":
    main()
