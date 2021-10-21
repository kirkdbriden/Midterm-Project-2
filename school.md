[Home](README.md)  
[General Info](general-info.md)  
[Sports](sports.md)  
[Hobbies](hobbies.md)
# School
### Elementary School:
![Kirk Day School](https://images.squarespace-cdn.com/content/v1/59a4327f6f4ca3e5e092c400/1597759897141-K26S30H122PYZF3QC2QT/KDS_vrt-color.jpg?format=100w)  
I attended **Kirk Day School** in St. Louis, Missouri from Kindergarten through sixth grade.  
[Kirk Day School's Website](https://www.kirkdayschool.org).
### Middle School/High School:
![Westminster](https://townandstyle.com/wp-content/uploads/2017/08/wca-logo1.png)  
I attended **Westminster Christian Academy** in St. Louis, Missouri from seventh grade through senior year of high school.  
[Westminster's Website](https://www.wcastl.org).
### College:
![Mizzou](1200px-Missouri_Tigers_logo.svg-2-2.png)  
I currently attend the **University of Missouri** in Columbia, Missouri. I am studying Information Technology. My goal is to become a professional software developer and either start my own business or take over the business that my dad started. My favorite part about my schoolwork at Mizzou is the challenges that are assigned each week in my programming classes. My favorite challenge that I've done is to write a python program that takes a file from the user that has a list of numbers and returns stats about the numbers. Here is the code for the file:

```
def get_filename_from_user():
    while True:
        try:
            filename=input("What is the name of the file? ")
            fp = open(filename)
            return filename
        except Exception as error:
            print("Please enter a valid file name.")


def get_count(filename, numbers):
    fp=open(filename)
    for x in fp:
        x = x.strip()
        if x.isnumeric():
            numbers.append(x)
        else:
            return False
    fp.close()
    return numbers


def get_sum(numbers):
    for i in range(0 , len(numbers)):
        numbers[i] = int(numbers[i])
    sum_numbers = sum(numbers)
    return sum_numbers
            

def get_average(numbers):
    average = round(sum(numbers) / len(numbers), 3)
    return average
    

def get_maximum(numbers):
    maximum = max(numbers)
    return maximum


def get_minimum(numbers):
    minimum = min(numbers)
    return minimum

def run_again():
    while True:
        run_again = input("Would you like to evaluate another file? (y/n)")
        if run_again == "y" or run_again == "Y":
             yes_or_no = "yes"
             return True
        elif  run_again == "n" or run_again == "N":
            yes_or_no = "no"
            return False
        else:
           print("Please enter 'y' or 'n'")

def main():
    while True:
        numbers = []
        filename = get_filename_from_user()
        count = get_count(filename, numbers)
        if count == False:
            print("File must only contain numbers")
            continue
        count = len(count)
        sum_numbers = get_sum(numbers)
        average = get_average(numbers)
        maximum = get_maximum(numbers)
        minimum = get_minimum(numbers)
    
        print("File name:", filename)
        print("Sum:", "{:,}".format(sum_numbers))
        print("Count:", "{:,}".format(count))
        print("Average:", "{:,}".format(average))
        print("Maximum:", "{:,}".format(maximum))
        print("Miminum:", "{:,}".format(minimum))
        print("Range:", "{:,}".format((maximum-minimum)))
        if  not run_again():
            break
    
        
    


main()
```
