# Libft - @42Born2Code

A custom C standard library containing re-implementations of essential standard C library functions, along with additional utility functions for memory management, string manipulation, and linked list handling.

---

## 📌 Overview

**Libft** (Library of functions) is the first project of the 42 core curriculum. The goal of this project is to create a custom C library (`libft.a`) from scratch. Understanding these fundamental C functions and rebuilding them by hand builds a deep foundation in memory management, pointer arithmetic, dynamic allocation (`malloc`), and basic data structures.

---

## 📑 Content

The library is divided into three main categories:

### 1. Standard C Library Functions (`libc`)
Re-implementations of standard C library functions, prefixed with `ft_`:

* **Memory:** `ft_memset`, `ft_bzero`, `ft_memcpy`, `ft_memmove`, `ft_memchr`, `ft_memcmp`, `ft_calloc`
* **String Analysis & Search:** `ft_strlen`, `ft_strchr`, `ft_strrchr`, `ft_strncmp`, `ft_strnstr`
* **String Copy & Concatenation:** `ft_strlcpy`, `ft_strlcat`
* **Character Checks & Conversion:** `ft_isalpha`, `ft_isdigit`, `ft_isalnum`, `ft_isascii`, `ft_isprint`, `ft_toupper`, `ft_tolower`
* **Conversion:** `ft_atoi`
* **Memory Copy/Duplicate:** `ft_strdup`

---

### 2. Additional Functions
Utility functions that are not part of the standard `libc`, or are present in an alternative form:

* **`ft_substr`** — Extracts a substring from a string.
* **`ft_strjoin`** — Concatenates two strings into a newly allocated string.
* **`ft_strtrim`** — Trims specified characters from the beginning and end of a string.
* **`ft_split`** — Splits a string into an array of strings using a delimiter character.
* **`ft_itoa`** — Converts an integer into a null-terminated string.
* **`ft_strmapi`** — Applies a function to each character of a string to create a new string.
* **`ft_striteri`** — Applies a function to each character of a string by reference.
* **`ft_putchar_fd`** — Outputs a character to a given file descriptor.
* **`ft_putstr_fd`** — Outputs a string to a given file descriptor.
* **`ft_putendl_fd`** — Outputs a string followed by a newline to a given file descriptor.
* **`ft_putnbr_fd`** — Outputs an integer to a given file descriptor.
* **`ft_putunbr_fd`** — Outputs an unsigned integer to a given file descriptor.

---

### 3. Bonus Functions (Linked Lists)
Functions for manipulating singly linked lists using the `t_list` structure:

```
typedef struct s_list
{
    void            *content;
    struct s_list   *next;
}   t_list;

```

* **`ft_lstnew`** — Creates a new list node.
* **`ft_lstadd_front`** — Adds a new node at the beginning of the list.
* **`ft_lstsize`** — Counts the number of nodes in a list.
* **`ft_lstlast`** — Returns the last node of a list.
* **`ft_lstadd_back`** — Adds a new node at the end of the list.
* **`ft_lstdelone`** — Deletes a node and frees its memory using a custom function.
* **`ft_lstclear`** — Deletes and frees an entire list.
* **`ft_lstiter`** — Iterates over a list and applies a function to each node's content.
* **`ft_lstmap`** — Iterates over a list, applying a function to create a new list.

---

## 🛠 Compilation & Usage

### Compilation Rules

The provided `Makefile` includes the following standard targets:

| Command | Action |
| --- | --- |
| `make` / `make all` | Compiles mandatory functions and builds `libft.a`. |
| `make bonus` | Compiles mandatory and bonus (linked list) functions into `libft.a`. |
| `make clean` | Removes object files (`.o`). |
| `make fclean` | Removes object files and `libft.a`. |
| `make re` | Performs a clean rebuild (`fclean` + `all`). |

---

### Integrating Libft into Your Project

1. **Clone the repository:**
```bash
git clone [https://github.com/davidrps/42_libft.git](https://github.com/davidrps/42_libft.git) libft

```


2. **Compile the library:**
```bash
cd libft
make

```


3. **Include the header in your C file:**
```c
#include "libft.h"

```


4. **Compile your program with `libft.a`:**
```bash
cc -Wall -Wextra -Werror main.c -L. -lft -o my_program

```



---

## 📜 License & Compliance

This project complies with 42 School's **Norminette** coding style rules and flags (`-Wall -Werror -Wextra`).