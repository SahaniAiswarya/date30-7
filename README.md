# date30-7

class vehicle:
    def start_engine(self):
        print("engine started...")
class car(vehicle):
    def drive(self):
        print("the car is being drove")
c=car()
c.start_engine()
c.drive()


 class person:
     def info(self):
         print("I am a student")
class student(person):
    def study(self):
        print("The student is studying!!!!")
s=student()
s.info()
s.study()


class operate:
    def userdata(self):
        self.num1=int(input("enter the value of num1:"))
        self.num2=int(input("enter the value of num2:"))
class summate(operate):
    def add(self):
        result=self.num1+self.num2
        print(f"the result is {result}:")
c=summate()
c.userdata()
c.add()


class operate:
    def userinput(self):
        self.num1=float(input("enter the value of num1:"))
        self.num2=float(input("enter the value of num2:"))
class divider(operate):
    def div(self):
        try:
            result=self.num1/self.num2
            print(f"the result is :{result}")
        except ZeroDivisionError:
            print("Error: cannot be divided by zero")
c=divider()
c.userinput()
c.div()


class intern: #super
    def __init__(self,name):
        self.name=name
    def display_intern(self):
        print(f"Name:{self.name}")

class employee(intern): #class
    def __init__(self,name,emp_id):
        super().__init__(name)
        self.emp_id=emp_id
    def display_employee(self):
        print(f"Employee Id:{self.emp_id}")

class manager(employee): #sub class
    def __init__(self,name,emp_id,dept):
        super().__init__(name,emp_id)
        self.dept=dept
    def display_manager(self):
        print(f"Department:{self.dept}")


name=input("enter name:")
emp_id=input("enter employee id:")
dept=input("enter department:")
m=manager(name,emp_id,dept)
m.display_intern()
m.display_employee()
m.display_manager()


class Input:
    def __init__(self):
        self.num1=int(input("enter the value of num1:"))
        self.num2=int(input("enter the value of num2:"))
class operate(Input):
    def __init__(self):
        super().__init__()
    def add(self):
        return self.num1+self.num2
    def mul(self):
            return self.num1*self.num2
class result(operate):
    def __init__(self):
        super().__init__()
    def display(self):
        print(f"sum: {self.add()}")
        print(f"mul: {self.mul()}")
r=result()
r.display()      
