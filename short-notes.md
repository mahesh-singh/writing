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
  
Function to modify the original slice, then need to pass a pointer to the slice as  a parameter to a function:
```
func myAppend(list *[]string, value string) {
    *list = append(*list, value)
}
```

7. Method receiver - value recevier & pointer recevier

```
type MyStruch struc {
 Value int
}

// value receiver
func(m MyStruct)PrintMe() {
 
}

//pointer revevier
func(m *MyStruct)PrintMe() {
}

```

8. Slice: Hold the ref to array (pointer)
9. Type assertion: apply to interface value x.(t) where x is interface expression and T is type
10. Derefrencing pointer: Give us access to the value that pointer point to. * is also used to “dereference” pointer variables. Dereferencing a pointer gives us access to the value the pointer points to.
11. & address operator, * retrive value stored at address
12. 
```
x :=1
p = &x
fmt.Println(*p) // 1
*p = 2 // sets a x = 2

```
13. Slice where each element is a array of size 2

```
pairs  = [][2]int
```

14. Access Characters of String in Go

  create and initialize a string
  
  `name := "Programiz"`

  access first character
  
  `fmt.Printf("%c\n", name[0])  // P`

  access fourth character
  
  `fmt.Printf("%c\n", name[3])  // g`

  access last character
  
  `fmt.Printf("%c", name[8])  // z`

 15. Trim spaces

```
strings.TrimSpace(s)
```

# Others

1. OLAP: Online analytical processing
2. OLTP: Online transaction processing
3. OLAP vs OLTP: Example: retail company with many store at differet location. Processing real time orders are OLTP. Later analysing the data will be done via OLAP.

