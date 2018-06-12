from abc import ABC, abstractmethod

class Employee(ABC):
    @abstractmethod
    def calculate_salary(self, sal):
        pass

class Developer(Employee):
    def calculate_salary(self, sal):
        finalsalary = sal * 1.10
        return finalsalary

    def position_1(self, position):
        self.position = position
        return position

emp_1 = Developer()
print(emp_1.calculate_salary(10))
print(emp_1.position_1('WebDeveloper'))
