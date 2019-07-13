# Functions lab 1

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1√

Complete the function so that it will print out total cost after tax. Make sure to **call the function** afterwards.

```swift
let itemCost = 45.0
let nyTax = 0.08775

func totalWithTax() {

}
```

```swift
let itemCost = 45.0
let nyTax = 0.08775

func totalWithTax() -> Double {
return (itemCost * nyTax) + itemCost
}

print(totalWithTax())
```

Then, modify the function you implemented to have a return type of `Int`, and use an external name that looks more readable. Function calls should look something like "total cost of the item after tax"

## Question 2√

Convert the the following if/else statement below into function with a `String` return type.

```swift
let todaysTemperature = 72

if todaysTemperature <= 40 {
    print("It's cold out.")
} else if todaysTemperature >= 85 {
    print("It's really warm.")
} else {
    print("Weather is moderate.")
}
```
```swift
let todaysTemperature = 72

func temp (_ currentTemp:Int) -> String {

var tempResult = String()

if currentTemp <= 40 {
tempResult = "It's cold out."
} else if currentTemp >= 85 {
tempResult = "It's really warm."
} else {
tempResult = "Weather is moderate."
}

return tempResult
}
temp(todaysTemperature)
```


## Question 3√

Write a function named `min2` that takes two `Int` values, `a` and `b`, and returns the smallest one.

Function Definition
`func min2(a: Int, b: Int) -> Int`

Example:
Input: `min2(a:1, b:2)`

Output: `1`

```swift
func min2(a: Int, b: Int) -> Int {
var minimum = Int()
if a < b {
minimum = a
}
if b < a {
minimum = b
}
return minimum
}

min2(a:1, b:2)

```


## Question 4√

Write a function that takes an `Int` and returns its last digit. Name the function `lastDigit`. Use _ to ignore the external parameter name.

Function Definition:
`func lastDigit(_ number: Int) -> Int`

Example:
Input: `lastDigit(12345)`

Output: `5`

```swift
func lastDigit(_ number: Int) -> Int {

let value = number % 10
return value
}
print(lastDigit(12345))
```

## Question 5√

Write a function that takes in any two positive integers and return the sum.

```swift
func sumOf2PositiveInt (_ num1:Int , _ num2:Int) -> Int {
let sum = num1 + num2
return sum
}
sumOf2PositiveInt(46, 99)
```
## Question 6√

Write a function takes in any number grade and returns a corresponding letter grade.

| Number Grade | Equivalent Letter Grade |
| :--------: | :---------: |
| 100 | A+ |
| 90 - 99 | A |
| 80 - 89 | B |
| 70 - 79 | C |
| 65 - 69 | D |
| Below 65 | F |

```swift
func gradeValue (_ grade:String) -> String {
var studentGrade = String()

switch grade {
case "A+":
studentGrade = "100"
case "A":
studentGrade = "90-99"
case "B":
studentGrade = "80-89"
case "C":
studentGrade = "70-79"
case "D":
studentGrade = "65-69"
case "F":
studentGrade = "Below 65"
default :
studentGrade = "Please enter a grade value of A+ A,B,C,D or F"

}
return studentGrade
}
print(gradeValue("A+"))
```

## Question 7√

Make a calculator function that takes in three parameters (two numbers and one operator) and returns the answer of the operation.
```swift
Operator parameter: (+, -, x, /)
func calculator (value1:Int , value2:Int, char:String) -> Int? {
switch char {
case "+":
return value1 + value2
case "-":
return value1 - value2
case "x":
return value1 * value2
case "/":
return value1 / value2
default :
return nil
}
}
calculator(value1: 4, value2: 5, char: "+")
```

## Question 8√

Write a function so that it will print out **total cost after tip.**

```swift
let mealCost = 45
let tipPercentage = 0.15

//Write your code below

let myFinalCost = totalWithTip() //Fill in the arguments
```
```swift
let mealCost = 45
let tipPercentage = 0.15

//Write your code below

func totalWithTip (_ cost:Int, _ tip:Double) -> Double {
let totalResult = (Double(cost) * tip) + Double(cost)

return totalResult
}

let myFinalCost = totalWithTip(mealCost, tipPercentage)
```

Write a function that will print out **total cost after tip and tax.**

```swift
let taxPercentage = 0.09

//Write your code below

let myFinalCostWithTipAndTax = totalWithTipAndTax() //Fill in the arguments in function
```
```swift
let mealCost = 45
let tipPercentage = 0.15
let taxPercentage = 0.09

//Write your code below

func totalWithTip (_ cost:Int, _ tip:Double, _ tax:Double) -> Double {
let totalResult = (Double(cost) * tip) + (Double(cost) * taxPercentage) + Double(cost)

return totalResult
}

let myFinalCost = totalWithTip(mealCost, tipPercentage, taxPercentage)

```

## Question 9√

Implement a function named `repeatPrint` that takes a string `message` and a integer `count` as parameters. The function should print `message` `count` number of times and then print a newline.

Example:
Input: `repeatPrint(message: "+", count: 10)`

Output: `++++++++++`

```swift
func repeatPrint (message: String, count: Int) -> String {
var result = String()
for _ in 1...count {
result += message
}
return result

}
print(repeatPrint(message: "+", count: 10))
```

## Question 10√

Write a function named `first` that takes an Int named n and returns an array with the first n numbers starting from 1.

Function Definition
`func first(_ n: Int) -> [Int]`

Example:
Input: `first(3)`

Output: `[1, 2, 3]`

```swift
func first(_ n: Int) -> [Int] {
var result = [Int]()
for i in 1...3 {
result += [i]
}
return result
}


print(first(3))
```

## Question 11√

Write a function that prints the numbers from 1 to x, except:

If the number if a multiple of 3, print `"Fizz"` instead of the number
If the number is a multiple of 5, print `"Buzz"` instead of the number
If the number is a multiple of 3 AND 5, print `"FizzBuzz"` instead of the number
Your function should take in one parameter: x (the number to count up to)

```swift
func numFizzBuzz (number: Int) -> [String] {
var result = [String]()
for num in 1...number {
if num % 3 == 0{
result += ["Fizz"]
} else if num % 5 == 0 {
result += ["Buzz"]
}else if num % 3 == 0 && num % 5 == 0 {
result += ["FizzBuzz"]
}else {
result += [String(num)]
}
}
return result
}
print(numFizzBuzz(number: 50))

```
## Question 12√

Write a function named `reverse` that takes an array of integers named `numbers` as a parameter. The function should return an array with the numbers from `numbers` in reverse order.


Example:
Input: `reverse([1, 2, 3])`

Output: `[3, 2, 1]`

```swift
var arrayInt = [1,2,3]
func reverse (number:[Int]) -> [Int] {
let arrayReversed = Array(number.reversed())
return arrayReversed
}
reverse(number: arrayInt)
```
## Question 13

Write a function that prints out the most frequently appearing Int in an array of Int.


## Question 14√

Write a function that sums all the even indices of an array of Ints.

```swift
var arrayValue = [1,2,3,4,5,6,7,8,9]

func sumOfAllEvenNum (number:[Int]) -> Int {
var  result = Int()
for (index, value) in arrayValue.enumerated() where index % 2 == 0{
result += value
}
return result
}
sumOfAllEvenNum(number: arrayValue)

```
## Question 15

Write a function that flips a dictionary.  All of the keys are now values and all of the values are now keys.

Example:
Input: `[1: "hi", 5: "bye:]`

Output: `["hi": 1, "bye": 5]`


## Question 16

Write a function that finds the person with the second highest test score in a Dictionary that maps names to scores.

Example:
Input: `["Person 1": 83, "Person 2": 74, "Person 3": 82]`

Output: `"Person 3"`

## Question 17√

Write a function that determines if a value is inside of array.

```swift
var arrayValue = [3,5,97,6,5,4]
var check = 5
func isItInside (array:[Int], number:Int) -> Bool {
var result = Bool()
if array.contains(number){
result = true
}else {
result = false
}
return result
}
isItInside(array: arrayValue, number: check)

```


## Question 18√

Write a function takes an `Int` as input, and returns true if it is even, or false if it is odd.
Using your new function, write code that prints out whether `dieRoll` is even or odd:

`let dieRoll = Int(arc4random_uniform(6) + 1)`

```swift
let diceRoll = Int(arc4random_uniform(6) + 1)

func rollResult (number:Int) -> Bool{
var result = Bool()

if number % 2 == 0 {
result = true
}else {
result = false
}
return result
}
rollResult(number: diceRoll)
```

## Question 19√

Write a function that takes `[Int]` as input. It should return the largest Int in the array.

Using your function from the first step, use String interpolation to print a sentence that states what the largest Int in `myArray` is.

`let myArray = [3,5,1,3,532,1,4,91,20,30,92,143]`

```swift
let myArray = [3,5,1,3,532,1,4,91,20,30,92,143]

func largestValue (array: [Int]) -> Int {
var value = Int()
if let result = array.max() {
value = result
}
return value
}
largestValue(array: myArray)
```

If you haven't already done so, write a function that takes in an Int and returns whether that number is even or odd. Use that function to print a sentence that states whether the largest Int in `myArray` is even or odd.

```swift
let myArray = [3,5,1,3,532,1,4,91,20,30,92,143]

func largestValue (array: [Int]) -> String {
let largestValueOddOrEven: String
var value = Int()
if let result = array.max() {
value = result
}
if value % 2 == 0 {
largestValueOddOrEven = "the largest Int in myArray is EVEN "
}else {
largestValueOddOrEven = "the largest Int in myArray is ODD "
}

return largestValueOddOrEven
}
print(largestValue(array: myArray))
```
## Question 20√

Write a function that takes a String as input and returns the number of characters in the string

Using your function, print how many characters are in myString:

`let myString = "Swift is a new programming language for iOS, OS X, watchOS, and tvOS apps that builds on the best of C and Objective-C, without the constraints of C compatibility."`

```swift
func characterCount (sentence:String) -> Int {
var counter = Int()
for char in sentence where char != " "{
counter += 1
print(char, terminator: "")
}
return counter
}
characterCount(sentence: myString)

```

## Question 21√

Write a function that counts how many characters in a String match a specific character.  (e.g: count how many "a"s are in a String, or count how many ","s are in a String.

Example:
Input:
```swift
let testString = "This is a test string for your code"
let targetCharacter: Character = "i"
```
Sample output: `3`

```swift

func characterCheck (_ testString:String,_ targetCharacter: Character) -> Int {

var counter = Int()
for i in testString where targetCharacter == i{
counter += 1
}
return counter
}
characterCheck(testString, targetCharacter)
```


## Question 22√

Write a function that counts how many characters in a String match one of several possible characters.  (e.g: count how many vowels are in a String, or count how many "a"s "b"s and "c"s are in a Sting)

Example:
Input:
```swift
let inputString = "This one is a little more complicated"
let targetCharacters: [Character] = ["a","e","i","o","u"]
```
```swift
func vowelsCheck (_ inputString:String,_ targetCharacter: [Character]) -> Int {
var  counter = Int()
for vowel in targetCharacter {
for letter in inputString {
if vowel == letter {
counter += 1
}
}
}
return counter
}
vowelsCheck(inputString, targetCharacters)
```

Output: `13`


## Question 23

Write a function that returns the number of unique Ints in an array of Ints.

Example:
Input: `let inputArray2 = [3,1,4,1,3,2,6,1,9]`

Output: `4`

//Explanation: 2, 4, 6, 9 are unique in the array. Every other number is not unique.


## Question 24√

Write a function that converts a binary number into decimal. The binary number will be given as an array of Ints.

Example:
Input: `let binaryArray = [1,0,1,1,1,0,1]`

Output: `93`

```swift
func binaryConverter (_ binaryArray: [Int]) -> Decimal {
var binaryCode = Decimal()
let arrayReversed = Array(binaryArray.reversed())
for (index, value) in arrayReversed.enumerated() where value == 1 {
print(pow(2,index))
binaryCode += pow(2,index)
}
return binaryCode
}
binaryConverter(binaryArray)
```

## Question 25√

Write a function named `timeDifference`. It takes as input four numbers that represent two times in a day and returns the difference in minutes between them. The first two parameters `firstHour` and `firstMinute` represent the hour and minute of the first time. The last two `secondHour` and `secondMinute` represent the hour and minute of the second time. All parameters should have external parameter names with the same name as the local ones.

Example:
Input: `timeDifference(firstHour: 12, firstMinute: 3, secondHour: 13, secondMinute: 10)`

Output: `67`

```swift
func timeDifference (firstHour:Int, firstMinute:Int, secondHour:Int, secondMinute:Int) -> Int {

let timeDiff = abs((firstHour * 60) - (secondHour * 60)) + abs(firstMinute - secondMinute)

return timeDiff
}
timeDifference(firstHour: 12, firstMinute: 3, secondHour: 13, secondMinute: 10)
```

## Question 26√

Write a function called `filterOdd` that takes an array of ints and returns it with just the even numbers.

Example:
Input:  `filterOdd(arr: [1, 2, 3, 4, 5, 6, 7, 8])`

Output: `[2, 4, 6, 8]`

```swift
func filterOdd (arr:[Int]) -> [Int] {
var evenValues = [Int]()
for number in arr where number % 2 == 0 {
evenValues += [number]
}
return evenValues
}
filterOdd(arr: [1, 2, 3, 4, 5, 6, 7, 8])

```

## Question 27√

Write a function called `doubleIt` that takes an array of ints and returns it with all the elements doubled.

Example:
Input: `doubleIt(arr: [1, 2, 3, 4])`

Output: `[2, 4, 6, 8]`

```swift
func doubleIt (arr:[Int]) -> [Int] {
var doubled = [Int]()
for number in arr {
doubled += [number * 2]
}
return doubled
}
doubleIt(arr: [1, 2, 3, 4])

```

Then write a function called `multiplyBy` that takes an array of ints and an int n that will return the array with all the elements multiplied by n.√

Output:  `[4, 8, 12, 16]`

```swift
func multiplyby (arr:[Int], multiplier:Int) -> [Int] {
var output = [Int]()
for number in arr {
output += [number * multiplier]
}
return output
}
multiplyby(arr: [1, 2, 3, 4], multiplier: 4)
```


## Question 28√

Write a function called `unwrap` that takes an array of optional ints and returns an array with them unwrapped with any nil values removed.

Example:
Input:  `unwrap(arr: [nil, 7, 4, nil, 43, 11, nil, 2])`

Output: `[7, 4, 43, 11, 2]`

```swift
func unwrap (arr:[Int?]) -> [Int] {
var unWrappedArray = [Int]()
for number in arr {
if let unwrapped = number {
unWrappedArray += [unwrapped]
}
}
return unWrappedArray
}
unwrap(arr: [nil, 7, 4, nil, 43, 11, nil, 2])
```

## Question 29√

Write a function that takes an array of bools and returns a dictionary that maps the bools to how many times they appear in the array.

Example:
Input:  `countBools(arr: [true, true, false, true, false, true])`

Output: `[false: 2, true: 4]`

```swift
func countBools (arr:[Bool]) -> [String: Int] {
var dict = [String: Int]()
var addTrue = Int()
var addFalse = Int()
for result in arr {
if result == true {
addTrue += 1
}else {
addFalse += 1
}
dict = ["false": addFalse, "true": addTrue]
}
return dict
}
countBools(arr: [true, true, false, true, false, true])

```


## Question 30

Write a function that takes a string as input and returns a dictionary that maps each unique character to how many times they appear in the string.

Example:
Input:  `countCharacters(str: "Hello, World!")`

Output: `["H": 1, "r": 1, "!": 1, "e": 1, "o": 2, "l": 3, ",": 1, " ": 1, "W": 1, "d": 1]`


## Question 31√

Write a function that takes this dictionary of baseball teams by ID and returns an array of tuples that contain each team's ID and name.

`let baseballTeamsById = [1001:"Mets", 1002:"Yankees", 1003:"Rays", 1004:"Marlins"]`

Example:
Input:  `dictToTuples(dict: baseballTeamsById)`

Output: `[(.0 1003, .1 "Rays"), (.0 1001, .1 "Mets"), (.0 1004, .1 "Marlins"), (.0 1002, .1 "Yankees")]`

```swift
let baseballTeamsById = [1001:"Mets", 1002:"Yankees", 1003:"Rays", 1004:"Marlins"]

func dictToTuples (dict: [Int:String]) -> [(Int,String)] {
var baseballtuple = [(Int,String)]()
for (key, value) in dict {
baseballtuple += [(key,value)]
}
return baseballtuple
}
print(dictToTuples(dict: baseballTeamsById))


```

## Question 32√

Write a function that checks if a String is a [Palindrome](https://en.wikipedia.org/wiki/Palindrome)

```swift
var phrase = "abcecba"

func Palindrome (word:String) -> Bool {
if word == String(word.reversed()) {
return true
}else {
return false
}
}
Palindrome(word: phrase)
```
## Question 33√

Write a function that checks if a String is a [pangram](https://en.wikipedia.org/wiki/Pangram)

```swift
var alphabet = "abcdefghijklmnopqrstuvwxyz"
var one = "The quick brown fox jumps over the lazy dog"
var two = "The quick brown fox jumped over the lazy dog"

func pangram (sentence:String , alphabets:String) -> String {
let setSentence = Set(sentence)
if setSentence.isSuperset(of: alphabets){
return "it is a Pangram"
}else {
return "it is NOT a Pangram"
}
}
pangram(sentence: one, alphabets: alphabet)

```

## Question 34√

Write your own `min()` and `max()` functions for an Array of Ints

```swift
var arraySet = [4,5,67,755,78,554,3,56,7,5,1,9]
func largeOrLess (array:[Int]) -> String {
var result = String()
let biggestInt = array.max()
if let max =  biggestInt {
if max >= 1000{
result = "you score of \(max) is High"
}else if max >= 500 && max <= 800 {
result = "you score of \(max) is Moderate"
}else {
result = "you score of \(max) is kind of Low. work harder"
}

}
return result
}
largeOrLess(array: arraySet)

```
## Question 35√

Given two arrays of Ints, write a function that tells you all the values they have in common.
```swift
var oneArray = [2,5,6,7,88,6,43,234]
var twoArray = [2,4,5,6,8,76,43,21]

func commonValue (_ firstArray:[Int], _ secondArray:[Int]) -> [Set<Int>] {
let intersection = Set(firstArray).intersection(Set(secondArray))
return [intersection]
}
commonValue(oneArray, twoArray)
```

## Question 36√

Find the most-frequently appearing Array of Ints in an Array of Arrays of Ints.

```swift
var myArray = [[4,5,6,7,5,4,54,4,4,4,1], [4,5,6,7,5,3,4,4]]

func myArrayOfArrays (arr: [[Int]]) -> String {
var result = String()
// Create dictionary to map value to count
var counts = [Int: Int]()
for arr in arr {
// Count the values with using forEach
arr.forEach { counts[$0] = (counts[$0] ?? 0) + 1 }
// Find the most frequent value and its count with max(by:)
if let (value, count) = counts.max(by: {$0.1 < $1.1}) {
result = "the \(value) occurs \(count) times "
}
}
return result
}
myArrayOfArrays(arr: myArray)
```

## Question 37√

Given a String as input, rotate all a-z characters by one.  This is called [ROT-1 encryption](http://www.rot-n.com/).

Sample input:
`This is a test string. Anything can be written in here (even Zebras and zebras).`

Sample output:
`Uijt jt b uftu tusjoh. Bozuijoh dbo cf xsjuufo jo ifsf (fwfo Afcsbt boe afcsbt).`


```swift
func encrypt(_ message: String, _ shift: Int) -> String {

func shiftLetter(ucs: UnicodeScalar) -> UnicodeScalar {
let firstLetter = Int(UnicodeScalar("A").value)
let lastLetter = Int(UnicodeScalar("Z").value)
let letterCount = lastLetter - firstLetter + 1

let value = Int(ucs.value)
switch value {
case firstLetter...lastLetter:
// Offset relative to first letter:
var offset = value - firstLetter
// Apply shift amount (can be positive or negative):
offset += shift
// Transform back to the range firstLetter...lastLetter:
offset = (offset % letterCount + letterCount) % letterCount
// Return corresponding character:
return UnicodeScalar(firstLetter + offset)!
default:
// Not in the range A...Z, leave unchanged:
return ucs
}
}

let msg = message.uppercased()
return String(String.UnicodeScalarView(msg.unicodeScalars.map(shiftLetter)))
}

print(encrypt(message, 1).lowercased())
```
