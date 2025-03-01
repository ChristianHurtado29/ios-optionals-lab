# Optionals lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1

a. Given the variable `userNameOne` below, print *"The username is Test User"*.  Use *Optional Binding* (`if let`) to print the name.

```swift
var userNameOne: String? = "Test User"
```
ANSWER
```
var userNameOne: String?
userNameOne = "Test User"

if let UserName = userNameOne {
    print("The user name is \(UserName)")
} else {
    print("The user name is invalid")
}
```

b. Given the variable `userNameTwo` below, print *"The username is undefined"*.  Use the *nil coalescing operator* (`??`).

```swift
var userNameTwo: String? = nil
```
ANSWER
```
Swift
var userNameTwo: String? = nil
print("The username is \(userNameTwo ?? "undefined")")
```

## Question 2

a. Given the variables `rectOneWidth` and `rectOneHeight` below, print "The area of rectOne is 50".  Use *Optional Binding* (`if let`) to print the area.

```swift
var rectOneWidth: Double? = 5
var rectOneHeight: Double? = 10
```
ANSWER
```
var rectOneWidth: Double? = 5
var rectOneHeight: Double? = 10

if let width = rectOneWidth, let height = rectOneHeight {
    print("the area of the rectangle is \(height * width)")
}
```

b. Given the variables `rectTwoWidth` and `rectTwoHeight` below, print "The are of rectTwo is not able to be calculated".  Use *Optional Binding* (`if let`) to print this message.

```swift
var rectTwoWidth: Double? = nil
var rectTwoHeight: Double? = nil
```
ANSWER
```
var rectTwoWidth: Double? = nil
var rectTwoHeight: Double? = nil

if let width = rectTwoWidth, let height = rectTwoHeight {
    print("the area of the rectTwo is \(width * height )")
} else {
    print("the area of rectTwo is unable to be calculated")
}
```

## Question 3

a. Given the variables `userOneName`, `userOneAge`, and `userOneHeight` below, write code that prints "Hello Anne!  You are 15 years old and 5.8 feet tall" (1 foot = 12 inches).  Use optional binding.


```swift
var userOneName: String? = "Anne"
var userOneAge: Int? = 15
var userOneHeight: Double? = 70
```
ANSWER
```
var userOneName: String? = "Anne"
var userOneAge: Int? = 15
var userOneHeight: Double? = 70
if let name = userOneName, let age = userOneAge, let height = userOneHeight {
 let forammtedString = String(format: "%.1f", height / 12)
print("Hello \(name)! You are \(age) years old and \(forammtedString) feet tall")
}
```

b. Given the variables `userTwoName`, `userTwoAge` and `userTwoHeight` below, write code that prints "Hello user!  You are 15 years old and I don't know how tall you are".  Use optional binding

```swift
var userTwoName: String? = nil
var userTwoAge: Int? = 15
var userTwoHeight: Double? = nil
```


## Question 4

Give the variable `favoriteNumber`, write code that either prints "Your favorite number is " followed by the number, or "I don't know what your favorite number is"

`favoriteNumber` is of type Int? and will either be `nil` or a random number between 0 and 10.  It will change each time you run your Playground.

```swift
var favoriteNumber = Bool.random() ? Int.random(in: 0...10) : nil
```
ANSWER
```
var favoriteNumber = Bool.random() ? Int.random(in: 0...10) : nil
if favoriteNumber == nil{
print("I don't know your favorite number.")
} else {print("Your favorite number is \(String(describing: favoriteNumber))")
}

```


## Question 5

Given the variables `numOne`, `numTwo` and `numThree`, write code that prints "The sum of all the numbers is " followed by their sum.  If a number is `nil`, don't add it to the sum.  If all numbers are `nil`, the sum is zero.

```swift
var numOne = Bool.random() ? Int.random(in: 0...10) : nil
var numTwo = Bool.random() ? Int.random(in: 0...10) : nil
var numThree = Bool.random() ? Int.random(in: 0...10) : nil
```
ANSWER
```
var numOne = Bool.random() ? Int.random(in: 0...10) : nil
var numTwo = Bool.random() ? Int.random(in: 0...10) : nil
var numThree = Bool.random() ? Int.random(in: 0...10) : nil

// append the variable to an optional array
var numbers = [numOne, numTwo, numThree]
var sum = 0
for num in numbers {
    if let validNumber = num {
        sum += validNumber
    }
}
print("The sum of our variables is \(sum)")
```

## Question 6

a. Given the variable `numbers` below, write code that prints "The sum of all the numbers is " followed by their sum.  If a number is `nil`, don't add it to the sum.  If all numbers are `nil`, the sum is zero.

```swift
var numbers = [Int?]()

for _ in 0..<10 {
    numbers.append(Bool.random() ? Int.random(in: 0...100) : nil)
}
```

b. Using the same variable, find the average of all non-nil values.

## Extra Questions

https://github.com/joinpursuit/Pursuit-Core-iOS-Extra-Optionals-Questions/blob/master/README.md
