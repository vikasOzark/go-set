# Go-Set

`Go-Set` is a generic implementation of a **Set** data structure in Go. A set is a collection of unique elements, and this implementation provides common set operations such as adding, removing, checking membership, and retrieving all elements.

## Features

- **Generic Implementation**: Works with any comparable type (`T comparable`).
- **Efficient Operations**: Uses a `map` under the hood for O(1) time complexity for most operations.
- **Common Set Methods**: Includes methods for adding, removing, checking membership, retrieving all elements, and getting the size of the set.

## Installation

To use this package, include it in your Go project by importing it:

```go
import "github.com/vikasOzark/go-set"
```

## Usage
Creating a New Set
To create a new set, use the NewSet function.
```go
package main

import (
    "fmt"
    "github.com/vikasOzark/go-set"
)

func main() {
    // Create a new set of integers
    intSet := goset.NewSet[int]()

    // Add elements to the set
    intSet.Add(1)
    intSet.Add(2)
    intSet.Add(3)

    // Check if an element exists
    fmt.Println("Contains 2:", intSet.In(2)) // Output: true

    // Remove an element
    intSet.Remove(2)

    // Get all elements
    fmt.Println("Elements:", intSet.Values()) // Output: [1 3]

    // Get the size of the set
    fmt.Println("Size:", intSet.Size()) // Output: 2
}
```