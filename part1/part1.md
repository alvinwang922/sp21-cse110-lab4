## Part 1a)

var declaration:
1) Line 9 prints "values added: 20"
2) Line 13 prints "final result: 20"

let declaration:
1) Line 9 prints "values added: 20"
2) Line 13 returns an error because we declared the "result" variable with let, so it can only be accessed within the block. However, in line 13, we are trying to access "result" outside of the block, so it returns an error since "result" doesn't exist in that block.

const declaration:
1) The code returns an error because we are using the const keyword to initialize "result," meaning it can not be reassigned. However, at line 7, we attempt to reassign it, which returns an error. Thus, we never gets to line 9.
2) Similar to before, the code returns an error because we are using the const keyword to initialize "result," meaning it can not be reassigned. However, at line 7, we attempt to reassign it, which returns an error. Thus, we never gets to line 13.

## Part 1b)
1) At line 12, the number "3" will be printed because the length of the prices array is 3, so after it runs through the loop for index 2, the variable i increments to 3, and since 3 not less than prices.length, it breaks out of the for loop when i is 3, and since line 12 prints i, it prints the number "3".
2) At line 13, the number "150" will be printed because during the last iteration of the for loop, the variable "discountedPrice" is set to "prices[i] * (1 - discount), and since i = 2 at this point, that equals 300 * (1 - 0.5)," which is 150. Thus, "150" is printed at line 13.
3) At line 14, the number "150" will be printed because during the last iteration of the for loop, the variable "finalPrice" is set to "Math.round(discountedPrice * 100) / 100," and since discountedPrice = 150 at this point, that equals "Math.round(150 * 100) / 100," which is 150. Thus, "150" is printed at line 14.
4) This function will return the array of [50, 100, 150]. This is because at each iteration of the for loop, we push the current value of "finalPrice" into the array "discounted" and we return this array at the end. Throughout the three iterations of the for loops, the values of "finalPrice" are just half of the value at index i in the "prices" array, so at the end, the values "50", "100", and "150" are pushed into the "discounted" array. Since this function returns "discounted," it will return this array of [50, 100, 150].
5) An error will occur at line 12, since we initialized "i" with let, so "i" can only be referenced within that block. Since line 12 is outside that block and we are trying to access it, line 12 will return an error.
6) Similar to problem 5, an error will occur at line 13, since we initialized "discountedPrice" with let, so "discountedPrice" can only be referenced within that block. Since line 13 is outside that block and we are trying to access it, line 13 will return an error.
7) At line 14, the number "150" will be printed. As explained before, the value of "finalPrice" after the for loop runs is "150." Since we initialized "finalPrice" in the outer block, the function block, using let, we can still access "finalPrice" on line 14, which is why there is no error.
8) This function will return the array of [50, 100, 150]. As explained before, after the for loop finishes running, the "discounted" array is populated with "50", "100", and "150." Since we initialized "discounted" in the outer block, the function block, using let, we can still access "discounted" on line 16 when returning it, which is why there is no error.
9) An error will occur at line 11, since we initialized "i" with let, so "i" can only be referenced within that block. Since line 11 is outside that block and we are trying to access it, line 11 will return an error.
10) At line 12, the number "3" will be printed because we initialized "length" as the length of "prices," and since we pass in [100, 200, 300] for prices, which has length 3, the value or "length" is "3." It is also initialized with "const," so it can't be reassigned or redeclared. Thus, when we print "length," it will print the number "3."
11) This function will return the array of [50, 100, 150]. This is because at each iteration of the for loop, we push the current value of "discountedPrice" into the array "discounted" and we return this array at the end. Throughout the three iterations of the for loops, the values of "discountedPrice" are just half of the value at index i in the "prices" array, so at the end, the values "50", "100", and "150" are pushed into the "discounted" array. Since this function returns "discounted," it will return this array of [50, 100, 150]. Even though "discounted" was initialized using the const keyword and something is changed, no errors are returned because we are never reassigning or redeclaring "discounted," we are just adding to the array that it already points to. Thus, as mentioned before, the function will return the array of [50, 100, 150] without errors.
12) A) student.name
    B) student["Grad Year"]
    C) student.greeting()
    D) student["favorite teacher"].name
    E) student.courseLoad[0]
13) A) "32", because the integer 2 maps to its string representation "2" and "3" + "2" is "32"
    B) 1, since you can't subtract strings, so "3" becomes 3 and 3 - 2 = 1
    C) 3, since null maps to 0 and 3 + 0 = 3
    D) "3null", since null maps to the string "null" and "3" + "null" = "3null"
    E) 4, since true maps to 1 and 1 + 3 = 4
    F) 0, since false maps to 0 and null maps to 0 and 0 + 0 = 0
    G) "3undefined", since undefined maps to the string "undefined" and "3" + "undefined" = "3undefined"
    H) NaN, since "3" maps to 3 for subtraction but undefined maps to NaN and subtraction involving NaN results in an answer of NaN
14) A) true, since "2" becomes 2 and 2 > 1 is true
    B) false, since the first string starts with "2" and the second string starts with "1," and lexicographically, "2" < "1" is false, so "2" < "12" is false
    C) true, since "==" converts types when comparing, so "2" becomes 2 and 2 == 2 is true
    D) false, since "===" makes comparisons without type conversion, and since 2 is an integer and "2" is a string, 2 === "2" is false
    E) false, since true becomes 1 and 1 == 2 is false
    F) true, because Boolean(2) is true without conversion and true === true
15) "==" checks equality with type conversions whereas "===" checks equality without type conversions
16) part1b-question16.js
17) The result will be "[2, 4, 6]." This is because when we pass in a number to "doSomething," it returns the number times 2. Thus, when calling "modifyArray" on "[1, 2, 3]" and "doSomething" (function stored in a variable), it creates a new array, "newArr." For each element in the array that is passed in, 1, 2, and 3, it passes this number into "doSomething," which returns the value doubled, and this new value is pushed in "newArr." Thus, "newArr" becomes an array that is just the array that is passed in except each value in the array that is passed in is doubled. This "newArr" is returned at the end of "modifyArray," giving us the result of "[2, 4, 6]" for this example.
18) part1b-question18.js
19) The output is as follow (the last line, 2, is printed 1 second after everything else):
    1
    4
    3
    2
    This is because when the function is executed, 1 is printed immediately. Then, 2 is printed, but with a 1 second delay, and 3 is printed with a 0 second delay. In the last line of the function, 4 is printed immediately. There is a setTimeout for printing 2 and 3, in which there is a 0 second delay for printing 3 and a 1 second delay for printing 2. The 0 second delay still causes the 3 to be printed immediately after the 4, though, since the 4 is printed immediately without delay. However, they display on console at pretty much the same time, just 4 comes before 3 in the order they are printed. Lastly, one second after the function starts, 2 is printed.