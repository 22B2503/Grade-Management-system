# Grade-Management-system
student_grades = {}

# Adding new student
def add_student(name, grade):
    student_grades[name] = grade
    print(f"Added {name} with a grade of {grade}")

# Update student
def update_student(name, grade):
    if name in student_grades:
        student_grades[name] = grade
        print(f"{name}'s grade has been updated to {grade}")
    else:
        print(f"{name} not found")

# Delete student
def delete_student(name):
    if name in student_grades:
        del student_grades[name]
        print(f"{name} has been deleted")
    else:
        print(f"{name} not found")

# View all students
def view_all_students():
    if student_grades:
        for name, grade in student_grades.items():
            print(f"{name}: {grade}")
    else:
        print("No students found")

def main():
    while True:
        print('\nStudent Grades Management System')
        print("1. Add Student")
        print("2. Update Student")
        print("3. Delete Student")
        print("4. View All Students")
        print("5. Exit")

        choice = float(input("Enter your choice: "))
        if choice == 1:
            name = input("Enter student name: ")
            grade = float(input("Enter grade: "))
            add_student(name, grade)
        elif choice == 2:
            name = input("Enter student name: ")
            grade = float(input("Enter grade: "))
            update_student(name, grade)
        elif choice == 3:
            name = input("Enter student name: ")
            delete_student(name)
        elif choice == 4:
            view_all_students()
        elif choice == 5:
            print("App is closing ...")
            break
        else:
            print("Invalid input")

if __name__ == "__main__":
    main()
