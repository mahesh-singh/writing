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
6. Pass a slice as a parameter to a function, and have that function modify the original slice
  
pass a slice as a parameter to a function, and have that function modify the original slice, then you have to pass a pointer to the slice:
```
```
# Others

1. OLAP: Online analytical processing
2. OLTP: Online transaction processing
3. OLAP vs OLTP: Example: retail company with many store at differet location. Processing real time orders are OLTP. Later analysing the data will be done via OLAP.
4. 

func myAppend(list *[]string, value string) {
    *list = append(*list, value)
}
```
