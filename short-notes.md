# Short notes

## Golang


1. Need to a list of items on which contains check needed 

Declare map

```Operators := map[string]bool{ "+": true, "-": true, "*": true, "/": true}```

2. Declare empty slice
```
mySlice1 := make([]int, 0)
mySlice2 := []int{}
```
3. Atoi - ASCII to integer


4. Convert string to integer

 

strconv implements conversions
```
//string to int
i, err := strconv.Atoi("-42")

//Int to string
s := strconv.Itoa(-42)
```

5. append to slice

```
s = make([]string, 3)
s[0] = "a"
s[1] = "b"
s[2] = "c"
s = append(s, "d")
s = append(s, "e", "f")
```
