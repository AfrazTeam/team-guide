# GoLang Style Guide

## Table of Contents

1. [Formatting](#formatting)
1. [Naming Conventions](#naming-conventions)
1. [Imports](#imports)
1. [Comments](#comments)
1. [Error Handling](#error-handling)
1. [Concurrency](#concurrency)
1. [Testing](#testing)
1. [Packages](#packages)
1. [Interfaces](#interfaces)
1. [Pointers](#pointers)

## Formatting

```go
    // bad
    func  badFormatting()  {
        x:= 10
        if (x>5)  {
        fmt.Println("x is greater than 5")
    }}

    // good
    func goodFormatting() {
        x := 10
        if x > 5 {
            fmt.Println("x is greater than 5")
        }
    }

```

## Naming Conventions

```go
// bad


// good
var count int
var description string
```

## Imports

```go
// bad

// good

```

## Comments

```go
// bad
// i is an integer
var i int

// good
// count represents the total number of items
var count int

```

## Error Handling

```go
// bad
func badErrorHandling() {
    result, _ := someFunction()
    fmt.Println(result)
}

// good
func goodErrorHandling() {
    result, err := someFunction()
    if err != nil {
        log.Fatal(err)
    }
    fmt.Println(result)
}

```

## Concurrency

```go
// bad
func badConcurrency() {
    go func() {
        // Some concurrent logic
    }()
    time.Sleep(time.Second * 2) // Waiting for goroutine to finish
}

// good
func goodConcurrency() {
    var wg sync.WaitGroup
    wg.Add(1)
    go func() {
        defer wg.Done()
        // Some concurrent logic
    }()
    wg.Wait()
}

```

## Testing

```go
// bad

// good

```

## Packages

```go
// bad

// good

```

## Interfaces

```go
// bad

// good

```

## Pointers

```go
// bad

// good

```

**[⬆ back to top](#table-of-contents)**
