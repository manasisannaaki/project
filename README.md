class Employee:
    def __init__(self, id, name, position, salary):
        self.id = id
        self.name = name
        self.position = position
        self.salary = salary
    def display_details(self):
        print(f"ID: {self.id}")
        print(f"Name: {self.name}")
        print(f"Position: {self.position}")
        print(f"Salary: ${self.salary}")
ceo = Employee(1, "sakshi", "CEO", 80000)
manager = Employee(2, "manasi", "Manager", 50000)
senior_engineer = Employee(3, "puja", "Senior Engineer", 30000)
employees = {
    ceo.id: ceo,
    manager.id: manager,
    senior_engineer.id: senior_engineer}

def get_position_and_salary_by_id_and_name():
    id = int(input("Enter employee ID: "))
    name = input("Enter employee name: ")
    if id in employees and employees[id].name.lower() == name.lower():
        print(f"Position: {employees[id].position}")
        print(f"Salary: ${employees[id].salary}")
    else:
        print("Employee not found")

def main():
    while True:
        print("\n1. Get position and salary by ID and name")
        choice = input("Enter your choice: ")
        if choice == "1":
            get_position_and_salary_by_id_and_name()
        elif choice == "2":
            break
        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    main()

