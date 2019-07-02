# Strings Lab 1

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit

## Question 1

Write code that prints out all the numbers from 1 to 10 as a single string.
(Hint: the `String()` function can convert an Int to a String)

```swift
let numbers = 1...10
var str = ""

for n in 1...10{
    str+=("\(String(n)) ")
    }
print(str)
```

***
## Question 2

Write code that prints out all the even numbers from 5 to 51 as a single string.

```swift
let range2 = 5...51
var str = ""
for n in range2 {
    if n % 2 == 0 {
        str+=("\(String(n)) ")
        }
    }
print(str)
```

***
## Question 3

Write code that prints out every number ending in 4 between 1 and 60 as a single string.

```swift
let range3 = 1...60
var str = ""

for n in range3 {
    if n % 10 == 4 {
        str+=("\(String(n)) ")
    }
}
print(str)
```

***
## Question 4

Print each character in the string `"Hello world!"`

```swift
var str = "Hello world!"

for c in str {
    print(c)
}
```

***
## Question 5

Print out the last character in the string below.  You cannot use the Character literal "!" (i.e you must access `myStringSeven`'s characters).

`let myStringSeven = "Hello world!"`

```swift
let myStringSeven = "Hello world!"
//long way
for c in myStringSeven {
    if c == "!" {
        print(c)
    }
}

//short way
print(myStringSeven.last!)
```

***
## Question 6

Write code that switches on a string, given the following conditions:
- If the string's length is even, print out every character.
- If the string's length is odd, print out every other character.

```swift
var str = "Hello world!"

if str.count % 2 == 0 {
    for c in str {
        print(c)
    }
}
else {
    for (index, element) in str.enumerated() {
        if index % 2 != 0 {
            print(element)
        }
    }
}
```

***
## Question 7

Initialize a String with a character. Show that it is a Character, and not another String, that you're using to initialize it.

```swift
var a: Character = "A"

let myCharacters: [Character] = ["l", "o", "v", "e"]
let myString = String(myCharacters)
print(myString)
```

***
## Question 8

Build five pairs of **canonically equivalent** strings, the first of each being a pre-composed character and the second being one that uses combinable unicode scalars. Show that they are equivalent.

```swift
var a = "\u{E1}"
var e = "\u{E9}"
var i = "\u{ED}"
var o = "\u{F3}"
var u = "\u{FA}"

var a2 = "\u{61}\u{301}"
var e2 = "\u{65}\u{301}"
var i2 = "\u{69}\u{301}"
var o2 = "\u{6F}\u{301}"
var u2 = "\u{75}\u{301}"


if a == a2{
    print("\(a) and \(a2) are equivalent")
}

if e == e2{
    print("\(e) and \(e2) are equivalent")
}

if i == i2{
    print("\(i) and \(i2) are equivalent")
}

if o == o2{
    print("\(o) and \(o2) are equivalent")
}

if u == u2{
    print("\(u) and \(u2) are equivalent")
}
```

***
## Question 9

**Using only Unicode**, print out `"HELLO WORLD!"`

```swift
var h = "\u{48}"
var e = "\u{45}"
var l = "\u{4C}"
var o = "\u{4F}"
var space = "\u{A0}"
var w = "\u{57}"
var r = "\u{52}"
var d = "\u{44}"
var exclamation = "\u{21}"

print("\(h)\(e)\(l)\(l)\(o)\(space)\(w)\(o)\(r)\(l)\(d)\(exclamation)")
```

***
## Question 10

**Using only Unicode**, print out your name.

```swift
var m = "\u{4D}"
var a = "\u{41}"
var r = "\u{52}"
var i = "\u{49}"
var e = "\u{45}"
var l = "\u{4C}"

print("\(m)\(a)\(r)\(i)\(e)\(l)")
```


***
## Question 11

**Using only Unicode**, print out `"HELLO WORLD!"` in another language.

```swift
var h = "\u{48}"
var o = "\u{4F}"
var l = "\u{4C}"
var a = "\u{41}"
var space = "\u{A0}"
var m = "\u{4D}"
var u = "\u{55}"
var n = "\u{4E}"
var d = "\u{44}"
var exclamation = "\u{21}"

print("\(h)\(o)\(l)\(a)\(space)\(m)\(u)\(n)\(d)\(o)\(exclamation)")

```

***
## Question 12

Print the below flower box using the following information.

- The unicode number for ⚘ is U-2698
- The top and bottom of the box are represented by dashes and the rows are |
- Use the terminator argument in your print statements to print on the same line.
- Hint: It may be useful to try printing out a box of just one character to start then work your way from there.

```swift
Flower Box:
- - - - - - - - - - -
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
- - - - - - - - - - -
```
```swift
let topBotton = String(repeating: "- ", count: 11)
let flower = String(repeating: "| \u{2698} ", count: 5)
print(topBotton)
for _ in 0...7 {
    print("\(flower)|")
}
print(topBotton)
```


***
## Question 13

Write a program that sets up a chess board using Unicode.

```swift
Chess Board:
♖ ♘ ♗ ♕ ♔ ♗ ♘ ♖
♙ ♙ ♙ ♙ ♙ ♙ ♙ ♙




♟ ♟ ♟ ♟ ♟ ♟ ♟ ♟
♜ ♞ ♝ ♛ ♚ ♝ ♞ ♜
```

```swift
var rook = "\u{2656}"
var knight = "\u{2658}"
var bishop = "\u{2657}"
var queen = "\u{2655}"
var king = "\u{2656}"
var pawn = "\u{2659}"

var rookBlack = "\u{265C}"
var knightBlack = "\u{265E}"
var bishopBlack = "\u{265D}"
var queenBlack = "\u{265B}"
var kingBlack = "\u{265A}"
var pawnBlack = "\u{265F}"

print("\(rook) \(knight) \(bishop) \(queen) \(king) \(bishop) \(knight) \(rook)")
print(String(repeating: "\(pawn) ", count: 8))

for _ in 0...5 {
    print(" ")
}

print(String(repeating: "\(pawnBlack) ", count: 8))
print("\(rookBlack) \(knightBlack) \(bishopBlack) \(queenBlack) \(kingBlack) \(bishopBlack) \(knightBlack) \(rookBlack)")
```

***
## Question 14

You are given a string stored in the variable `aString`. Create new string named `replacedString` that contains the characters of the original string with all the occurrences of the character `"e"` replaced by `"\*"`.

```swift
var aString = "Replace the letter e with *"
var replacedString = aString.replacingOccurrences(of: "e", with: "*")
print(replacedString)
 ```

Example:

Input:
`var aString = "Replace the letter e with *"`

Expected values:
`replacedString = "R*plac* th* l*tt*r * with *"`

***
## Question 15

You are given a string stored in variable `aString`. Create a new string called `reverse` that contains the original string in reverse order. Print the reversed string.

```swift
var aString = "this string has 29 characters"
var reverse = ""

// Your code here
reverse = String(aString.reversed())
print(reverse)
```

Example:
Input:
`var aString = "Hello"`

Output:
`"olleH"`

***
## Question 16

You are given a string stored in variable `aString`. Print `true` if `aString` is a palindrome, and `false` otherwise. A **palindrome** is a string which reads the same backward or forward.

```swift
let aString = "anutforajaroftuna"

// Your code here
let aString = "anutforajaroftuna"
var reverse = String(aString.reversed())

if aString == reverse {
    print(true)
    } 
    else {
        false
}

```

Example 1:
Input:
`var aString = "anutforajaroftuna"`

Output:
`true`

Example 2:
Input:
`var aString = "Hello"`

Output:
`false`

***
## Question 17

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"

// Your code
var problemSplit = problem.replacingOccurrences(of: " ", with: "\n")
print(problemSplit)

```

Example:
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

***
## Question 18

You are given a string stored in variable `problem`. Write code that prints the longest word in the string.

```swift
var problem = "find the longest word in the problem description"

// Your code here
var problemSplit = problem.split(separator: " ")

var longest = ""

for word in problemSplit {
    if word.count > longest.count {
        longest = String(word)
    }
}

print(longest)
```

Example:
Input:
`var problem = "find the longest word in the problem description"`

Output:
`description`

Hint: Keep track of the longest word you encounter and also keep track of its length.

***
## Question 19

Given a string in English, create a tuple containing the number of vowels and consonants.

```swift
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"
let input = "Count how many vowels I have!"

var numberOfConsonants = 0
var numberOfVowels = 0

for c in input {
if vowels.contains(c) {
    numberOfVowels+=1
    }
    else if consonants.contains(c){
        numberOfConsonants+=1
    }
}
print("\(numberOfVowels), \(numberOfConsonants)")
```

***
## Question 20

Given a string of words separated by a `" "`. Write code that prints out the length of the last word.

If there is no last word print out `"No last word"`.

Example:
Input: `"How are you doing this Monday?"`

Output: `7`

```swift
var input = "How are you doing this Monday?"
var arr = input.split(separator: " ")

print(arr.last?.count ?? "No last word")
```

***
