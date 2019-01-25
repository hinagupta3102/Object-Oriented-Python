# Object-Oriented-Python
OOP Python
class Employee:
    # The __init__ method accepts arguments for the
    # name, and number of employees. It initializes
    # the data attributes with these values.
    
    def __init__(self, name, number):
        self.__name = name
        self.__number = number
       
    # The following methods are mutators for the
    # class's data attributes.
    
    def set_name(self, name):
        self.__name = name

    def set_number(self, number):
        self.__number = number

    # The following methods are the accessors
    # for the class's data attributes.
    
    def get_name(self):
        return self.__name

    def get_number(self):
        return self.__number

# The ProductionWorker class represents a production worker. It is a subclass
# of the Employee Class.

class ProductionWorker(Employee):
    # The __init__ method accepts arguments for the
    # employee's name, the employee's number
    # the employee's shift, and the employee's hourly rate.
    
    def __init__(self, name, number, shift, hourlyrate):
        # Call the superclass's __init__ method and pass
        # the required arguments. Note that we also have
        # to pass self as an argument.
        Employee.__init__(self, name, number)
        
        # Initialize the __shift attribute.
        self.__shift = shift

        # Initialize the __hourlyrate attribute.
        self.__hourlyrate = hourlyrate

    # The set_shift method is the mutator for the
    # __shift attribute.

    def set_shift(self, shift):
        self.__shift = shift

    # The get_shift method is the accessor for the
    # __shift attribute.

    def get_shift(self):
        return self.__shift
        
    # The set_hourlyrate method is the mutator for the
    # __hourlyrate attribute.

    def set_hourlyrate(self, hourlyrate):
        self.__hourlyrate = hourlyrate

    # The get_hourlyrate method is the accessor for the
    # __hourlyrate attribute.

    def get_hourlyrate(self):
        return self.__hourlyrate

# This program demonstrates the ProductionWorker class.

def main():
    
    # From the ProductionWorker Class, user will put in the.
    # worker's name, employee number, shift, and hourly rate.
    name = str(input("Please enter name "))
    number = int(input("Please enter number "))
    shift = int(input("Please enter shift "))
    hourlyrate = int(input("Please enter hourly rate "))

    production_worker = ProductionWorker(name, number, shift, hourlyrate)
    
    # Display the ProductionWorker data.
    print('name:', production_worker.get_name())
    print('number:', production_worker.get_number())
    print('shift:', production_worker.get_shift())
    print('hourly rate:', production_worker.get_hourlyrate())

# Call the main function.
main()
