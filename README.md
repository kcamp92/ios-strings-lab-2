# Strings Lab 2

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.

## Question 1     

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"

// Your code
```
Example

Input:
`var problem ="split this string into words and print them on separate lines"`

Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines

```

```
var sentence = "split this string into words and print them on separate lines "
var space = " "
var currentWord = ""

for character in sentence {
if String (character) == space {
print(currentWord)
currentWord = ""
continue
}
currentWord += String(character)
}
```
## Question 2

Given a string `testString` create a new variable called `condensedString` that has any consecutive spaces in `testString` replaced with a single space.

```swift
let testString = "  How   about      thesespaces  ?  "
//condensedString = " How about thesespaces ? "
```

```
let testString = "  How   about      these spaces  ?  "
let condensedString = " How about these spaces ? "
var stringArray = testString.components(separatedBy: .whitespacesAndNewlines)
print(stringArray)
var currentArray = ""

for character in stringArray {
if character == "" {
continue
}
currentArray += character + " "

}
print (currentArray)
```

## Question 3

Given a string with multiple words. Reverse the string word by word.

Example:

Sample Input: `"Swift is the best language"`

Sample Output: `"language best the is Swift"`

```
let string = "Swift is the best language"
var myString = "Swift is the best language"

myString = String(string.reversed())
print(myString)
```

## Question 4

Given a string with multiple words. Write code that prints how many of them are palindromes.

Example:

Sample Input: `"danaerys dad cat civic bottle"`

Sample Output: `2`

```
let string = "danaerys dad cat civic bottle"
var stringComponents = string.components(separatedBy: " ")
var count = 0

var reversedString = String(string.reversed())
string == reversedString

for i in stringComponents {
if  i == String(i.reversed()) {
count += 1
}

}
print(count)
```

## Question 5

You are given a string representing an **attendance record** for a student. The record only contains the following three characters:

`'A' : Absent.`

`'L' : Late.`

`'P' : Present.`

If a student has more than one 'A' or more than 2 continuous 'L's that student should not be rewarded. Print true if student is to be rewarded and False if they shouldn't.

Example:

Sample Input: `"PPALLP"`

Sample Output: `true`

```
let attendanceRecord = "PPALLP"

let attendanceRecord = "PPALLP"

var a = "A"
var l = "L"
var countA = 0
var countL = 0

for i in attendanceRecord {
if String(i) == a {
countA += 1
}
if countA >= 2 {
print(false)

break
}
if String(i) == l {
countL += 1
}
if countL >= 3 {
print (false)
} else {
print(true)

break
}
}
```

## Question 6

Given a tuple with two strings. The first string is a **ransom note**, the second string being the characters from a magazine. Determine whether or not you can construct the ransom note using the characters from the magazine.

Each letter from the magazine can only be used once. You can assume all letters are lowercased.

Examples:

Sample Input1: `("a", "b")`

Sample Output1: `False`

Sample Input2: `("aa", "aab")`

Sample Output2: `True`

```
var tuple1 = ("a", "b")
var tuple2 = ("aa", "aab")

if tuple1.1.contains(tuple1.0.replacingOccurrences(of: " ", with: ""))
{
print(true)
} else {
print(false)
}
if tuple2.1.contains(tuple2.0.replacingOccurrences(of: " ", with: ""))
{
print(true)
} else {
print(false)
}
```
