# Short notes

## Golang


 ### Need to a list of items on which contains check needed 

Declare map

```Operators := map[string]bool{ "+": true, "-": true, "*": true, "/": true}```

-----

### Declare empty slice
```
mySlice1 := make([]int, 0)
mySlice2 := []int{}
```
----

### Atoi - ASCII to integer

----
### Convert string to integer

-----

strconv implements conversions
```
//string to int
i, err := strconv.Atoi("-42")

//Int to string
s := strconv.Itoa(-42)
```

-----
### append to slice

```
s = make([]string, 3)
s[0] = "a"
s[1] = "b"
s[2] = "c"
s = append(s, "d")
s = append(s, "e", "f")
```
----
### Pass a slice as a parameter to a function, and have that function modify the original slice
  
Function to modify the original slice, then need to pass a pointer to the slice as  a parameter to a function:
```
func myAppend(list *[]string, value string) {
    *list = append(*list, value)
}
```
----
### Method receiver - value recevier & pointer recevier

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
-----
### Slice: Hold the ref to array (pointer)
-----
### Type assertion: apply to interface value x.(t) where x is interface expression and T is type

-----


### pointer (*) and address-of operator (&)

A pointer is a variable that stores the memory address of another variable.
```
var ptr *int // Declares a pointer to an integer
```

To assign the address of a variable to a pointer, you use the address-of operator & 
```
x := 42
ptr = &x // Assigns the address of 'x' to 'ptr'
```

To access the value stored at the memory address pointed to by a pointer, you can use the dereference operator *:
```
fmt.Println(*ptr) // Prints the value stored at the memory address 'ptr' points to (in this case, 42)

Derefrencing pointer: Give us access to the value that pointer point to. * is used to “dereference” pointer variables. 
```

Use & to get the memory address of a variable and assign it to a pointer

```
x := 42
ptr := &x // 'ptr' now contains the memory address of 'x'
```

Use & in function calls to pass variables by reference, allowing functions to modify the original values

```
func modifyValue(v *int) {
    *v = *v * 2
}

x := 10
modifyValue(&x) // Passes 'x' by reference, so 'x' will be modified to 20
```
------
### Slice where each element is a array of size 2

```
pairs  = [][2]int
```
------

### Access Characters of String in Go

  create and initialize a string
  
  `name := "Programiz"`

  access first character
  
  `fmt.Printf("%c\n", name[0])  // P`

  access fourth character
  
  `fmt.Printf("%c\n", name[3])  // g`

  access last character
  
  `fmt.Printf("%c", name[8])  // z`

------

### Trim spaces

```
strings.TrimSpace(s)
```
-----

### For loop on map

```
for k, v := range m { 
    fmt.Printf("key[%s] value[%s]\n", k, v)

}
```
-----

### Get small case alphabets index in array of 26 length

```
  arr := [26]string
//to store a at index 0
arr['a'-'a'] = "a"
//to store c at index 2
arr['c'-'a'] = "c"
```

### How to clean up go.mod file by removing the dependency which are unused

```
go mod tidy
```
It also add dependencies which are used but not added into the go.mod file

### What is the role of go.sum

```
Its ensure module integrity by adding checksum in go.sum file. It is used the check modules while downloading via checksum. It is also used for version pinning  
```

---------
---------

# Docker

### Pull the image from one repo, tag it and push it to the new registry.

```
docker pull old-registry/app:some_tag
docker tag old-registry/app:some_tag new-registry/app:some_tag
docker push new-registry/app:some_tag
```
-----

### How to get into the docker container via docker-compose 
```
docker-compose run web bash

//--service-ports expose the service ports on the host
docker-compose run --service-ports web bash
```



-----
-----
# Others

1. OLAP: Online analytical processing
2. OLTP: Online transaction processing
3. OLAP vs OLTP: Example: retail company with many store at differet location. Processing real time orders are OLTP. Later analysing the data will be done via OLAP.

