*This project has been created as part of the 42 curriculum by **fjose-hi**.*

# Libft

A custom static C library developed as part of the 42 curriculum. This project recreates several standard C library functions while introducing additional utility functions and linked list management tools that can be reused throughout future projects.

---

## Description

Libft is one of the foundational projects in the 42 curriculum. The goal of the project is to deepen the understanding of low-level programming concepts in C by rebuilding commonly used standard library functions from scratch.

The project focuses on:

- Understanding memory management and pointer manipulation.
- Reimplementing functions from the standard C library.
- Creating reusable utility functions.
- Learning how static libraries work.
- Writing clean and maintainable code following the 42 Norm.

The final result is a static library called `libft.a`, which can be linked into future C projects.

This library includes:

- Character and string manipulation functions.
- Memory handling functions.
- Conversion utilities.
- File descriptor output functions.
- Linked list utilities (bonus part).

---

## Features

### Mandatory Functions

#### Character Checks & Conversion

| Function | Description |
|---|---|
| `ft_isalpha` | Checks if a character is alphabetic |
| `ft_isdigit` | Checks if a character is a digit |
| `ft_isalnum` | Checks if a character is alphanumeric |
| `ft_isascii` | Checks if a character is ASCII |
| `ft_isprint` | Checks if a character is printable |
| `ft_toupper` | Converts lowercase letters to uppercase |
| `ft_tolower` | Converts uppercase letters to lowercase |

### String Functions

| Function | Description |
|---|---|
| `ft_strlen` | Calculates string length |
| `ft_strlcpy` | Copies strings safely |
| `ft_strlcat` | Concatenates strings safely |
| `ft_strchr` | Locates a character in a string |
| `ft_strrchr` | Locates the last occurrence of a character |
| `ft_strncmp` | Compares strings |
| `ft_strnstr` | Finds a substring in a string |
| `ft_strdup` | Duplicates a string |
| `ft_substr` | Extracts a substring |
| `ft_strjoin` | Concatenates two strings |
| `ft_strtrim` | Trims characters from a string |
| `ft_split` | Splits a string into an array |
| `ft_strmapi` | Applies a function to each character |
| `ft_striteri` | Iterates through a string applying a function |

### Memory Functions

| Function | Description |
|---|---|
| `ft_memset` | Fills memory with a constant byte |
| `ft_bzero` | Sets bytes to zero |
| `ft_memcpy` | Copies memory areas |
| `ft_memmove` | Copies memory safely between overlapping areas |
| `ft_memchr` | Searches memory |
| `ft_memcmp` | Compares memory areas |
| `ft_calloc` | Allocates and initializes memory |

### Conversion Functions

| Function | Description |
|---|---|
| `ft_atoi` | Converts a string to an integer |
| `ft_itoa` | Converts an integer to a string |

### File Descriptor Functions

| Function | Description |
|---|---|
| `ft_putchar_fd` | Writes a character to a file descriptor |
| `ft_putstr_fd` | Writes a string to a file descriptor |
| `ft_putendl_fd` | Writes a string followed by a newline |
| `ft_putnbr_fd` | Writes a number to a file descriptor |

---

## Bonus Part — Linked List Functions

The bonus section introduces a linked list API based on the `t_list` structure.

```c
typedef struct s_list
{
    void            *content;
    struct s_list   *next;
}   t_list;
```

| Function | Description |
|---|---|
| `ft_lstnew` | Creates a new list node |
| `ft_lstadd_front` | Adds a node at the beginning |
| `ft_lstsize` | Counts the number of nodes |
| `ft_lstlast` | Returns the last node |
| `ft_lstadd_back` | Adds a node at the end |
| `ft_lstdelone` | Deletes a single node |
| `ft_lstclear` | Clears an entire list |
| `ft_lstiter` | Iterates through the list |
| `ft_lstmap` | Creates a new list applying a function |

---

## Project Structure

```text
.
├── Makefile
├── libft.h
├── ft_*.c
└── bonus functions
```

---

## Instructions

### Clone the Repository

```bash
git clone https://github.com/felipehillebrand-ops/Libft.git
cd Libft
```

### Compilation

Compile mandatory functions:

```bash
make
```

Compile bonus functions:

```bash
make bonus
```

### Cleaning Object Files

Remove object files:

```bash
make clean
```

Remove object files and library:

```bash
make fclean
```

Recompile everything:

```bash
make re
```

---

## Using the Library

Include the header in your project:

```c
#include "libft.h"
```

Compile your program with the library:

```bash
cc main.c libft.a
```

Example:

```c
#include "libft.h"
#include <stdio.h>

int main(void)
{
    printf("%d\n", ft_strlen("42"));
    return (0);
}
```

---

## Technical Choices

This project follows the requirements defined by the 42 subject:

- Written entirely in C.
- Compiled with the flags:

```bash
-Wall -Wextra -Werror
```

- No global variables.
- Fully compliant with the 42 Norm.
- Static library generated using `ar`.

---

## Testing

The project can be tested using:

- `norminette`
- `libftTester`
- `libft-war-machine`
- `Francinette`

Example:

```bash
norminette
```

---

## Resources

### Documentation & References

- The C Programming Language — Brian W. Kernighan & Dennis M. Ritchie
- Linux Manual Pages (`man` pages)
- POSIX documentation
- GNU C Library Documentation
- 42 Subject PDF for Libft

Useful online references:

- https://man7.org/linux/man-pages/
- https://cplusplus.com/reference/cstring/
- https://www.gnu.org/software/libc/documentation.html
- https://github.com/Tripouille/libftTester
- https://github.com/jtoty/Libftest

### AI Usage Disclosure

AI tools were used during this project for:

- Reviewing README structure and formatting.
- Clarifying concepts related to memory management and linked lists.
- Improving documentation quality and wording.
- Verifying explanations of standard C library behavior.

All implementation, debugging, testing, and final validation of the code were completed manually.

---

## Learning Outcomes

Through this project, the following concepts were strengthened:

- Memory allocation and management.
- Pointer arithmetic.
- String manipulation in C.
- Static library creation.
- Linked list data structures.
- Defensive programming.
- Modular code organization.
- Writing reusable utility functions.

---

## License

This project was developed for educational purposes as part of the 42 curriculum.

---

## Author

Felipe José Hillebrand

GitHub: https://github.com/felipehillebrand-ops
