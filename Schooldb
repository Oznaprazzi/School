#-------------------------------------------------------------------------------
# Name:        module1
# Purpose:
#
# Author:      huangc
#
# Created:     26/05/2014
# Copyright:   (c) huangc 2014
# Licence:     <your licence>
#-------------------------------------------------------------------------------
#!/usr/bin/env python

class School:
    def __init__(self, schoolname, numpupils, numclasses):
        self.schoolname = schoolname
        self.numpupils = numpupils
        self.numclasses = numclasses

    def pupils_per_class(self):
        return self.numpupils/self.numclasses

    def show_info(self):
        """
        >>> s = School("Eveyln Intermediate", 1500, 96)
        >>> s.show_info()
        Eveyln Intermediate has 15.62 pupils per room
        """
        str_form="{} has {:.2f} pupils per room"
        print(str_form.format(self.schoolname, self.pupils_per_class()))

def collect_data():
    global school_name
    global num_pupils
    global num_classes
    school_name=""

    while len(school_name) <= 2:
        school_name = input("Enter the name of the school.").title()
        if len(school_name) <= 2:
            print("Enter the name of the school.")

    while True:
        try:
            num_pupils = int(input("Enter the number of pupils altogether in the school."))
            if num_pupils <= 0:
                print ("Enter the number of pupils altogether in the school.")
            else:
                break
        except ValueError:
            print ("Enter the number of pupils altogether in the school.")

    while True:
        try:
            num_classes = int(input("Enter the number of classes in the school."))
            if num_classes <= 0:
                print ("Enter the number of classes in the school.")
            else:
                break
        except ValueError:
            print ("Enter the number of classes in the school.")


if __name__ == "__main__":
    import doctest
    doctest.testmod(verbose = True)
    cont="y"
    schools = []
    while cont=="y":
        repeat = int(input("How many schools do you want to enter?"))

        for i in range(repeat):
            collect_data()
            schools.append(School(school_name, num_pupils, num_classes))
        for School in schools:
            School.show_info()

        while True:
            cont=input("Do you want to enter more schools? (Please enter 'y' or'n')")
            if cont not in ("n", "y"):
                print("Please enter 'y' or 'n'")
            else:
                break

import csv #imports csv format
file_name = 'schooldb.txt' #sets up school database file name and saves it as a txt file

ofile = open(file_name, 'a') #open with write('w') or append('a') privelages
writer = csv.writer(ofile, delimiter=',') #separates values with commas
 
#explicitly closes the output file
ofile.close()
