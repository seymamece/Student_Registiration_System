"# Student_Registiration_System" 

students = []
close = False

def add_student():
    student_number = int(input("How many students do you want to add :"))
    for i in range(student_number):
        student = input("Please enter name and surname for add action :")
        students.append(student)
def delete_student():
    delete_number_of_student = int(input("How many students do you want to remove :"))
    List =[]
    x = 0
    while delete_number_of_student:
        remove_student = input("Please enter name and surname for add action :")
        List.append(remove_student)
        x += 1
        for i in students:
            if i in List:
               students.remove(i)
            else:
               continue
        if List == x:
            break
    print(List)

    print("The new students list :" + str(len(students)))
    for i in students:
        print("The new students list :" + str(i))

def show_student():
    student_number = 0
    for i in students:
        student_number += 1
        print(str(student_number) + " : " + str(i))

def show_student_number():
    show_number = input("Please enter name and surname for add action :")
    x = 0
    for i in students:
        if i == show_number:
            print("Student " + str(i) + "Number of index" + str(x))
        x += 1

def close():
    print("Close the program")
    for i in students:
        print(i)
    close = True
    return close

def menu():
    select_menu = int(input("Select the action you want to do : \n 1 = > Add Student \n 2 = > Remove Student \n 3 = > Show added students \n 4 = > Show the students number \n 5 = > Close the program and get the final list \n In order to use any of the values ​​given in the menu, press the menu number at the beginning..." ))
    if select_menu == 1:
        add_student()
    elif select_menu == 2:
        delete_student()
    elif select_menu == 3:
        show_student()
    elif select_menu == 4:
        show_student_number()
    elif select_menu == 5:
        return close()
    else:
        print("Try again")

while True:
    if menu():
        break





              



