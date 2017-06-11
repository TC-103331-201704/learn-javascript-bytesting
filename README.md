Introduction to Javascript by testing
=====================================

A small course introducing Javascript that uses test
to introduce and teach concepts.


Setup
-----

1. Clone this repository

### With Node (preferred)

2a. Install node (recommended by using https://github.com/creationix/nvm), 

3a. Install live-server

    $ npm install -g live-server

4a. Execute live-server in the repository directory

    $ live-server .


### With Chrome (less powerful)

2b. Install the Chrome extension "Web Server for Chrome"
    - https://chrome.google.com/webstore/detail/web-server-for-chrome/ofhbbkphhbklhfoeikjpcbhemlocgigb?hl=en

3b. Serve the cloned directory and show index.html


### Custom

2c. Use any webserver already installed in your computer.

3c. Serve the cloned directory and show index.html


How To
------

Once opened you will see tens of tests failing.
Your task is make them pass.

Tests are inside spec/ directory. 
Each spec file is numbered.
Start with the lower number and go for the next
when it passes. Repeat until all tests passes.

Author
------

David Rodenas (@drpicox)


    Introduction
        You must make all tests pass like this one
        Your first test to pass, change only expect(contents)
        Use "hint" if you're get stuck

    Numbers
        constants
            1,2,5000 are numbers
            1.2 -2.3 1e2 are also numbers
            numbers are IEEE-754, they have low resolution
            1/0 gives Infinity
            gives NaN when something goes wrong, example 0 divided by 0
        operations
            has addition
            has substraction
            has multiplication
            has division
            has reminder
            reminder of negative numbers is also signed
        comparisons
            a < b returns true if a is less than b
            a <= b returns true if a is less than b or equal to b
            a >= b returns true if a is greater than b or equal to b
            a > b returns true if a is greater than b
            a === b returns true if both numbers are the same
            a === b returns false if one is number but the other is not
            a !== b returns true if both numbers are the different
            a !== b returns true if one is number but the other is not
            never use a == b (two equals) you cannot trust it
            never use a != b (one equal) you cannot trust it
        methods
            toFixed converts a number into a string with a fixed number of decimals
        Math
            Math.max gets the maximum of two numbers
            Math.min gets the minimum of two numbers
            Math.floor gets the number without decimals rounded down
            Math.ceil gets the number without decimals rounded up
            Math.round gets the nearest integer
            Math.round gets the nearest integer (tied negatives go up)
        Cast to number
            use Number(string) to convert a string to a number
            Number(string) gives NaN if string cannot be converted
        NaN
            NaN is NOT a NaN
            use isNaN(number) to know if it is NaN

    Strings
        constants
            "hello", "a", "long word" are constans
            character is a string with length 1
        encoded as UCS-2
            each position is 16bits and most characters are length 1
            some characters requires has double length
        operators
            a + b concatenates two strings
        comparisons
            a < b returns true if a is less than b
            a <= b returns true if a is less than b or equal to b
            a >= b returns true if a is greater than b or equal to b
            a > b returns true if a is greater than b
            a === b returns true if both numbers are the same
            a === b returns false if one is number but the other is not
            a !== b returns true if both numbers are the different
            a !== b returns true if one is number but the other is not
            never use a == b (two equals) you cannot trust it
            never use a != b (one equal) you cannot trust it
        methods
            slice(begin, end) gets a substring from the string
            slice(begin) gets the substring starting at begin
            slice(-begin) gets the substring starting at the last character count
            indexOf finds the first occurrence of a substring
            indexOf returns -1 if no matching
            includes true if there is an occurrence of a substring
            includes returns false if no matching
            toUpperCase converts a string to uppercase
            toLowerCase converts a string to lowercase
        cast to String
            can convert any object to string with String()

    Booleans
        constants
            false and true are the only existing booleans
        operations
            logical and
            logical or
            not
        cast
            use Boolean() to convert from truthy/falsy booleans to boolean
            use Boolean() to convert from truthy/falsy objects to boolean
            use Boolean() to convert from truthy/falsy strings to boolean
            use Boolean() to convert from truthy/falsy numbers to boolean
        if conditions follows truthy/falsy rules
            example with "3"
            example with 0
            example with undefined
            example with "false"

    Arrays
        constants follows JSON rules
            [1,2,3], [42,"sense",["of", "life"]], []
        get set
            you can use [index] to read any position
            you can use [index] to set any position
            you can mix types
            you get undefined if you read an unset number
            you can set any position (grows dinamically)
            all positions between the setted and last become undefined
        length
            length returns the actual length of the array
            length can be set to shrink the array
            length can be set to enlarge the array filled with undefined
            length grows when more elements are added
        can mutate
            unmutated array
            can behave as a stack
                from behind
                    push adds a new element to the end
                    pop removes the last element
                    pop returns the value of the last element
                from head
                    unshift adds a new element to the beggining
                    shift removes the first element
                    shift returns the value of the first element
            can behave as a queue
                you can add elements in the end and get them from the front
                you can add elements in the head and get them from the tail
            splice
                splice can insert numbers in any position
                splice can remove numbers in any position
            sort
                sort orders array contents
                sort returns the array itself ordered
                sort orders strings by default, if no, it imagines strings
                sort accepts a ordering function
            reverse
                reverses the contents of an array
                returns the reversed array itself
        non mutating operations
            slice
                slice copies an array
                slice(begin,end) can copy a part of an array
                slice(position) copies from the position to the end
                slice(-position) copies from the last nth position to the end
            concat
                concatenates another array
                does not modifies the array
            iterators
                filter selects elements from the array
                map applies a function to each element
                reduce(fn, initial) applies an accumulator operation
                every evaluates if a condition is satisfied by all elements
                some evaluates if a condition is satisfied by any elements
                forEach executes a function for each element
                none modifies the array
            finders
                indexOf(value) looks for the same exact value position
                indexOf(value) returns -1 if the element does not exists
                find returns the first element that satisfies a condition
                find returns undefined if no element satisfies the condition
                findIndex returns the position of the first element that satisfies a condition
                findIndex returns -1 if no element satisfies the condition

    Objects
        JSON
            {} is an empty object
            {hello: "world"} is an object with one field
            JSON.parse converts JSON strings to obejcts
            JSON.stringify converts any object to JSON
        get set
            you can use . to get the value of a property
            you can use [string] to get the value of a property
            you can use . to set the value of a property
            you can use [string] to set the value of a property
            return undefined if the property is not defined
            you can add dynamically any property
            you can use delete to remove properties
        walk
            Object.keys() gets an array with all the property keys
            Object.values() gets an array with all property values
        assign
            assign merges two or more objects into the first
            assign returns the target object
            can be merged more than one object
            if a property is duplicated keeps the last value
            can be used to copy an object

    Functions
        short notation
            () => {} is the shortest function
            (a,b) => {} accepts arguments
            a => {} is a shorthand for one argument
            () => n returns n
            n => n is identity
            (a,b) => a+b sums two numbers
            () => ({ hello: "world" }) requires parenthesis to return a constant object
            () => { /*code*/ } accepts any arbitrary code inside brackets
        large notation
            function() {} was the shortest function
            function(a,b) {} accepts arguments
            function(a) {} there is no shorthand for one argument
            function() { return n; } returns n
            function name() { … } can have named
            function (n) { return n; } is identity
            function (a, b) { return a + b; } sums two numbers
            function() { return { hello: "world" }; } requires nothing special to return a constant object
            function() { /*code*/ } accepts any arbitrary code inside brackets
        missmatching parameters / returns
            ignores extra parameters
            converts missing parameters into undefined
            always returns something, returns undefined by default
            returns return undefined if no value specified
        closures
            functions can have children functions
            children functions can read parent variables
            functions can return functions
            parent variales live after parent finishes
            parent variales are duplicated in each function call
        return standarized bug
            return does not need ; to finish

    Classes
        are defined using class keyword
        new creates new instances
        class instances are objects
        you can get/set properties to class object like any object
        instance methods are defined in the class
        instance methods can read instance properties through this
        without this it reads parent variables
        uses this to call to its own methods
        without this it calls a parent function
        can create dynamically new own properties throw this
        there are no private properties
        constructor is a special funcion called constructor
        has inheritance using extends
        you can call super constructor with super
        you can call super method with super
        you can use instanceof to know if an object is an instance of a class
        you can use instanceof to know (true/false) if an object is an instance of a class or inheritancy
        () => {} shorthand functions allows to use this
        () => {} shorthand functions preserves this
        function() {} long notation uses this value is undefined