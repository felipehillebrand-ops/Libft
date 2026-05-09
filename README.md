# Libft

> A custom C library developed as part of the 42 School curriculum.

## 📚 About

Libft is the first foundational project in the 42 curriculum.  
The objective is to recreate a collection of standard C library functions from scratch, while also implementing additional utility functions that will be reused throughout future projects.

This project strengthens understanding of:

- Memory management
- String manipulation
- Pointer arithmetic
- Linked lists
- Modular programming
- Static libraries in C
- Low-level programming concepts

The library is compiled into a static archive (`libft.a`) that can be linked into future C projects.

---

## ⚙️ Compilation

Compile the mandatory part:

```bash
make
```

Compile including bonus functions:

```bash
make bonus
```

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

## 📦 Library Structure

### Part 1 — Libc Functions

Re-implementations of standard C library functions.

#### Character Checks

- `ft_isalpha`
- `ft_isdigit`
- `ft_isalnum`
- `ft_isascii`
- `ft_isprint`

#### String & Memory Functions

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

#### Conversion Functions

- `ft_atoi`
- `ft_toupper`
- `ft_tolower`

#### Memory Allocation

- `ft_calloc`

---

### Part 2 — Additional Functions

Custom utility functions not included in the standard libc.

- `ft_substr`
- `ft_strjoin`
- `ft_strtrim`
- `ft_split`
- `ft_itoa`
- `ft_strmapi`
- `ft_striteri`
- `ft_putchar_fd`
- `ft_putstr_fd`
- `ft_putendl_fd`
- `ft_putnbr_fd`

---

### Bonus Part — Linked Lists

Singly linked list manipulation functions.

- `ft_lstnew`
- `ft_lstadd_front`
- `ft_lstsize`
- `ft_lstlast`
- `ft_lstadd_back`
- `ft_lstdelone`
- `ft_lstclear`
- `ft_lstiter`
- `ft_lstmap`

---

## 🛠️ Usage

Include the header in your project:

```c
#include "libft.h"
```

Compile your project with the library:

```bash
cc main.c -L. -lft
```

Example:

```c
#include "libft.h"
#include <stdio.h>

int main(void)
{
    char str[] = "libft";

    printf("Length: %zu\n", ft_strlen(str));
    return (0);
}
```

---

## 📁 Project Structure

```text
.
├── Makefile
├── libft.h
├── ft_*.c
├── ft_*.o
└── libft.a
```

---

## ✅ Rules & Constraints

This project follows the 42 School norm requirements:

- No global variables
- Compilation flags:
  - `-Wall`
  - `-Wextra`
  - `-Werror`
- Only allowed functions may be used
- Code must follow the Norminette style guide

---

## 🧪 Testing

The library can be tested using:

- Norminette
- Custom unit tests
- Community testers such as:
  - Tripouille libftTester
  - libft-war-machine

---

## 🚀 Goals of the Project

Through Libft, the goal is to learn how standard C functions work internally by rebuilding them manually.  
This project serves as the base library for many future 42 projects such as:

- ft_printf
- get_next_line
- so_long
- push_swap
- minishell
- cub3D

---

## 👨‍💻 Author

Felipe José Hillebrand

GitHub: https://github.com/felipehillebrand-ops

---

## 📄 License

This project is for educational purposes as part of the 42 curriculum.
