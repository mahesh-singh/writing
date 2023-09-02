# Short notes

## Golang

1. Declare empty string array

```Stack := []string{ }```

2. Need to a list of items on which contains check needed 

Declare map

```Operators := map[string]bool{ "+": true, "-": true, "*": true, "/": true}```

3. Declare empty slice
```
mySlice1 := make([]int, 0)
mySlice2 := []int{}
```
4. Atoi - ASCII to integer
5. Convert string to integer 

strconv implements conversions
```
//string to int
i, err := strconv.Atoi("-42")

//Int to string
s := strconv.Itoa(-42)
```

