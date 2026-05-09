*This project has been created as part of the 42 curriculum by **fjose-hi**.*

# Libft

## Description

Libft is a custom C library developed as part of the 42 School curriculum.  
The objective of the project is to recreate a set of standard C library functions while gaining a deeper understanding of low-level programming concepts such as memory management, string manipulation, pointers, and data structures.

This project serves as a foundational library that will be reused throughout future 42 projects.

The library is compiled into a static archive named `libft.a`, which can then be linked to other C programs.

### Project Goals

The goals of this project are to:

- Reimplement commonly used libc functions
- Understand how standard library functions work internally
- Learn static library creation and usage
- Improve proficiency in the C programming language
- Practice clean, modular, and reusable code
- Develop a deeper understanding of memory allocation and pointer manipulation

---

# Instructions

## Compilation

Compile the mandatory part of the library:

```bash
make
```

Compile the bonus part:

```bash
make bonus
```

Remove object files:

```bash
make clean
```

Remove object files and the library:

```bash
make fclean
```

Recompile the entire project:

```bash
make re
```

---

## Using the Library

Include the header file in your project:

```c
#include "libft.h"
```

Compile your program together with the library:

```bash
cc main.c -L. -lft
```

Example:

```c
#include "libft.h"
#include <stdio.h>

int main(void)
{
    printf("%zu\n", ft_strlen("Libft"));
    return (0);
}
```

---

# Library Description

## Part 1 — Libc Functions

These functions are reimplementations of standard C library functions.

### Character Classification

- `ft_isalpha`
- `ft_isdigit`
- `ft_isalnum`
- `ft_isascii`
- `ft_isprint`

### String and Memory Manipulation

- `ft_strlen`
- `ft_memset`
- `ft_bzero`
- `ft_memcpy`
- `ft_memmove`
- `ft_strlcpy`
- `ft_strlcat`
- `ft_strchr`
- `ft_strrchr`
- `ft_strncmp`
- `ft_memchr`
- `ft_memcmp`
- `ft_strnstr`
- `ft_strdup`

### Character Conversion

- `ft_toupper`
- `ft_tolower`

### Conversion and Allocation

- `ft_atoi`
- `ft_calloc`

---

## Part 2 — Additional Functions

These are utility functions created to extend the standard library.

### String Utilities

- `ft_substr` — Extracts a substring from a string
- `ft_strjoin` — Concatenates two strings
- `ft_strtrim` — Removes specified characters from the beginning and end of a string
- `ft_split` — Splits a string according to a delimiter
- `ft_itoa` — Converts an integer into a string
- `ft_strmapi` — Applies a function to each character of a string
- `ft_striteri` — Iterates through a string and applies a function

### File Descriptor Output

- `ft_putchar_fd`
- `ft_putstr_fd`
- `ft_putendl_fd`
- `ft_putnbr_fd`

---

## Bonus Part — Linked Lists

The bonus part introduces singly linked list manipulation.

### Linked List Functions

- `ft_lstnew`
- `ft_lstadd_front`
- `ft_lstsize`
- `ft_lstlast`
- `ft_lstadd_back`
- `ft_lstdelone`
- `ft_lstclear`
- `ft_lstiter`
- `ft_lstmap`

### Linked List Structure

```c
typedef struct s_list
{
    void            *content;
    struct s_list   *next;
} t_list;
```

---

# Project Structure

```text
.
├── Makefile
├── libft.h
├── ft_*.c
├── ft_*.o
└── libft.a
```

---

# Rules and Constraints

This project follows the 42 School norm requirements.

## Compilation Flags

```bash
-Wall -Wextra -Werror
```

## Constraints

- No global variables
- Functions must follow the Norminette coding style
- Only authorized functions may be used
- Memory leaks must be avoided

---

# Resources

## Documentation and References

### Official Documentation

- The C Standard Library documentation  
  https://cplusplus.com/reference/clibrary/

- Linux manual pages  
  https://man7.org/linux/man-pages/

- GNU C Library Documentation  
  https://www.gnu.org/software/libc/documentation.html

### Tutorials and Learning Resources

- GeeksforGeeks — C Programming  
  https://www.geeksforgeeks.org/c-programming-language/

- Learn C  
  https://www.learn-c.org/

- Harvard CS50 Notes  
  https://cs50.harvard.edu/

---

## AI Usage Disclosure

Artificial Intelligence tools were used during the development of this project for:

- Clarifying concepts related to C programming
- Understanding function behavior and edge cases
- Improving documentation quality
- Reviewing explanations of memory management concepts
- Generating README structure and formatting suggestions

AI was **not** used to automatically generate or replace the implementation logic of mandatory project functions without understanding or manual verification.

---

# Future Usage

This library will be reused in future 42 projects such as:

- ft_printf
- get_next_line
- push_swap
- so_long
- minishell
- cub3D

---

# Author

Felipe Hillebrand

GitHub: https://github.com/felipehillebrand-ops

---

# License

This project was developed for educational purposes as part of the 42 curriculum.
