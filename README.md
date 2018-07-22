# Python
Notes for Python

Pre-Code
    
    Attributes of Python
        - Python is an interactive language, which means we don't actually have to compile it. 
        - Python is white space based, which means we don't need semi-colons as compared to C, instead, we just need the appropriate white space or indentation levels for each line of code. 
        - Python is dyanmic - this means that our variables don't need to be initialised as a certain data type. e.g, Instead of initialising x by using "int x = 5", we can just do "x = 5". As such, WE CAN CHANGE THE TYPE OF VALUE HELD BY VARIABLES. For example, in C, if we declare int x = 5, this means we can't then assign "Hello" as the value of x. On the other hand, in Python, we can have x = 5, then declare, later on, that x = "Hello". 

Mathematics

    It should be noted that in python, assigning a string to a variable does not require brackets. #C doesn't need this either does it? It's only for printing as far as I recall...
    Floats
    
        Floats are automatically recognised when we put decimal points after the number, or even just a decimal point at the end.
        
        you can even define floats using scientific notation with e indicating the power of 10
        
        e.g 1.5e2, representing 1.5 * 10^2
        
        A modulo operation with a % b finds the remainder of the division.
        
        If an ordinary division yields a decimal number, then Python will round it to the nearest whole number. To convert it to a decimal,
        we must convert either 1 or both of the nominator/denominator to a float. This can also be done by using float(a) or float(b). If
        we define a variable as a division of two variables, assuming we want the answer in decimal form, then we can define the factor variables as floats
    
    A boolean is a datatype which can only take one of two values.
    
    Booleans are defined in Python using keywords True and False
    
    True represents 1 and False represents 0. Essentially, a boolean is like a Bernoulli trial.
    
    we can convert variables to different datatypes using str(), int() and float();



INPUT:

    To take an input from the console, use
    
        raw_input("Prompt")

Printing
    Note that \n still works in Python as it does in C, creating a new line.
    
    Concatenation
        To concatenate strings, integers etc, we can use the following notation:
        
            print "String" + str(integer) + ...
            
    Printing with commas
        In the previous printing method, each string or integer would've been printed with no spaces in between. If you want gaps between them, use the following print method (ie, just put commas in between):
        
        print "string", "string", "str.."

Strings
    Introduction
        In Python, a string can contain letters, numbers and symbols, and is created with either "string" or 'string', but not string or "string'.
        If we were to try and create a string via the previous examples, the console would indicate an error.
        
        Apostrophes in string can be remedied by a \ in front of the apostrophe, e.g isn\'t.
        
        In Python, accessing an item from an array of string is given by "string"[item number]
    
    String Methods
        len()
        Finds the length of a string. To implement it, use the generic formula below
        
            len(variable_name) or len("Actual string")
            
        lower()
        Removes all caitalisation in strings. Implemented using the method
        
            "Actual String".lower() or variable_name.lower()
            
        upper()
        Causes all string elements to become upper case. Implemented using
        
            "Actual string".upper() or variable_name.upper()
            
        str()
        Converts all non-string datatypes into strings. Implemented using the below notation
        
            str(variable_name) or str(actual non-string data)
        
        It should be noted that methods which only work with string will use dot notation, whereas non-dot notation methods can use
        non-strings (obviously).
        
        The area where we write our code is called the editor, wheras the place where the results are printed is called the console.
        
    Concatenation
        Using +'s after each piece of string to create a desired sentence or statement etc.
    
    String formatting
        Use %s in the string where you want the non-string data to go, then afterwards, use %(variable_name) where variable_name is the data
        you want to insert. If you want to print a variable that is an integer, pad it with zeros, e.g
        
            %02d
        
        Here, the 0 means pad with zeros, the 2 means to pad 2 characters wide and d means teh number is a signed integer. 2 characters wide means
        that it will simply pad the number until there are 2 characters. Thus if a number already has 2 characters, then no leading zeros
        will be assigned. 
    
        Note that obviously, you must have teh same number of %s s in the string as the number of variables in the parenthesis.
        
        
Date and Time

    Useful for when we want to keep track of when something happened, we use date time. This is done by:
    
        from datetime import datetime
        now = datetime.now()
        
    Note that the line "from datetime import datetime" imports the datetime library so we can use it in some way.
    This will give the result:
    
        Year-Month-Day hour:minute:second
        
    However, to access only a certain element of datetime, we can use
    
        now.year;
        now.month;
        now.day;
        
    To print in the usual format of mm-dd-yyyy, we can use:
    
    "%02d-%02d-%04d"%(now.month, now.day, now.year)
    
    
Conditionals

    Comparators:
    
        == equal to
        != not equal to
        < less than
        <= less than or equal to
        > greater than
        >= greater than or equal to
        ** to the power of
        
    Boolean operators:
    
        and checks if both statements are correct in the statement "A and B"
        or checks if at least on statement is correct in the statement "A or B"
        not statement is true if conditional is false. To be more precise, if we have a statement A, and our boolean is the result of
        "not A", when A is in fact true, then the boolean will be false.
        If we have statement A, and A is false, then the boolean will be true. 
        
        Note that the actual value of the boolean will have two answers for operators of the "and" type:
        
            True/False and True/False
            
        In other words, it determines the veracity of each conditional separately. Note that we must always use capitals for the first
        letter of boolean values, otherwise it becomes a variable.
    
        It should be noted that there is an order to which the operators are evaluated. This order is:
        
            1. () brackets
            2. not
            3. and
            4. or
            
        This means that say for example we have a boolean whose value is equivalent to the result of False or not True and False.
        In this case, we evaluate the not statement first, which would be false. This means that the and statement (which is already false)
        is false. Therefore, the overall statement is false because the secondary condition for the "or" statement is also false.
        
        If we had True or not True and False, then we would have true, since at least one of the conditions is true. Likewise, if we had
        the statement as False or not (True and False), then we would still have true, since the bracket statement is false,
        so the not statement is true, so the overall or statement is true.
    
    
    Conditional Statements
    
            if a conditional statement which executes its specified code after checking if its expression is true. An if statement is implemented as follows:
            
                if condition:
                
            
            NOTE: You don't need brackets for the argument/condition in Python, whereas for C
            we do. 
            
            else a complementary statement to the if statement.  It runs some other block of code assuming the if statement is not fulfilled.
            An else statement is implemented as follows:
            
            else: 
            
            elif a conditional statement which provides an alternative to the if statements. An elif statement is implemented as follows:
            
            elif condition:
            
        
        In other words, the if is essentially the primary scenario, the elif statements alternatives to the if statement, and the else statement
        accounts for every other scenario except the if and elif statements.
        
        Essentially, when you call on a function with some value in the brackets, that is passing the value into the function as an
        argument or variable value, which can then be used in the function.
        
        NOTE: the conditional statements are evaluated sequentially: we first look at the if statement, then continue downwards through all
        the elseif statements if the if statement is false. Then, if an argument fulfils more than one elseif statement, the program will only
        execute the code for the earliest elseif statement that the argument fulfils.
        
        
        To get input from the console, assign a variable equal to raw input:
        
        variable_name = raw_input("What's you name?")


Functions

    Functions are blocks of code which are often used multiple times. Functions are comprised of 3
    main features
    
        1. header: This includes the "def" keyword(defines the function), the name
        of the function, and any parameters the function needs. This can be seen below
        
            def function_name(parameter1, parameter2, parameter3...)
            
            Where parameter[i] denotes arguments, or just values/variables used by the function in its body. 
            
        2. Comment: This part is optional, and explains what the function does.
        
        3. The body describes the procedures the function carries out. The body is indented, just like
        blocks of code would be in conditional statements.
    
    Calling
        To implement a function, we must always "call" it by typing in the function name and parameters if need be.
        This can be showni in the following notation
        
            function_name(parameter1, parameter2, parameter3)
        
        Note that we can't actually call a function before defining the function in our editor.
        This is actually intuitive since it wouldn't make sense to call a non-existent function.
    
    Parameters
        A variable which is an input to a function. So when we have the parameter n in the function as below
        
            def function_name(n)
            
        We're saying that when the function is used, n can take any value, but for now, we'll
        call the variable n.
        
        Note that the actual value of the parameter is called the ARGUMENT
        
        
    Return
        When we return a value or any output, that is the output of the function for the
        specific arguments which created that output. If the function was called, then
        the returned output will essentially be substituted into the original code which
        called the function with the specific arguments.
        
        Note that if the function has a conditional statement inside it, and the conditional
        statement returns an output, that output becomes the output of the outer function
        unless it manipulates the return value of the conditional even further.
        
        For instance, we had one block of code which was
        
            def test(parameter1, parameter2):
                if(parameter1 >= 5):
                    return parameter1*parameter2
                
                else:
                    return parameter1 + parameter2
                    
            def some_function(n):
                test_variable = test(n,2)
                print test variable
                
            some_function(5)
            
        In this case, the value 5 was passed as both an argument for the functions some_function and test
        
        We then have the returned value for the if statement becoming the returned value for
        the test function. 
        
    Fuction referencing other functions
    This can be done by returning/calling the other function within the other function.
    
        def function1(n):
            """Block of code"""
            
        def function2(n):
        
            return function1(n)
            
    Importing
        It's often the case that we need to import a number of functions, e.g sqrt or other math functions
        to do so, we type
        
            import module_name
            
        It's also possible to import a single function from a module, called a function import
        and this is done by the generic code
        
            from module import function
            
        It's also possible to do a universal import, importing all variables from a module.
        This is done by
        
            from module import *
            
        The problem with a unviersal import however, is that it could result in conflicting
        variable names, since we no longer need to type
        
            module.function
            
        To use a certain function anymore.
        
    Some other functions
    
        max(args) will give the maximum number from a set of number
        min(args) wil give the minimum number from a set of numbers
        abs(arg) will give the absolute value of a number
        type() returns the type of data the function receives.
        
Arithematic
    Brackets in arithematic will not affect anything.
    For conditionals, we can use an inequality of the form a<x<b.
    Arithematic when passing an argument, even when the argument involves the arithematic of
    another argument, is allowed.
    
    
    
Lists
    Essentially equivalent to an array from C. Lists are a data type which can be used to store collections of different pieces of information
    as a sequence under a single name. Lists can be empty. Lists are initialised in the following manner:
    
        list_name = [list_item1, list_item2.....]
        
    Index/access
        Individual items can be accessed through a lists index. The index appears after
        the list name, as seen below
        
            list_name[index]
            
        List indices begin with 0, not 1! Note that the index refers to the index number
        of an element in the list (which begins at 0).
        
            Multivariable lists/arrays or Lists in Lists
            To access the element within the list inside of another list, we use the same notation as we would for multidimensional arrays in C. For example:
            
                array = [[1,2,3,4][5,6,7,8]]
                
            If we want to access the element 6, we use the following notation:
            
                array[1][1] ///Since we're looking for the second element in the second list. 
        
    List Length
        If we have a list called list_name, then the length of the list (no.items in that list) can be found by:
        
            len(list_name)
        
    Replacement
        We can replace/change list items by redefining the item by defining the list item
        through teh index
        
            list_name[item number] = "New value"
            
    Addition
        We can also add itmes to lists through the append function. This will add a new item to the
        END of the list. This is shown below:
        
            list_name.append('new value')
            
    Slicing
        To access a range of items from the list, use the following notation
        
            slice = list_name[a:b]
            
        Note that whilst the "a"th item of the list will be included in the slice, the "b"th item will not.
        NOTE: When we talk about "index x", we are talking about the item of the list with
        index number of x, not the xth item of the list. Thus, index x is always the item after than
        the index of the xth item of the list.
        
        Note also that if the slice includes a range from the beginning of the list or to the
        end of the list, then the index numbers for the beginning/end do not have to be written
        in the slice. 
        
    Strings
        Strings are just a list of characters as stated previously in C. 
        
        
    Indexing
        Indexing is essentially just searching. If we want to search for a specific item, we use the index function
        
            list_name.index("value")
            
    Inserting
        Inserting will create items in the list in a specified index number:
        
            list_name.insert(index number, value)
            
        Note that this will not delete the list item previously at the specified index number, instead, all items after the index number will now have +1 index numbers.
        Ie, the new item pushes everything to the right. 
            
        
    For Loops
        For loops in python operate by assigning a variable an item in a list, then doing some
        process on that variable. This then continues for the rest of the list.
        
            for variable_name in list_name:
                """Code"""
                
        Alternatively, to actually modify the item you want, we have to use the index numbers
        method:
        
            for dummy_variable in range(len(list_name)):
                """Code to do something with list_name[dummy_variable]"""
                
    Sorting
        Using the sort fuction will cause a list to be arranged in alphabetical order or increasing
        value.
        
        #What's the actual call for this though? 
        
        
    Dictionary
        A dictionary is similar to a list, but values are accessed by finding a
        key rather than index number. A key is just a string or integer.
        
            dictionary_name = {"key1" : value, "key2": value...}
            
            OR
            
            dictionary_name = {
            
            
            "key1" : value,
            "key2" : value,
            .
            .
            .
            
            
            }
            
        Note that either double quotes or single quotes can be used to reference a key name.
        
        Adding values to a dictionary is done by
        
            dictionary_name[new_key] = new_value
            
        Modification
        
            Deletion of a dictionary item can be done by
            
                del dictionary_name[key_name]
                

            Modification of a dictionary item can be done by
            
                dicionary_name[key_name] = new_value
                
    Removal
        To remove an item from a list, we use the remove function:
            
            list_name.remove("list_item_to_be_removed)
            
        Alternatively, we can use
        
            list_name.pop(list_item)
            
    Lists-Functions
        It should be noted that functions can also take lists as arguments. 
            

For loops
    
    For loops in Python are slightly different to what we've previously seen in C. For loops in Python simply iterate over all the items, or elements in some iterable sequence. For example, a list is comprised of a sequence of indexes, which are iterable, while dictionaries are comprised of a sequence of keys.  
    
    For loops - dictionaries/lists
        For loops can be used to iterate over all the items in a list through
        following notation:
        
            for item in list_name
            
        Note that a for loop goes through each item in the list, rather than going through
        the number or index of each item. 
        
        The notation for a dictionary is slightly different. We have to essentially
        reference the list key first.
        
            for key in dictionary_name
            
            Then if we want to print the items.
            
            print dictionary_name[key]
            
        Note that in both cases, when we use the for "" in "", we are assigining each variable
        in the dictionary/list a variable name given by the first "". We can then manipulate
        or test this variable however we wish in the following code. Essentially, we loop through
        the list/dictionary and store each item under the variable name.
        
    For loops - accessing a range of values
        For loops can be used to iterate over a certain range of indexes in a list
        through the following notation
        
            for dummy_variable in range(0, len(list_name))
            
            
    Enumerate
        The enumerate fuction in Python works by supplying a corresponding index to each item
        you iterate over. It is used with the following notation:
        
            for index_dummy_variable, item in enumerate(list_name)
            
    Multiple lists
        For loops can also iterate over multiple lists using the notation:
        
            for item_in_list_A, item_in_list_B in zip(list_A, list_B):
            
        item_in_list_A and item_in_list_B therefore become the dummy variables for items
        in list A and items in list B respectively. 
            
Range function
    The range function is a shortcut for generating a list. A range function can be denotated three
    ways:
    
        1. range(stop)
        2. range(start, stop)
        3. range(start, stop, step)
        
    The start argument tells the range function from which integer to begin the list.
    The stop argument tells the function the upper integer (which is not included).
    The step argument tells the range function how much to increase by in each step.
    
    NOTE: The default start for a range function is 0, NOT 1. 
            
List-Concantenation
    If you want to derive a larger list which is a combination of two lists, simply use:
    
        x = y+z
        
    where x is the new list, and y and z are the lists added together. The list x will therefore
    contain the items in y, and the items in z in that order. Thus if we had
    
        x = z+y
        
    then the list items of x would have the list items of z first, and then the list items of
    y. 

    Joining
        When we have a list of string for example, and we want to remove the commas between
        them, then we use the notation:
        
        " ".join(list_name)
        
        OR
        
        "---".join(list_name)
        
        Which will remove the commas between each item, making it seem as if it were a single
        string. I'm guessing that you can in fact put anything in between "" and it will
        place your input between the items. 
            
While Loop
    A while loop will continue to execute the nested blocks of code until its condition is
    false:
    
        while condition:
            """Code"""
        
        
    While - else
    
        While loops can also have a naturally associated else statement. This else statement
        will be executed the moment the while loop's condition becomes false. However,
        the else statement will not print if we put a break in the while loop first. To illustrate,
        take the below example
        
            while [condition1]:
                "Code"
                
                if condition2:
                    break
                    
            else:
            
                "Code"
                
        Here, the while loop will continue to run until either condition1 is false, in which case
        the else statement will run, or if condition2 is true, in which case the break is implemented
        and the else statement is therefore not printed. 
        
        
List Comprehension
    In some cases, where you want to create a new list where the items follow a general pattern, you can simply the following notation:
    
        new_list = [variable_name for [something to do with the pattern of x]], to illustrate, consider the following example
        
            new_list = [x for x in range(1,100) if(x%3 == 0)]
            
            In this example, the new list will consist of items x, with x holding values from 1 to 100, but only if they are fully divisible by three.
            
            
Bitwise operation and Binary Counting

Note: Print statements will always print a number in integer form unless you specify it prints in binary form through bin(number)

    Binary Counting
        Each place in a number can only hold two values: 1 or 0, 1 indicating that the value of the place is true, and 0 indicating that
        the value is 0.
        Each place however, instead of representing some power of 10, represents some power of 2. To illustrate, consider an ordinary number:
    
            7654321
        
        Here, going from the right, we go: 1*10^0 (the ones), 2*10^1 (10s), 3*10^2 (hundreds) and so on. With binary counting, we use the following:
    
            10101010
        
        Here, going from the right, we have a zero in the 1s, a 1 in the 2s, a zero in the 4s, a 1 in the 8s and so on. To get the full number represented by the binary
        number, we add together all the digits in their places. so here, we would have 2+8+32+128 = 170
    
    
    Writing and Printing in Binary
        To write in binary, use the notation:
    
            "0b_____" where ____ represents the number in binary form.
        
        To convert a number to binary form, use:
    
            bin(number)
        
        
    Converting from Binary to integer
    Use:
    
            int("____", 2)
        
        Here, we use the int function in a specific manner, we pass it a string "____" (representing the binary number) and tell the int function what its base is,
        in this case, 2, and therefore causes the string to be converted to normal integer form.
        
    REMEMBER: A print command almost always prints in integer form unless specified otherwise. 
    
    
    Sliding
    
        We can increase or decrease the value of a binary number through the following notation:
        
            Slide left (increasing):
            
                0b____ << n
                
            Through the left slide, the original binary number, 0b____, is increased as the 1s and 0s will be translated n places left. To illustrate:
            
                0b0010010 << 2 == 0b1001000 == 128+8 = 136
            
            
            Slide right(decreasing):
            
                0b____ >> n
                
            Through the right slide, the original binary number, 0b____, is decreased as the 1s and 0s will be translated n places right. To illustrate:
            
                0b11011 >> 3 == 0b00011
                
            REMEMBER: If a value "falls off" the right edge of the 2 bit placeholder, then it no longer exists. For instance, in the example above, the original
            1s at the 1 and 2s place values moved beyond the minimal placevalue, so they no longer count. 
                
        NOTE: We can easily use variables as substitutes for the actual numbers, as we do for ordinary integers, and manipulate the variables instead.
        
        
    Operators
    
        The Bitwise AND operator (&)
            The Bitwise AND operator compares the values in each place value between two number and returns a 1 iff there is a 1 in the same place value
            for both numbers. The Bitwise And operator is implemented like this:
            
                0b_____ & 0b______
                
            To illustrate
            
                0b1101 & 0b0001 == 0b0001
                
            This is because between the two numbers, the only place where there is a 1 is in the very last place.
            
            
        The Bitwise OR operator (|)
            The Bitwise OR operator compares the values in each place value between two numbers and returns a 1 if there is a one at a given place value
            for ANY of the two numbers.
            - The OR operator is implemented as follows:
            
                0b____ | 0b____
                
            To illustrate, consider the following:
            
                0b1010 | 0b0111 == 0b1111
                
            This is because in all place values, between the two numbers, there is always a 1. Note that it doesn't matter if 1s overlap between the numbers, as long
            as there is a 1 in a place value, then there will be a 1 in the corresponding product number at that place value:
            
                0 | 0 = 0
                0|1 = 1
                1|0 = 1
                1|1 = 1
                
        
        The Bitwise XOR operator (^)
            The bitwise XOR operator compares the values in each place value between two number and returns a 1 iff there is only a single 1 in a given place value
            between the two numbers.
            - The XOR operator is implemented as follows:
            
                0b____ ^ 0b____
                
            To illustrate:
            
                0b10011 ^ 0b10101 == 0b00110
                
            Here, notice that the 1s in the left-most place (the 32 bit place value) cancel out because they ARE BOTH 1s - the XOR operator requires that there
            be a 1 in the place value, but only in a single number. 
        
        
Objects
    
    Objects are essentially #things? in Python which contain both data and functions. The data and function of objects are called the attributes and methods respectively. 
    
    Objects in Python are declared in the following manner:

        class [object_name](object):
        
            def __init__(self, [other_argument_1], [other_argument_2]):
            
                self.attribute_1 = other_argument_1
                self.attribute_1 = other_argument_2
                etc. 
                
            #Note that init is really just a method to "boot up" or initialise the object.
            
            def method1(self, [other_argument_1]...):
            
            
                #Block of Code
                
                
           
           
     Access
     To access an object's attributes or methods, we use the "." operator as such:

            object.attribute_1
            
            and for the method
            
            object.method1([other_argument_1])
            
            #note how we don't actually need to pass in self again when calling the object method. 
            
            
            
            
            
    The properties of objects can in fact be manipulated or changed after their initialisation. 
